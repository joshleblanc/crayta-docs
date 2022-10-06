# Shape

An [Entity](entity.md) can have a single physical representation. Shape derives from Entity so if you have a Shape you can do any of these functions as well as the functions in Entity. You can do entity:IsA(Shape) to see if a particular entity variable is a Shape type entity.

## Functions

| Function Name                                             | Return Type | Description                                                                      | Tags |
|-----------------------------------------------------------|-------------|----------------------------------------------------------------------------------|------|
| AddImpulse([Vector](../types/vector) impulse)             | None        | Add impulse. An integral of force over a time interval. Newton Seconds           | None |
| AddAngularImpulse([Rotation](../types/rotation) rotation) | None        | Add Angular Impulse. An integral of torque over a time interval. Newton seconds. | None |

## Properties

| Property Name    | Return Type                               | Description                                                                                                                                                                                                                                                | Tags       |
|------------------|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| shape            | [ShapeAsset](../assets/shape_asset) shape | Get/set the shape asset used by this entity                                                                                                                                                                                                                | Read-Write |
| color            | [Color](../types/color) color             | Get/Set the color tint of the shape                                                                                                                                                                                                                        | Read-Write |
| shapeScale       | [Vector](../types/vector) scale           | Get or change the scale                                                                                                                                                                                                                                    | Read-Write |
| collisionEnabled | boolean                                   | Turn on or off collision (ie calling entry point OnCollision).                                                                                                                                                                                             | Read-Write |
| onCollision      | [Event](../types/event) event             | Called when this entity is collided with by a player Character with the Character passed as an argument, as well as the mesh Entity from which the onCollision event was triggered. An alternative to listening for OnCollision in a script on the entity. | Read       |
| physicsEnabled   | boolean                                   | Turn on or off physics.                                                                                                                                                                                                                                    | Read-Write |
| gravityEnabled   | boolean                                   | Turn on or off gravity.                                                                                                                                                                                                                                    | Read-Write |
