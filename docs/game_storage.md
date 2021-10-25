# GameStorage

## Class Functions

| Class Function Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| GameStorage.GetCounter(string counterName, function callback) | None | Get the value of a global counter for this game. Global counters are shared between all servers running the game and saved between sessions. The value is returned by calling the callback function with the value as an argument. Global counters are always whole (integer) numbers | Server Only |
| GameStorage.UpdateCounter(string counterName, number increment, function callback) | None | Update the value of a global counter for this game by adding increment to the existing value. Global counters are shared between all servers running the game and saved between sessions. The new incremented value is returned by calling the callback function with the value as an argument. Global counters are always whole (integer) numbers | Server Only | 
| GameStorage.UpdateCounter(string counterName, number increment) | None | Update the value of a global counter for this game by adding increment to the existing value. Global counters are shared between all servers running the game and saved between sessions. Global counters are always whole (integer) numbers | Server Only |

## Examples