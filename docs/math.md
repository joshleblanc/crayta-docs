# math

## Class Functions

| Class Function Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| math.lerp(number a, number b, number t) | number | The interpolated float result between the two float values | None |
| math.sign(number a)| number | Returns 1 if value is position, -1 if value is negative | None |
| math.copysign(number a, number b) | number |Copies the sign from b onto a | None |  
| math.clamp(number a, number min, number max) | number | Clamps the given value between the given minimum float and maximum float values. Returns the given value if it is within the min and max range | None |

## Examples

### lerp

Linearly interpolates between a and b by t.

The parameter t is **not** clamped to the range [0, 1] and is effectively the same as `a + (b - a) * t`

When t = 0 returns a.
When t = 1 return b.
When t = 0.5 returns the midpoint of a and b.

```lua
function ExampleScript:Lerp()
    local a = 0
    local b = 100

    print(math.lerp(a, b, -0.5)) -- prints -50
    print(math.lerp(a, b, 0)) -- prints 0
    print(math.lerp(a, b, 0.5)) -- prints 50
    print(math.lerp(a, b, 1)) -- prints 100
    print(math.lerp(a, b, 1.5)) -- prints 150
end
```

### sign

```lua
function ExampleScript:Sign()
    local a = 100
    local b = -25
    print(math.sign(a)) -- prints 1
    print(math.sign(b)) -- prints -1
end
```

### copysign

```lua
function ExampleScript:CopySign()
    local a = 100
    local b = -25
    local c = math.copysign(a, b)
    print(c) -- prints -100
end
```

### clamp

```lua
function ExampleScript:Heal(amt)
    self.health = self.health + amt
    self.health = math.clamp(self.health, 1, 100) -- Ensure we stay within 1 and 100 health
end
```
