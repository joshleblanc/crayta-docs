# Widget

## Functions

| Function Name                          | Return Type  | Description                                                                                                                                                                                                                  | Tags |
|----------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Show()                                 | None         | Show the widget                                                                                                                                                                                                              | None |
| Hide()                                 | None         | Hide the widget                                                                                                                                                                                                              | None |
| CallFunction(string functionName, ...) | None         | Call the names functioned on the widget                                                                                                                                                                                      | None |
| GetProperties()                        | [Properties] | Alternative to properties, this gets the bag of values produced from the property editor for this script on this Entity. The properties are defined by the static Properties table on the table returned by the Lua script.  | None |

## Properties

| Property Name  | Return Type  | Description                                                    | Tags       |
|----------------|--------------|----------------------------------------------------------------|------------|
| js             | table        | Access the underlying models in the widget                     | Read-Write |
| visible        | boolean      | Set or get the visibility of this widget                       | Read-Write |
| properties     | [Properties] | Get the widget properties                                      | Read-Write |
| requiresCursor | boolean      | Whether or not the widget requires a cursor                    | Read-Write |
| order          | number       | The order the widget should be drawn relative to other widgets | Read-Write |

## Overrides

| Override Name | Return Type | Description     | Tags |
|---------------|-------------|-----------------|------|
| index         | object      | Get widget data | None | 
| new_index     | object      | Set widget data | none |

## Examples

### CallFunction

CallFunction lets you call frontend functions directly from your lua scripts. Doing so requires the function to be registered with the engine.

```js
engine.on("SayHello", name => {
    console.log(`Hello, ${name}!`);
})
```

```lua
function ExampleScript:SayHello()
    self:GetEntity().helloWidget:CallFunction("SayHello", "Jane") -- The client will log "Hello, Jane!"
end
```