# Rotation

## Constructors

| Constructor Name                                    | Return Type             | Description                                 | Tags |
|-----------------------------------------------------|-------------------------|---------------------------------------------|------|
| Rotation.New(number pitch, number yaw, number roll) | [Rotation](rotation.md) | Constructs a Rotation with the given values | None |
| Rotation.FromVector([Vector](vector.md) vector)     | [Rotation](rotation.md) | Constructs a Rotation from the given Vector | None |

## Class Functions

| Class Function Name                                                                     | Return Type             | Description                     | Tags |
|-----------------------------------------------------------------------------------------|-------------------------|---------------------------------|------|
| Rotation.Lerp([Rotation](rotation.md) rot1, [Rotation](rotation.md) rot2, number alpha) | [Rotation](rotation.md) | Interpolate between 2 rotations | None |

## Functions

| Function Name                              | Return Type             | Description                             | Tags |
|--------------------------------------------|-------------------------|-----------------------------------------|------|
| RotateVector([Vector](vector.md) vector)   | [Vector](vector.md)     | Rotate a given vector by the rotation   | None |
| UnrotateVector([Vector](vector.md) vector) | [Vector](vector.md)     | Unrotate a given vector by the rotation | None |
| Inverse()                                  | [Rotation](rotation.md) | Get the inverse of this rotation        | None |

## Properties

| Property Name | Return Type | Description                  | Tags |
|---------------|-------------|------------------------------|------|
| pitch         | number      |  Pitch component of Rotation | None |
| yaw           | number      | Yaw component of Rotation    | None |
| roll          | number      | Roll component of Rotation   | None |

## Constants

| Constant Name | Return Type             | Description                           | Tags |
|---------------|-------------------------|---------------------------------------|------|
| Rotation.Zero | [Rotation](rotation.md) | Return a Rotation with 0 on each axis | None |

## Overrides

| Override Name | Return Type             | Description                                      | Tags |
|---------------|-------------------------|--------------------------------------------------|------|
| +             | [Rotation](rotation.md) | Add 2 rotations                                  | None |
| -             | [Rotation](rotation.md) | Subtract 2 rotations                             | None |
| *             | [Rotation](rotation.md) | Multiply a rotation by a number                  | None |
| to_string     | string                  | Return the string representation of the Rotation | None |


## Examples