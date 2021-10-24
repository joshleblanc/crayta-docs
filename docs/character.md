# Character

## Functions

| Function Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| Attach([Entity](entity) entityToAttach, string socketName) | None | Deprecated, see [AttachTo](entity#AttachTo) | Deprecated, Server Only |
| GetUser() | [User](user) | Get the User entity which controls this Character	 | None |
| SetAlive(boolean alive) | None | Set the character state to alive or dead | Server Only |
| IsAlive() | boolean | Get whether a Player is alive. Return false for non-Player | None |
| GetLookAtPos() | [Vector](vector) | Get the point the player is looking at, for an action camera this is the same as User:GetCameraLookAtPos but for orbit style cameras it will be in front of the player | Server Only, Local Only |
| GetLookAt() | [Vector](vector), [Vector](vector) | Return two values, the position of the player's virtual "eye" and the position the player is looking at. For an action camera this is the same as User:GetCameraLookAt but for an orbit style camera it will be the player's head position and what is in front of the player | Server Only, Local Only |
| SetInputLocked(boolean inputLocked) | None | Lock player control | Server Only, Local Only |
| SetGrip([GripAsset](grip_asset) gripAsset) | None | Set the current grip animations used by this player. Passing nil is the same as calling SetNoGrip() | None |
| SetNoGrip() | None | 	Reverts the player back to the default 'unarmed' animations. Can also be achieved by calling SetGrip(nil) | None |
| PlayAction(string action, table properties) | None | Play an animation action, with properties specifying how it should be played | None |
| PlayAction(string action) | None | Play an animation action with default properties	 | None |
| HasAction(string action) | boolean | Returns true if the current grip can perform this type of action | None |
| GetActions() | table | Get the name of every available action for the current grip | None |
| GetActionEvents(string action) | table | Get the name of every available event for an action | None |
| HasActionEvent(string action, string event) | boolean | Returns true if this action has an animation event of the specified name | None |
| GetPlayLength(string action) | number | Returns the length of an animation, in seconds, assuming a playbackSpeed of 1 is set | None |
| Launch([Vector](vector) vector) | None | Launch the character	| None |
| GetInteraction() | [Entity](entity), [HitResult](hit_result) | Get whichever Entity you would interact with if you pressed interact | Server Only, Local Only |
| PlayVibrationEffect([VibrationEffectAsset](vibration_effect_asset) effect) | None | Plays the given vibration effect on the player's controller | None |
| PlayManualVibration(number intensity, number duration, boolean affectSmallMotors, boolean affectLargeMotors) | Manually vibrate the player's controller | None |
| AdjustAim(...) | [AdjustAimHandle](adjust_aim_handle) | Programmatically move the user's camera to look at specific points | None |
| CancelAdjustAim([AdjustAimHandle](adjust_aim_handle) handle) | Cancel an aim adjustment | None |
| IsAdjustAimActive() | boolean | Returns whether the player's aim is currently being adjusted | None |

## Properties


| Property Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| speedMultiplier | number | Multiplier on movement speed (default is 1.0)	| Read-Write |
| jumpHeightMultiplier | number | Multiplier on jump height (default is 1.0) | Read-Write |
| canSprint | boolean | Turn on or off ability to sprint | Read-Write |
| canRun | boolean | Turn on or off ability to run	| Read-Write |
| canWalk | boolean | Turn on or off ability to walk	| Read-Write |
| canMantle | boolean | Turn on or off ability to mantle	| Read-Write |
| maxMantleHeight | boolean | Set the maximum height that a player can mantle | Read-Write |
| canSlide | boolean | Turn on or off ability to slide	| Read-Write |
| canRoll | boolean | Turn on or off ability to roll	| Read-Write |
| canRelax | boolean | Turn on or off ability to go into a grip's relaxed pose	 | Read-Write |
| breakFall | boolean | Turn on or off ability to break fall on landing	 | Read-Write |
| breakFallSpeed | boolean | Turn on or off ability to break fall on landing	| Read-Write |
| canJump | boolean | Turn on or off ability to jump	| Read-Write |
| displayDefaultNameTag	| boolean | Turn on or off the default name tag	 | Read-Write |
| displayDefaultQuickChat	| boolean | Turn on or off the default overhead quick chat	| Read-Write |
| canCrouch | boolean | Turn on or off ability to crouch or go prone	 | Read-Write |
| interactionRange | number | Interaction range (from camera in cm)	| Read-Write |
| cameraType	| number | Set the character camera type. 1 = Action, 2 = Orbit	| Read-Write |
| forcedCameraPerspective | number | Set restrictions on the action player camera perspective. 1 = No Restrictions, 2 = 1st Person Only, 3 = 3rd Person Only. (Default is 1) | Read-Write |
| canIronSight | boolean | Will the action camera iron-sight on secondary press	| Read-Write |
| thirdPersonFOV	| number | FOV of the third person action camera	| Read-Write |
| thirdPersonIronSightFOV	| number | FOV of the third person action camera in Iron Sight mode	 | Read-Write |
| firstPersonFOV	| number | FOV of the third person action camera	| Read-Write |

## Examples

### AdjustAim

AdjustAim works in much the same way as timelines. It accepts any number of arguments, where the first argument is speed, the second argument is either a relative rotation, or a vector to look at, and the third parameter is easing. 

Possible easing values are "Linear" (default), "EaseIn", and "EaseInOut".

```lua
function ExampleScript:LookAtStuff(player)
    player:AdjustAim(
        10, Vector.New(100, 100, 100) -- look at point (100, 100, 100) with speed 10,
        100, Rotation.New(360, 0, 0), "EaseOut", -- Rotate 360 degrees with a speed of 100, easing out of the last position
        1000, Vector.New(0,0,0), "EaseIn", -- Look at point (0, 0, 0) with a speed of 1000, easing in as the adjustment finished
    )
end
```