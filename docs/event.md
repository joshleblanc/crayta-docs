# Event

## Functions 

| Function Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| Send(...) | None | Send data to all listeners of the event | None |
| Listen([Script](script) script, string functionName) | None | Listen to this event, calling functionName on script when sent | None |   
| HasBindings() | boolean | Return true if this Event is bound to anything, even if its something like "every instance of a script" which would actually resolve to no bindings | None |
| GetAllBindings() | table | Get a table where each element is a table containing a 'script' variable and a 'function' variable, describing each call that is bound by this event | None |

## Overrides

| Override Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| to_string | string |  | None |

## Examples

### Send

Sends an event to all listeners of the specific event with any arguments passed into `Send`.

```lua
ExampleScript.Properties = {
    {
        name = "OnExampleEvent",
        type = "event",
        tooltip = "Example event to fire",
    },
}

function ExampleScript:Send()
    self.properties.OnExampleEvent:Send(self:GetEntity()) -- will send the entity this script is on to all scripts that are listening on this event
end
```

### Listen

Tells the script passed into the function call to listen for the event to be fired handling it with the passed in function

```lua
function ExampleScript:Listen(event)
    event:Listen(self, "OnExampleEventHandler") -- will call "OnExampleEventHandler" on this script when the passed in event is fired
end

-- function that will be called when the event passed into "ExampleScript:Listen" is fired
function ExampleScript:OnExampleEventHandler(entity)
    print("I hear you!")
end
```
