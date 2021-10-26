# Script

## Functions

| Function Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| GetProperties() | [Properties](properties) | Alternative to self.properties, this gets the bag of values produced from the property editor for this script on this Entity. The properties are defined by the static Properties table on the table returned by the Lua script | None |
| RevertClientProperty(string propertyName) | None | Revert a property that's been changed on the client back to the server's value for it | Client Only |
| GetEntity() | [Entity](entity) | Returns the Entity that the script is attached to | None |
| GetScriptAsset() | [ScriptAsset](script_asset) | Returns the ScriptAsset this is an instance of | None |
| ListenForEvent(string eventName, [Script](script) listenerScriptComponent) | None | Tell this script that listenerScriptComponent wants to be informed when it sounds eventName using SendEventToListeners. eventName will be called on the listenerScriptComponent script | None |
| ListenForEvent(string eventName, [Script](script) listenerScriptComponent, string functionName) | Tell this script that listenerScriptComponent wants to be informed when it sounds eventName using SendEventToListeners. functionName will be called on the listenerScriptComponent script | None |
| SendEventToListeners(string eventName, ...) | None | Call eventName on any scripts that have registered for it using ListenForEvent with the given args. If called on the server do it only on the server, if called on a client do it only on that client | None |
| Schedule(function callback) | [ScheduleHandle](schedule_handle) | Pass this a function to do that function in a thread. Can use globals like Wait to control flow as the function will be re-entrant | None |  
| Cancel([ScheduleHandle](schedule_handle) handle) | None | Cancel a scheduled task if its running | None |
| SetSaveData(table saveData) | None | Set the save data for this script to the table supplied. The script must be owned by a User or Player | Server Only |
| GetSaveData(function callback) | None | Get the save data previously written out with SetSaveData on this script. This function is asynchronous and will call the callback function when its finished with the save data as an argument | Deprecated, Server Only |
| GetSaveData() | table | Get the save data previously written out with SetSaveData on this script. This function returns the save data immediately | Server Only |
| SendToScript(string eventName, ...) | None | Call eventName on this script if it exists, with the given args | None | 
| SendToAllClients(string eventName, ...) | None | Call eventName on this script on all clients currently connected to the server with the given args. Note, this function call can not guarantee that entities are all in a ready state on the client at the time of call, and might therefore miss events during construction | Server Only |
| SendToServer(string eventName, ...) | None | Call eventName on this script on the server | Local Only |
| SendToLocal(string eventName, ...) | None | Call eventName on this script on the client that owns the Player or User this script is attached to | Server Only |


## Entry Points

These methods are called at specific points in a game's lifecycle, if present in a script. 

```lua
-- This method is called when the script is initialized on the server
function ExampleScript:Init()

end
```

| Entry Point Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| OnInteract([Character](character) player, [HitResult](hit_result) hitResult) | None | Called when a player interacts with an entity on all scripts of the entity | Server Only |
| OnCollision([Entity](entity) entity) | None | Called when a player collides with an entity on all scripts of the entity. Also calls this function on the player's scripts with the entity as the argument | Server Only |
| OnDamage(number amount, [Entity](entity) causer, [HitResult](hit_result) hitResult) | None | Called when an entity is damaged on all scripts of the entity | Server Only |
| Init() | None | Called to initialize a script on the server | Server Only |
| ClientInit() | None | Called to initialize a script on the client | Client Only |
| LocalInit() | None | Called to initialize a script on the client that owns this entity | Local Only |
| OnTick(number deltaTime) | None | Called each frame on the server, passed the time in seconds since the last call | Server Only |
| ClientOnTick(number deltaTime) | None | Called each frame on the client, passed the time in seconds since the last call | Client Only |
| LocalOnTick(number deltaTime) | None | Called each frame on the client that owns this script, passed the time in seconds since the last call | Local Only |
| OnUserLogin([User](user) user) | None | Called when a new user joins the game | Server Only |
| OnUserLogout([User](user) user) | None | Called when a user leaves the game | Server Only |
| OnDeathPlaneTrigger() | None | Called on the player when the player is below the death plane | Server Only |
| OnTriggerEnter([Entity](entity) entity) | None | Called by a trigger component when an entity enters the trigger volume | Server Only |
| OnTriggerExit([Entity](entity) entity) | None | Called by a trigger component when an entity leaves the trigger volume | Server Only |
| OnButtonPressed(string buttonName) | None | Called on player and user scripts when a particular button is pressed, giving the string name of the button | Server Only |
| OnButtonReleased(string buttonName) | None | Called on player and user scripts when a particular button is released, giving the string name of the button | Server Only |
| OnIronSightStart() | None | Called when the character goes in to Iron Sight mode | Server Only |
| OnIronSightStop() | None | Called when the character stops Iron Sight mode | Server Only |
| OnSprintStart() | None | Called when the character starts sprinting | Server Only |
| OnSprintStop() | None | Called when the character stops sprinting	 | Server Only |
| OnCrouch() | None | Called when the character crouches | Server Only |
| OnStand() | None | Called when the character stands | Server Only |
| OnJump() | None | Called when the character jumps | Server Only |
| LocalOnButtonPressed(string buttonName) | None | Called locally on player and user scripts when a particular button is pressed, giving the string name of the button | Local Only |
| LocalOnButtonReleased(string buttonName) | None | Called locally on player and user scripts when a particular button is released, giving the string name of the button | Local Only|
| LocalOnIronSightStart() | None | Called when the character goes in to Iron Sight mode	| Local Only |
| LocalOnIronSightStop() | None | Called when the character stops Iron Sight mode | Local Only |
| LocalOnSprintStart() | None | Called when the character starts sprinting	| Local Only | 
| LocalOnSprintStop() | None | Called when the character stops sprinting | Local Only |
| LocalOnCrouch() | None | Called when the character crouches | Local Only |
| LocalOnStand() | None | Called when the character stands from crouch | Local Only |
| LocalOnJump() | None | Called on the player when a jump action happened | Local Only |
| OnHotbarChanged(number hotbarIndex) | None | Called on server when the user's hotbar index changes, either by using the previous and next buttons or using the hotbar keys on a keyboard. Calls function on all user and player scripts | Server Only |
| OnChatMessage([User](user) user, [Text](text) message) | Called when a quick chat message is triggered by a user | Client Only |
| OnDestroy() | None |  Called on the server when an entity is destroyed | Server Only |
| LocalOnMantleStart() | None | Called when the character starts to mantle up to a platform	| Local Only | 
| OnMantleStart() | None | Called when the character starts to mantle up to a platform | Server Only |
| LocalOnMantleStop() | None | Called when the character stops to mantling up to a platform	| Local Only |
| OnMantleStop() | None | Called when the character stops to mantling up to a platform | Server Only |
| LocalOnSlideStart() | None | Called when the character starts to slide | Local Only | 
| OnSlideStart() | None | Called when the character starts to slide | Server Only |
| LocalOnSlideStop() | None | Called when the character stops sliding | Local Only |
| OnSlideStop() | None | Called when the character stops sliding | Server Only |
| LocalOnRollStart() | None | Called when the character starts to roll | Local Only |
| OnRollStart() | None | Called when the character starts to roll | Server Only | 
| LocalOnRollStop() | None | Called when the character stops rolling | Local Only |
| OnRollStop() | None | Called when the character stops rolling | Server Only |
| LocalOnSpawnEffectEnded() | None | Called when the character spawn effect has ended | Local Only |
| OnSpawnEffectEnded() | Called when the character spawn effect has ended | Server Only |
| OnActivityTriggered(string id, [Text](text) display, string category) | None | Called when an activity is triggered | None | 

## Examples