# Vector

## Constructors

| Constructor Name                         | Return Type         | Description                                                                          | Tags |
|------------------------------------------|---------------------|--------------------------------------------------------------------------------------|------|
| Vector.New(number x, number y, number z) | [Vector](vector.md) | Construct a new Vector with the given x, y and z components, where z is generally up | None |

## Class Functions

| Class Function Name                                                        | Return Type         | Description                                                                                                  | Tags |
|----------------------------------------------------------------------------|---------------------|--------------------------------------------------------------------------------------------------------------|------|
| Vector.Distance([Vector](vector.md) vec1, [Vector](vector.md) vec2)        | number              | Return the distance between two Vector values                                                                | None |
| Vector.SquaredDistance([Vector](vector.md) vec1, [Vector](vector.md) vec2) | number              | Return the square of the distance of two Vector values                                                       | None |
| Vector.Cross([Vector](vector.md) vec1, [Vector](vector.md) vec2)           | [Vector](vector.md) | Return the cross product of two Vector values                                                                | None |
| Vector.Dot([Vector](vector.md) vec1, [Vector](vector.md) vec2)             | number              | Return the dot product of two Vector values                                                                  | None |
| Vector.Lerp([Vector](vector.md) vec1, [Vector](vector.md) vec2)            | [Vector](vector.md) | Linearly interpolate between vec1 and vec2 by the fraction alpha, where alpha is normally in the range [0,1] | None |

## Functions

| Function Name   | Return Type         | Description                                                                                                     | Tags |
|-----------------|---------------------|-----------------------------------------------------------------------------------------------------------------|------|
| Normalize()     | [Vector](vector.md) | Return a normalized Vector (where the length is 1.0)                                                            | None |
| Length()        | number              | Return the length of the given Vector                                                                           | None |
| SquaredLength() | number              | Return the square of the length of the given Vector                                                             | None |
| Abs()           | [Vector](vector.md) | Return a Vector constructed from the absolute (ie positive or zero) x, y and z components of the given Vector   | None |
| Ceil()          | [Vector](vector.md) | Returns a Vector constructed from the ceiling (ie next integer value) x, y and z components of the given Vector | None |
| Floor()         | [Vector](vector.md) | Returns a Vector constructed from the floor (ie integer value below) x, y and z components of the given Vector  | None |

## Properties

| Property Name | Return Type | Description               | Tags |
|---------------|-------------|---------------------------|------|
| x             | number      | X component of 3D vector	 | None |
| y             | number      | Y component of 3D vector  | None |
| z             | number      | Z component of 3D vector  | None |

## Constants

| Constant Name | Return Type      | Description           | Tags |
|---------------|------------------|-----------------------|------|
| Zero          | [Vector](vector.md) | Zero vector (0, 0, 0) | None |

## Overrides 

| Override Name | Return Type      | Description                                                          | Tags |
|---------------|------------------|----------------------------------------------------------------------|------|
| +             | [Vector](vector.md) | Add two Vector values together and return a new Vector of the result | None |
| -             | [Vector](vector.md) | Subtract two Vector values and return a new Vector of the result     | None |
| unary_minus   | [Vector](vector.md) | Negate a Vector value and return the result                          | None |
| *             | [Vector](vector.md) | Multiply a Vector by a number, returning a Vector                    | None |
| /             | [Vector](vector.md) | Divide a Vector by a number, returning a Vector                      | None |
| to_string     | string           | Convert to a string                                                  | None |

## Examples