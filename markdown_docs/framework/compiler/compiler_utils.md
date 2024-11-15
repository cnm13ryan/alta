## FunctionDef _get_feed_forward_params(program_spec, config, dim_mappings, expanded_dim_mappings)
```json
{
  "name": "User",
  "description": "A representation of a user within the system.",
  "properties": {
    "userId": {
      "type": "integer",
      "description": "A unique identifier for the user."
    },
    "username": {
      "type": "string",
      "description": "The username chosen by the user, which is used to identify them within the system."
    },
    "email": {
      "type": "string",
      "description": "The email address associated with the user's account. This must be a valid email format."
    },
    "registrationDate": {
      "type": "date-time",
      "description": "The date and time when the user registered their account within the system."
    }
  },
  "methods": [
    {
      "name": "updateEmail",
      "description": "Updates the user's email address.",
      "parameters": [
        {
          "name": "newEmail",
          "type": "string",
          "description": "The new email address to be set for the user."
        }
      ],
      "returnType": "boolean",
      "description": "Returns true if the email was successfully updated, false otherwise."
    },
    {
      "name": "changeUsername",
      "description": "Changes the username of the user.",
      "parameters": [
        {
          "name": "newUsername",
          "type": "string",
          "description": "The new username to be set for the user."
        }
      ],
      "returnType": "boolean",
      "description": "Returns true if the username was successfully changed, false otherwise."
    }
  ]
}
```
## FunctionDef compile_transformer(program_spec, config, compile_ffn, verbose)
```json
{
  "module": "data_processing",
  "class": "DataCleaner",
  "description": "The DataCleaner class is designed to handle data cleaning tasks, including removing duplicates, handling missing values, and standardizing data formats. It provides methods for each of these operations, allowing users to specify parameters such as the columns to process or the strategy for filling in missing data.",
  "methods": [
    {
      "name": "__init__",
      "parameters": [],
      "description": "Initializes a new instance of the DataCleaner class."
    },
    {
      "name": "remove_duplicates",
      "parameters": [
        {"name": "columns", "type": "list", "description": "A list of column names to consider when identifying duplicates. If not specified, all columns are considered."}
      ],
      "description": "Removes duplicate rows from the dataset based on the specified columns."
    },
    {
      "name": "handle_missing_values",
      "parameters": [
        {"name": "strategy", "type": "str", "description": "The strategy to use for handling missing values. Options include 'drop', 'fill', or 'interpolate'. Default is 'drop'."},
        {"name": "value", "type": "any", "description": "The value to use when filling in missing data if the strategy is 'fill'. This parameter is ignored for other strategies."}
      ],
      "description": "Handles missing values in the dataset using the specified strategy."
    },
    {
      "name": "standardize_formats",
      "parameters": [
        {"name": "columns", "type": "list", "description": "A list of column names to standardize. If not specified, all columns are considered."},
        {"name": "format", "type": "str", "description": "The format to which the data should be standardized. Options include 'date', 'currency', or 'percentage'. Default is 'date'."}
      ],
      "description": "Standardizes the formats of specified columns in the dataset."
    }
  ]
}
```
