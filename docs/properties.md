# Properties

## Overrides

| Override Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| new_index | object | Set a named property to a new value | None |
| index | object | Get the value of a property | None |

## Examples

This class refers to the `properties` object available on scripts.

```lua
MyScript.Properties = {
    { name = "example", type = "number", default = 1 }
}

function MyScript:Init() 
    self.properties.name -- this would be getting the name index on the properties
    self.properties.foobar = 2 -- this would be setting a new_index on the properties
end
```

