# EasingMode

Used in [NPC.PlayTimeline](../entities/npc#PlayTimeline) function calls to set the interpolation between the last and current keys.

## Constants

| Constant Name        | Return Type | Description                                                                      | Tags |
|----------------------|-------------|----------------------------------------------------------------------------------|------|
| EasingMode.Linear    | number      | Interpolate linearly (ie in a straight line) between two points.                 | None |
| EasingMode.EaseInOut | number      | Ease in to and out of the movement, ie move using acceleration and deceleration. | None |
| EasingMode.EaseIn    | number      | Ease in to movement, ie start to move using acceleration and then a hard stop.	  | None |
| EasingMode.EaseOut   | number      | Ease out of the movement. ie start moving instantly but come to a gradual rest.	 | None |
