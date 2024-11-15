## ClassDef ScanParserProgramTest
Doc is waiting to be generated...
### FunctionDef test_scan(self)
```json
{
  "target_object": {
    "name": "Event",
    "description": "The Event class represents a specific occurrence that can be scheduled and managed within an application. It includes properties such as event name, date, location, and participants.",
    "properties": [
      {
        "name": "id",
        "type": "integer",
        "description": "A unique identifier for the event."
      },
      {
        "name": "name",
        "type": "string",
        "description": "The name of the event."
      },
      {
        "name": "date",
        "type": "datetime",
        "description": "The date and time when the event is scheduled to occur."
      },
      {
        "name": "location",
        "type": "string",
        "description": "The location where the event will take place."
      },
      {
        "name": "participants",
        "type": "array of integers",
        "description": "A list of user IDs representing participants in the event."
      }
    ],
    "methods": [
      {
        "name": "addParticipant",
        "parameters": [
          {
            "name": "userId",
            "type": "integer"
          }
        ],
        "return_type": "void",
        "description": "Adds a participant to the event. Accepts a user ID as an argument."
      },
      {
        "name": "removeParticipant",
        "parameters": [
          {
            "name": "userId",
            "type": "integer"
          }
        ],
        "return_type": "void",
        "description": "Removes a participant from the event. Accepts a user ID as an argument."
      },
      {
        "name": "updateLocation",
        "parameters": [
          {
            "name": "newLocation",
            "type": "string"
          }
        ],
        "return_type": "void",
        "description": "Updates the location of the event. Accepts a new location string as an argument."
      },
      {
        "name": "isParticipant",
        "parameters": [
          {
            "name": "userId",
            "type": "integer"
          }
        ],
        "return_type": "boolean",
        "description": "Checks if a user is a participant in the event. Accepts a user ID as an argument and returns true if the user is a participant, false otherwise."
      }
    ]
  }
}
```
***
