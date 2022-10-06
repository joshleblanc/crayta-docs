# Text

## Class Functions

| Class Function Name                         | Return Type     | Description                                                                                                                                                                                                                                                                                                                          | Tags |
|---------------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Text.Format(string format, ...)             | [Text](text.md) | Same as the normal Text:Format function but uses a Lua string as the format specifier, this is unwise as it means there is no opportunity to localize it but useful for simply combining a localised string with a number for example. (Note: Currently entering localised text into text properties is not supported by the editor) | None |
| Text.FormatTime(string format, number time) | [Text](text.md) | Same as the normal Text:FormatTime function but uses a Lua string as the format specifier. This means the actual time format will not be localisable into client languages. (Note: Currently entering localised text into text properties is not supported by the editor)                                                            | None |

## Functions

| Function Name           | Return Type     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Tags |
|-------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Format(...)             | [Text](text.md) | Format a string using the passed in arguments list (in which case replaces {1} with the first one, {2} with the second, etc) or a table (in which case the string keys are replaced with their values). If run on the client this will localise all the Text values involved to the client language where translations are available, if run on the server it will use the native language of each Text value. (Note: Currently entering localised text into text properties is not supported by the editor) | None |
| FormatTime(number time) | [Text](text.md) | Format a time into a Text value using the following expansions, {hh} - hour component of passed in time, {mm} - minute component of passed in time, {ss} - seconds component of passed in time, {ms} - milisecond component of passed in time. If run on the client the format Text variable will be localized to the client language where translations are available, if run on the server it won't. (Note: Currently entering localised text into text properties is not supported by the editor)         | None |

## Overrides

| Override Name | Return Type | Description                                                                            | Tags |
|---------------|-------------|----------------------------------------------------------------------------------------|------|
| to_string     | string      | Note: tostring() will lose any non-ASCII characters from the local version of the text | None |

## Examples

### Text.Format

```lua
function ExampleScript:FormatStrings()
  Text.Format("Hello, {1}", "Cereal") -- Hello, Cereal
  Text.Format("Hello, {name}", { name = "Cereal" }) -- Hello, Cereal
  Text.Format("Hello, {1}. Welcome to {2}.", "Cereal", "Crayta") -- Hello, Cereal. Welcome to Crayta.
end
```
