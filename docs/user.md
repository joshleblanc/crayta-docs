# User

## Functions

| Function Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| GetUsername() | [Text](text) | Get the display name of the User | None |
| GetPlayerCardIcon() | string | Get the player avatar URL | None |
| SpawnPlayer([Template](template) playerTemplate) | [Character](character) | Spawn a player Entity for this User using the supplied template asset | Server Only |
| SpawnPlayer([Template](template) playerTemplate, [Locator](locator) locatorEntity) | [Character](character) | Spawn a player Entity for this User using the supplied template asset, at the position and rotation of the locatorEntity | Server Only |
| SpawnPlayer([Template](template) playerTemplate, [Vector](vector) position, [Rotation](rotation) rotation) | [Character](character) | Spawn a player Entity for this User using the supplied template asset, at the given position and rotation | Server Only |
| SpawnPlayerWithEffect([Template](template) playerTemplate, function callback) | [Character](character) | Spawn a player Entity for this User using the supplied template asset and trigger the spawn effect with callback	| Server Only |
| SpawnPlayerWithEffect([Template](template) playerTemplate, [Locator](locator) locatorEntity, function callback) | [Character](character) | Spawn a player Entity for this User using the supplied template asset, at the position of the spawnPoint (which can be any Entity with a 'playerstart' component) and trigger the spawn effect with callback | Server Only |
| SpawnPlayerWithEffect([Template](template) playerTemplate, [Vector](vector) position, [Rotation](rotation) rotation, function callback) | [Character](character) | Spawn a player Entity for this User using the supplied template asset, at the given position and trigger the spawn effect | Server Only |
| SpawnPlayerWithEffect([Template](template) playerTemplate) | [Character](character) | Spawn a player Entity for this User using the supplied template asset and trigger the spawn effect | Server Only |
| SpawnPlayerWithEffect([Template](template) playerTemplate, [Locator](locator) locatorEntitiy) | [Character](character) | Spawn a player Entity for this User using the supplied template asset, at the position of the spawnPoint (which can be any Entity with a 'playerstart' component) and trigger the spawn effect | Server Only |
| SpawnPlayerWithEffect([Template](template) playerTemplate, [Vector](vector) position, [Rotation](rotation) rotation) | [Character](character) | Spawn a player Entity for this User using the supplied template asset, at the given position and trigger the spawn effect	| Server Only |
| DespawnPlayer() | None | Despawn a player	| Server Only | 
| DespawnPlayerWithEffect(function callback) | None | Despawn a player and trigger the despawn effect with callback when it finishes | Server Only |
| DespawnPlayerWithEffect() | None | Despawn a player and trigger the despawn effect | Server Only |
| GetPlayer() | [Character](character) | Get the Entity (if there is one) that has been spawned for the User | None |
| SetCamera([Entity](entity) camera) | None | Set camera view of this User to the given cameraEntity (which can be either a Camera entity or a Character entity) | Server Only |
| SetCamera([Entity](entity) camera, number transitionTime) | None | Set camera view of this User to the given cameraEntity (which can be either a Camera entity or a Character entity). Transitions the camera over a given time from the previous one | Server Only |
| GetCamera() | [Camera](camera) | Get the camera for the user | None |
| GetCameraLookAtPos() | [Vector](vector) | Get the point the camera is looking at | None |
| GetCameraLookAt() | [Vector](vector), [Vector](vector) | Return two values, the position of the camera and a point the camera is facing at (where it collides with the scene) | None |
| LeaveGame() | None | Leave the game | Server Only, Local Only |
| LeaveGame(function callback) | None | Leave the game, calling the callback if leaving fails | Server Only |
| GoToGame(string gameId) | None | Go to game, specified by game id | Server Only |
| GoToGame(string gameId, function callback) | None | go to game, specified by game id, calling callback if travel fails | Server Only |
| GoToWorld([WorldAsset](world_asset) world) | None | Go to world | Server Only |
| GoToWorld([WorldAsset](world_asset) world) | None | Go to world, calling callback if the travel fails | Server Only |
| OpenStore() | None | Open the in-game crayta store | Server Only, Local Only |
| OpenNews() | None | Open the in-game crayta news | Server Only, Local Only |
| OpenGameHelp(string helpPageId) | None | Open the game-specific help menu at the given page | Server Only, Local Only |
| OpenGameHelp() | None | Open the game-specific help menu | Server Only, Local Only |
| OpenGameControls(string controlSchemeId) | None | Open the game-specific game controls, at the specified control scheme | Server Only, Local Only |
| OpenGameControls() | None | Open the game-specific game controls | Server Only, Local Only |
| ShowCursor(boolean showCursor) | None | Turn the cursor on or off	| Deprecated |
| ProjectPositionToScreen([Vector](vector) worldLocation) | [Vector2D](vector_2d) | Converts a position in world space to a screen space co-ordinate Returned on-screen values are in the range 0 to 1 Usage | Local Only |
| ProjectPositionToWidget([Widget](widget) widget, [Vector](vector) worldPosition) | Converts a position in world space to a widget space co-ordinate Returned on-screen values are in the range 0 to 1 | Local Only |
| PlayVibrationEffect([VibrationEffectAsset](vibration_effect_asset) vibrationEffectAsset) | None | Play the specific vibration effect | None |
| PlayManualVibration(number intensity, number duration, boolean affectSmallMotors, boolean affectLargeMotors) | None | Manually play a vibration using the given values | None |
| PlayCameraShakeEffect([CameraShakeAsset](camera_shake_asset) cameraShakeAsset, number scale) | None | Play a camera shake effect on this User with a scale multiplier	| None |
| PlayCameraShakeEffect([CameraShakeAsset](camera_shake_asset) cameraShakeAsset) | None | Play a camera shake effect on this User | None |
| [SetMoveOverride](#SetMoveOverride)([Vector2D](vector_2d) scale, [Vector2D](vector_2d) add) | None | Set a scale on the user's actual move input and an addition 2D vector to add to it. Used for example to auto-walk a player forward but scaling the real input down to zero and adding an additional value | None |
| SetLookOverride([Vector2D](vector_2d) scale, [Vector2D](vector_2d) add) | None | Set a scale on the user's actual look input and an addition 2D vector to add to it. Used for example to auto-look a player at a particular point by scaling the real input down to zero and adding an additional value | None |
| SetLeaderboardValue(string leaderboardId, number value, function callback) | None | Set a value in the given leaderboard with the given value. Call the given callback with the result | Server Only |
| SetLeaderboardValue(string leaderboardId, number value) | None | Set a value in the given leaderboard with the given value | Server Only |
| GetLeaderboardValue(string leaderboardId, function callback) | None | Gets the highest ranking value on the specified leaderboard for this user. Results are returned as parameters to the callback function. Callback function parameters are Score & Rank | Server Only |
| AddToLeaderboardValue(string leaderboardId, number increment, function callback) | None | Add a number to the leaderboard value on the specified leaderboard for this user. Results are returned as parameters to the callback function. Callback function parameter is the new score | None |
| AddToLeaderboardValue(string leaderboardId, number increment) | None | Add a number to the leaderboard value on the specified leaderboard for this user | Server Only |
| GetChallengeProgress(string challengeId) | number | Gets the current progress on an active challenge | None |
| SendChallengeEvent(string eventName, table eventParameters) | None | Please use SendGameEvent instead of this. SendGameEvent trigger Challenges and Activities | Deprecated, Server Only |
| SendChallengeEvent(string eventName) | None | Please use SendGameEvent instead of this. SendGameEvent trigger Challenges and Activities | Deprecated, Server Only |
| SendXPEvent(string eventName, table eventParameterTable) | None | Sends an event for this user that can be used by the Challenges and Activities systems. Takes a lua table of named parameters which are checked against the conditions inside each challenge and activity | Server Only |
| SendXPEvent(string eventName) | None | Sends an event for this user that can be used by the Challenges and Activities systems. This is the same as sending an empty parameter list in the other SendXPEvent overload | Server Only |

## Properties

| Property Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| showDefaultCrosshair | boolean | Show the default crosshair | None |
| useHotbar | boolean | Use hotbar inputs, using the next and previous item buttons on controller and the hotbar buttons on keyboard | None |
| hotbarMax | number | Number of slots in the hotbar, this is a wrap point for next and previous item buttons | None |
| hotbarIndex | number | The current (1-based) hotbar index for this user | None |
| voiceChannel | number | The current voice channel for this user (1 - 32) | None |

## Examples

### SendXPEvent

Here's an example of sending an event called SomeEvent which will progress any matching challenges or trigger any activities and give the player XP. The parameter names are entirely up to you and will be compared against the conditions in the definitions.

```lua
self:GetEntity():GetUser():SendXPEvent("SomeEvent", {someParameter1 = someValue1, someParameter2 = someValue2})
```

### SetMoveOverride

SetMoveOveride lets you do two things:

1. Scale user input on the X and Y axes
2. Add a fixed amount to user input on the X and Y axes

For example, to force the user to move only left and right:

```lua
function UserScript:Init()
  self:GetEntity():SetMoveOverride(Vector.New(1, 0), Vector.Zero)
end
```
