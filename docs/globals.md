# Globals

## Functions

| Function Name     | Return Type | Description                                                                                                                                               | Tags          |
|-------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| IsInSchedule()    | boolean     | Returns whether the function is executed inside a schedule or not                                                                                         | None          |
| Wait(number time) | number      | Wait for at least given time interval in seconds then resume execution, and return the exact time taken (which will be the next frame after time seconds) | Schedule-Only |
| Wait()            | number      | Wait for the next frame, then resume execution                                                                                                            |               |
| print(...)                       | None    | Standard print function (same as Print), takes a comma separated list of arguments and prints out their string representation.       | None |
| Print(...)                       | None    | Standard print function (same as print), takes a comma separated list of arguments and prints out their string representation.       | None |
| printf(...)                      | None    | This print function replaces instances of {1} in format with the first argument passed in, {2} with the second etc (same as Printf). | None |
| Printf(...)                      | None    | This print function replaces instances of {1} in format with the first argument passed in, {2} with the second etc (same as printf). | None |
| FormatString(string format, ...) | string  | Format a string using either {1}, {2} as in Printf, etc or using named variables.                                                    | None |
| GetWorld()                       | [World](World)   | Get the World object                                                                                                                 | None |
| IsClient()                       | boolean | Return true if this script is running on the client                                                                                  | None |
| IsServer()                       | boolean | Return true if this script is running on the server                                                                                  | None |

## Examples

### IsInSchedule

```lua
function ExampleScript:PerformSchedule()
    self:Schedule(function() 
        print(IsInSchedule()) -- prints true
    end)
    print(IsInSchedule()) -- prints false
end
```

### Wait

```lua
function ExampleScript:PerformSchedule()
    self:Schedule(function()
        local dt = Wait() -- waits a single frame
        print(dt) -- Prints the number of seconds since the last frame
    end)
end
```
```lua
function ExampleScript:PerformSchedule()
    self:Schedule(function()
        local dt = Wait(10) -- waits 10 seconds
        print(dt) -- Prints the number of seconds since the last frame
    end)
end
```

### print
```lua
function ExampleScript:Print()
    Print("Hello, world!")
end
```

### Print

see: [print](#print)

### printf

```lua
function ExampleScript:Printf()
    printf("Hello, {1}", "AJ") -- prints "Hello, AJ"
end
```

### Printf

see: [printf](#printf)

### FormatString

```lua
function ExampleScript:FormatString()
    local formattedString = FormatString("Hello, {1}", "AJ")
    print(formattedString) -- prints "Hello, AJ"
end
```

### GetWorld

Gets the currently loaded [World](World)

```lua
function ExampleScript:GetWorld()
    local world = GetWorld()
    print(world.dayLenght) -- Prints the length of the world's day 
end
```

### IsClient

```lua
function ExampleScript:Init()
    print(IsClient()) -- Returns false, since Init is run on the server
end

function ExampleScript:LocalInit()
    print(IsClient()) -- Returns true, since LocalInit is run on a client
end

function ExampleScript:ClientInit()
    print(IsClient()) -- Returns true, since ClientInit is run on all clients
end
```

### IsServer

```lua
function ExampleScript:Init()
    print(IsServer()) -- Returns true, since Init is run on the server
end

function ExampleScript:LocalInit()
    print(IsServer()) -- Returns false, since LocalInit is run on a client
end

function ExampleScript:ClientInit()
    print(IsServer()) -- Returns false, since ClientInit is run on all clients
end
```


