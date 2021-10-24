# Entity

## Class Functions

| Class Function Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| Entity.IsValid([Entity](entity) entity) | boolean | Returns true if the parameter passed to it is a valid entity	| None |

## Functions

| Function Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| IsA(table derivedType) | boolean | Returns true if the entity is the type passed | None |
| GetName() | string | Get the name of this entity | None |
| GetWorld() | [World](world) | Get the World from an entity | Deprecated |
| RevertClientProperty(string propertyName) | None | Revert a property that's been changed on the client back to the server's value for it | Client Only |
| SetPosition([Vector](vector) position) | None | Set the position of this Entity in 3D space | None |
| AlterPosition([Vector](vector) position, number time) | number | Move from current to position over time | None |
| AlterPosition([Vector](vector) fromPosition [Vector](vector) toPosition, number time) | number | Move from fromPosition to toPosition over time | None |
| GetPosition() | [Vector](vector) | Get the position of this Entity | None |
| SetRotation([Rotation](rotation) rotation) | None | 	Set the rotation of this Entity | None |
| AlterRotation([Rotation](rotation) rotation, number time) | number | Rotate from current to rotation over time | None | 
| AlterRotation([Rotation](rotation) fromRotation, [Rotation](rotation) toRotation, number time) | number | Rotate from fromRotation to toRotation over time | None |
| GetRotation() | [Rotation](rotation) | Get the rotation of this Entity | None |
| SetRelativePosition([Vector](vector) position) | None | Set the position of this Entity relative to whatever this entity is parented to | None |
| AlterRelativePosition([Vector](vector) position, number time) | number | Move from current to position over time relative to whatever this entity is parented to | None |
| AlterRelativePosition([Vector](vector) fromPosition, [Vector](vector) toPosition, number time) | number | Move from fromPosition to toPosition over time relative to whatever this entity is parented to | None |
| GetRelativePosition() | [Vector](vector) | Get the position of this Entity relative to whatever this entity is parented to | None |
| SetRelativeRotation([Rotation](rotation) rotation) | None | Set the rotation of this Entity relative to whatever this entity is parented to | None |
| AlterRelativeRotation([Rotation](rotation) rotation, number time) | number | Rotate from current to rotation over time relative to whatever this entity is parented to | None |
| AlterRelativeRotation([Rotation](rotation) fromRotation, [Rotation](rotation) toRotation, number time) | number | Rotate from fromRotation to toRotation over time relative to whatever this entity is parented to | None |
| GetRelativeRotation() | [Rotation](rotation) | Get the rotation of this Entity relative to whatever this entity is parented to | None |
| GetForward() | [Vector](vector) | Get the forward facing vector of an Entity from its rotation | None |
| GetRight() | [Vector](vector) | Get the right facing vector of an Entity from its rotation | None |
| GetUp() | [Vector](vector) | Get the up facing vector of an Entity from its rotation | None |
| SetForward([Vector](vector) forward) | None | Set the rotation of an Entity to make its front face in a given direction | None |
| SetForward([Vector](vector) forward, [Vector](vector) up) | None | Set the rotation of an Entity to make its front face in a given direction, and its top point in another | None |
| PlaySound([SoundAsset](sound_asset) sound) | [SoundHandle](sound_handle) | Play a sound Asset on this Entity, returning a Handle which can be used to stop the sound | None |
| PlaySound([SoundAsset](sound_asset) sound, number fadeIn) | [SoundHandle](sound_handle) | Play a sound Asset on this Entity, returning a Handle which can be used to stop the sound. Fades in over the given fadeIn time | None |


## Properties

| Property Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|

## Examples

### AttachTo

Available sockets:

```
spine_01
spine_02
spine_03
spine_04
spine_05
neck_01
neck_02
head
clavicle_l
shoulder_l
upperarm_l
lowerarm_l
hand_l
weapon_l
clavicle_r
shoulder_r
upperarm_r
lowerarm_r
hand_r
weapon_r
thigh_l
calf_l
foot_l
thigh_r
calf_r
foot_r
```