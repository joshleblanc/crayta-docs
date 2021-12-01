# Trigger

## Functions

| Function Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| IsOverlapping([Entity](entity) entity) | boolean | Returns whether a passed in entity is currently within the trigger	| None |
| IsInside([Vector](vector) position) | boolean | Returns whether the point given (world space) is within the bounds of the trigger (whether the trigger is active or not) | None |

## Properties

| Property Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| playersOnly | boolean | Set whether the trigger should only overlap players or all entities | Read-Write |
| size | [Vector](vector) | The size of the trigger box	| Read-Write |
| active | boolean | The trigger box is active | Read-Write |
| interactable | boolean | The trigger box is interactable | Read-Write |
| onTriggerEnter | [Event](event) | Called when this trigger volume is entered by a valid entity, with the Entity passed as an argument, as well as the trigger Entity from which the onTriggerEnter event is sent. An alternative to listening for OnTriggerEnter in a script on the entity | Read |
| onTriggerExit | [Event](event) | Called when this trigger volume is exited by a valid entity, with the Entity passed as an argument, as well as the trigger Entity from which the onTriggerExit event is sent. An alternative to listening for OnTriggerExit in a script on the entity | Read |
 
## Examples