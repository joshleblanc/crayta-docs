# Vector2D

## Constructors

| Constructor Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| Vector2D.New(number x, number y, number z) | [Vector2D](vector_2d) | Construct a new Vector2D with the given x, y and z components, where z is generally up | None |

## Class Functions

| Class Function Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| Vector2D.Distance([Vector2D](vector_2d) vec1, [Vector2D](vector_2d) vec2) | number | Return the distance between two Vector2D values | None |
| Vector2D.SquaredDistance([Vector2D](vector_2d) vec1, [Vector2D](vector_2d) vec2) | number | Return the square of the distance of two Vector2D values | None |
| Vector2D.Cross([Vector2D](vector_2d) vec1, [Vector2D](vector_2d) vec2) | [Vector2D](vector_2d) | Return the cross product of two Vector2D values | None |
| Vector2D.Dot([Vector2D](vector_2d) vec1, [Vector2D](vector_2d) vec2) | number | Return the dot product of two Vector2D values | None |
| Vector2D.Lerp([Vector2D](vector_2d) vec1, [Vector2D](vector_2d) vec2) | [Vector2D](vector_2d) | Linearly interpolate between vec1 and vec2 by the fraction alpha, where alpha is normally in the range [0,1] | None |

## Functions

| Function Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| Normalize() | [Vector2D](vector_2d) | Return a normalized Vector2D (where the length is 1.0) | None |
| Length() | number | Return the length of the given Vector2D | None |
| SquaredLength() | number | Return the square of the length of the given Vector2D | None |
| Abs() | [Vector2D](vector_2d) | Return a Vector2D constructed from the absolute (ie positive or zero) x, y and z components of the given Vector2D | None |
| Ceil() | [Vector2D](vector_2d) | Returns a Vector2D constructed from the ceiling (ie next integer value) x, y and z components of the given Vector2D | None |
| Floor() | [Vector2D](vector_2d) | Returns a Vector2D constructed from the floor (ie integer value below) x, y and z components of the given Vector2D | None |

## Properties

| Property Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| x | number | X component of 2D Vector	| None |
| y | number | Y component of 2D Vector | None |
| z | number | Z component of 2D Vector | None |

## Constants

| Constant Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| Zero | [Vector2D](vector_2d) | Zero Vector2D (0, 0) | None |

## Overrides 

| Override Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| + | [Vector2D](vector_2d) | Add two Vector2D values together and return a new Vector2D of the result | None |
| - | [Vector2D](vector_2d) | Subtract two Vector2D values and return a new Vector2D of the result | None |
| unary_minus | [Vector2D](vector_2d) | Negate a Vector2D value and return the result | None |
| * | [Vector2D](vector_2d) | Multiply a Vector2D by a number, returning a Vector2D | None |
| / | [Vector2D](vector_2d) | Divide a Vector2D by a number, returning a Vector2D | None |
| to_string | string | Convert to a string | None |

## Examples