# Template

## Class Functions

| Class Function Name        | Return Type          | Description                                                                                         | Tags |
|----------------------------|----------------------|-----------------------------------------------------------------------------------------------------|------|
| Template.Find(string name) | [Template](template) | Find a Template in the world by name. Returns nil if not found. Alternative to World:FindTemplate() | None |

## Functions

| Function Name                                                    | Return Type              | Description                                                     | Tags |
|------------------------------------------------------------------|--------------------------|-----------------------------------------------------------------|------|
| FindScriptProperty(string propertyName)                          | object                   | Find a property by property name on any script on this template | None |
| FindScriptProperties(string scriptName)                          | [Properties](properties) | Find all properties for script by name                          | None |
| FindScriptProperties([ScriptAsset](script_asset) scriptAsset)    | [Properties](properties) | Find all properties for script by script asset                  | None |
| FindAllScriptProperties(string scriptName)                       | table                    | Find all script properties for a script by name                 | None |
| FindAllScriptProperties([ScriptAsset](script_asset) scriptAsset) | table                    | Find all script properties for a script asset                   | None |
| FindWidgetProperty(string propertyName)                          | table                    | Get the value of a widget property on this template             | None |
| FindWidgetProperties(string widgetName)                          | table                    | None                                                            | None |
| FindWidgetProperties([WidgetAsset] widgetAsset)                  | table                    | None                                                            | None |
| FindAllWidgetProperties(string widgetName)                       | table                    | None                                                            | None |
| FindAllWidgetProperties([WidgetAsset] widgetAsset)               | table                    | None                                                            | None |

## Examples
