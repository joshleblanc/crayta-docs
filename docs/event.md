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