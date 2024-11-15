## FunctionDef get_program(program_name, dynamic_halting)
**Documentation for Target Object**

The `Target` class is designed to represent a specific target within a system. It includes properties and methods that facilitate its management and interaction with other components of the system.

### Properties

- **Id**: Represents the unique identifier of the target. This property is read-only.
  - Type: `int`
  
- **Name**: The name assigned to the target, which can be used for identification purposes.
  - Type: `string`

- **IsActive**: Indicates whether the target is currently active or not.
  - Type: `bool`

### Methods

- **Activate()**: Sets the `IsActive` property to true, marking the target as active.
  - Parameters: None
  - Returns: Nothing
  
- **Deactivate()**: Sets the `IsActive` property to false, marking the target as inactive.
  - Parameters: None
  - Returns: Nothing

### Example Usage

```csharp
// Create a new instance of Target with Id = 1 and Name = "SampleTarget"
var target = new Target(1, "SampleTarget");

// Activate the target
target.Activate();

// Check if the target is active
bool isActive = target.IsActive; // Returns true

// Deactivate the target
target.Deactivate();

// Check again if the target is active
isActive = target.IsActive; // Returns false
```

This documentation provides a clear understanding of the `Target` class, including its properties and methods, which are essential for managing targets within the system.
