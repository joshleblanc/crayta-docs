---
sidebar_position: 1
---

# Globals

## Functions

| Function Name     | Return Type | Description                                                                                                                                               | Tags          |
|-------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| IsInSchedule()    | boolean     | Returns whether the function is executed inside a schedule or not                                                                                         | None          |
| Wait(number time) | number      | Wait for at least given time interval in seconds then resume execution, and return the exact time taken (which will be the next frame after time seconds) | Schedule-Only |
| Wait()            | number      | Wait for the next frame, then resume execution                                                                                                            |               |

## Examples