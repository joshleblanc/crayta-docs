# Rotation

## Constructors

| Constructor Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| Rotation.New(number pitch, number yaw, number roll) | [Rotation](rotation) | Constructs a Rotation with the given values | None |
| Rotation.FromVector([Vector](vector) vector) | [Rotation](rotation) | Constructs a Rotation from the given Vector | None |

## Class Functions

| Class Function Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| Rotation.Lerp([Rotation](rotation) rot1, [Rotation](rotation) rot2, number alpha) | [Rotation](rotation) | Interpolate between 2 rotations | None |

## Functions

| Function Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| RotateVector([Vector](vector) vector) | [Vector](vector) | Rotate a given vector by the rotation | None |
| UnrotateVector([Vector](vector) vector) | [Vector](vector) | Unrotate a given vector by the rotation | None |
| Inverse() | [Rotation](rotation) | Get the inverse of this rotation | None |

## Properties

| Property Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| pitch | number | 	Pitch component of Rotation | None |
| yaw | number | Yaw component of Rotation | None |
| roll | number | Roll component of Rotation | None |

## Constants

| Constant Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| Rotation.Zero | [Rotation](rotation) | Return a Rotation with 0 on each axis | None |

## Overrides

| Override Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| + | [Rotation](rotation) | Add 2 rotations | None |
| - | [Rotation](rotation) | Subtract 2 rotations | None |
| * | [Rotation](rotation) | Multiply a rotation by a number | None |
| to_string | string | Return the string representation of the Rotation | None |


## Examples