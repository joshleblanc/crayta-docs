# Entity

## Class Functions

| Class Function Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| Entity.IsValid([Entity](entity) entity) | boolean | Returns true if the parameter passed to it is a valid entity	| None |

## Functions

| Function Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| IsA(table derivedType) | boolean | Returns true if the entity is the type passed | None |
| GetName() | string | Get the name of this entity | None |
| GetWorld() | [World](world) | Get the World from an entity | Deprecated |
| RevertClientProperty(string propertyName) | None | Revert a property that's been changed on the client back to the server's value for it | Client Only |
| SetPosition([Vector](vector) position) | None | Set the position of this Entity in 3D space | None |
| AlterPosition([Vector](vector) position, number time) | number | Move from current to position over time | None |
| AlterPosition([Vector](vector) fromPosition [Vector](vector) toPosition, number time) | number | Move from fromPosition to toPosition over time | None |
| GetPosition() | [Vector](vector) | Get the position of this Entity | None |
| SetRotation([Rotation](rotation) rotation) | None | 	Set the rotation of this Entity | None |
| AlterRotation([Rotation](rotation) rotation, number time) | number | Rotate from current to rotation over time | None | 
| AlterRotation([Rotation](rotation) fromRotation, [Rotation](rotation) toRotation, number time) | number | Rotate from fromRotation to toRotation over time | None |
| GetRotation() | [Rotation](rotation) | Get the rotation of this Entity | None |
| SetRelativePosition([Vector](vector) position) | None | Set the position of this Entity relative to whatever this entity is parented to | None |
| AlterRelativePosition([Vector](vector) position, number time) | number | Move from current to position over time relative to whatever this entity is parented to | None |
| AlterRelativePosition([Vector](vector) fromPosition, [Vector](vector) toPosition, number time) | number | Move from fromPosition to toPosition over time relative to whatever this entity is parented to | None |
| GetRelativePosition() | [Vector](vector) | Get the position of this Entity relative to whatever this entity is parented to | None |
| SetRelativeRotation([Rotation](rotation) rotation) | None | Set the rotation of this Entity relative to whatever this entity is parented to | None |
| AlterRelativeRotation([Rotation](rotation) rotation, number time) | number | Rotate from current to rotation over time relative to whatever this entity is parented to | None |
| AlterRelativeRotation([Rotation](rotation) fromRotation, [Rotation](rotation) toRotation, number time) | number | Rotate from fromRotation to toRotation over time relative to whatever this entity is parented to | None |
| GetRelativeRotation() | [Rotation](rotation) | Get the rotation of this Entity relative to whatever this entity is parented to | None |
| GetForward() | [Vector](vector) | Get the forward facing vector of an Entity from its rotation | None |
| GetRight() | [Vector](vector) | Get the right facing vector of an Entity from its rotation | None |
| GetUp() | [Vector](vector) | Get the up facing vector of an Entity from its rotation | None |
| SetForward([Vector](vector) forward) | None | Set the rotation of an Entity to make its front face in a given direction | None |
| SetForward([Vector](vector) forward, [Vector](vector) up) | None | Set the rotation of an Entity to make its front face in a given direction, and its top point in another | None |
| PlaySound([SoundAsset](sound_asset) sound) | [SoundHandle](sound_handle) | Play a sound Asset on this Entity, returning a Handle which can be used to stop the sound | None |
| PlaySound([SoundAsset](sound_asset) sound, number fadeIn) | [SoundHandle](sound_handle) | Play a sound Asset on this Entity, returning a Handle which can be used to stop the sound. Fades in over the given fadeIn time | None |
| PlaySound([SoundAsset](sound_asset) sound, number fadeIn, string group) | [SoundHandle](sound_handle) | Play a sound Asset on this Entity, returning a Handle which can be used to stop the sound. Fades in over the given fadeIn time. Fades out any sound already playing in the GroupName with the given fadeIn time | None |
| PlaySound2D([SoundAsset](sound_asset) sound) | [SoundHandle](sound_handle) | Play a sound Asset on this Entity but without a 3D transform on the sound (useful for UI sounds, stereo music stings, etc) | None |
| PlaySound2D([SoundAsset](sound_asset) sound, number fadeIn) | [SoundHandle](sound_handle) | Play a sound Asset on this Entity but without a 3D transform on the sound (useful for UI sounds, stereo music stings, etc). Fades in over the given fadeIn time | None |
| PlaySound2D([SoundAsset](sound_asset) sound, number fadeIn, string group) | [SoundHandle](sound_handle) | Play a sound Asset on this Entity but without a 3D transform on the sound (useful for UI sounds, stereo music stings, etc). Fades in over the given fadeIn time. Fades out any sound already playing in the GroupName with the given fadeIn time | None |
| PlaySoundAtLocation([Vector](vector) location, [SoundAsset](sound_asset) sound) | [SoundHandle](sound_handle) | Play a sound Asset on this Entity at the given location | None |
| PlaySoundAtLocation([Vector](vector) location, [SoundAsset](sound_asset) sound, number fadeIn) | [SoundHandle](sound_handle) | Play a sound Asset on this Entity at the given location. Fades in over the given fadeIn time | None |
| PlaySoundAtLocation([Vector](vector) location, [SoundAsset](sound_asset) sound, number fadeIn, string group) | [SoundHandle](sound_handle) | Play a sound Asset on this Entity at the given location. Fades in over the given fadeIn time. Fades out any sound already playing in the GroupName with the given fadeIn time | None |
| StopSound([SoundHandle](sound_handle) handle) | None | Given a sound Handle stop the sound on this Entity | None |
| StopSound([SoundHandle](sound_handle) handle, number fadeOut) | None | Given a sound Handle stop the sound on this Entity. Fade the sound out over the given fadeOut time | None | 
| PlayEffect([EffectAsset](effect_asset) effect) | [EffectHandle](effect_handle) | Play a particle effect Asset on this Entity, returning a Handle which can be used to stop the effect | None |
| PlayEffect([EffectAsset](effect_asset) effect, boolean attached) | [EffectHandle](effect_handle) | Play a particle effect Asset on this Entity, returning a Handle which can be used to stop the effect. Optionally the effect is attached to the entity and so all spawned particles are relative to it | None |
| PlayEffectAtLocation([Vector](vector) location, [EffectAsset](effect_asset) effect) | [EffectHandle](effect_handle) | Play a particle effect Asset at a given world location and rotation, returning a Handle which can be used to stop the effect | None |
| PlayEffectAtLocation([Vector](vector) location, [EffectAsset](effect_asset) effect, boolean attached) | [EffectHandle](effect_handle) | Play a particle effect Asset at a given world location and rotation, returning a Handle which can be used to stop the effect. Optionally the effect is attached to the entity and so all spawned particles are relative to it | None | 
| StopEffect([EffectHandle](effect_handle) handle) | None | Stop the effect represented by the given handle | None |
| Clone() | [Entity](entity) | Clone the Entity returning the clone | Server Only |
| AttachTo([Entity](entity) entity) | None | Attach this Entity to another Entity | Server Only |
| AttachTo([Character](character) character, string socket) | None | Attach this Entity to a Character entity, using the named socket | None |
| Detach() | None | Detach this entity from its parent | None |
| ApplyDamage(number damageAmount, [HitResult](hit_result) hitResult, [Vector](vector) shootDirection, [Entity](entity) fromEntity) | None | Apply damageAmount damage to the Entity (by calling OnDamage on it on any scripts that override that), also pass a HitResult from a World Raycast function and a shootDirection Vector and fromEntity which will be passed to the OnDamage function | None |
| ApplyDamage(number damageAmount, [HitResult](hit_result) hitResult, [Vector](vector) shootDirection, [Entity](entity) fromEntity, table damageModifiers) | None | Apply damageAmount damage to the Entity (by calling OnDamage on it on any scripts that override that), also pass a HitResult from a World Raycast function and a shootDirection Vector and fromEntity which will be passed to the OnDamage function | None |
| ApplyDamage(number damageAmount, [Vector](vector) shootDirection, [Entity](entity) fromEntity) | None | Apply damageAmount damage to the Entity (by calling OnDamage on it on any scripts that override that), also pass a shootDirection Vector and fromEntity which will be passed to the OnDamage function | None |
| ApplyDamage(number damageAmount, [Vector](vector) shootDirection, [Entity](entity) fromEntity, table damageModifiers) | None | Apply damageAmount damage to the Entity (by calling OnDamage on it on any scripts that override that), also pass a shootDirection Vector and fromEntity which will be passed to the OnDamage function | None |
| GetParent() | [Entity](entity) | Get a parent Entity that this Entity is attached to either within the world tree or using the Attach function | None |
| GetChildren() | table | Get all children directly below this. The order of children is not guaranteed, and may change randomly | None |
| Destroy() | None | Destroy an Entity. Use with care as any variables referencing that Entity will now be invalid | Server Only |
| SendToScripts(string eventName, ...) | None | Call eventName function with the given args on all scripts that have it as a function. If called on the server do it only on the server, if called on a client do it only on that client | None |
| SendToAllClients(string eventName, ...) | None | Call eventName on all scripts of this Entity on all clients connected to the server with the given args | Server Only |
| SendToServer(string eventName, ...) | None | Call eventName on all script of this Entity on the server | Local Only |
| SendToLocal(string eventName, ...) | None | Call eventName on all scripts of this Entity on the client that owns the Player or User this script is attached to | Server Only |
| IsLocal() | boolean | See if this Entity is owned by the local client | Local Only |
| IsClient() | boolean | Check if this Entity is on the client | Deprecated |
| FindScript(string scriptName) | [Script](script) | This is alternative to entity.scriptName which is the preferred way of getting a script | None |
| FindScript(string scriptName, boolean recursive) | This is alternative to entity.scriptName which is the preferred way of getting a script. This can be recursive to find the script on any child entities | None | 
| FindScript([ScriptAsset](script_asset) scriptAsset) | [Script](script) | Find a script by its script asset | None |
| FindScript([ScriptAsset](script_asset) scriptAsset, boolean recursive) | [Script](script) | Find a script by its script asset. This can be recursive to find the script on any child entities | None |
| FindScriptProperty(string propertyName) | object | Find a script with the named property on it and return value from the property | None |
| FindAllScripts(string scriptName) | table<[Script](script)> |  Find all scripts named scriptName recursively on this entity and all child entities. Most often used where multiple scripts are used to simulate an array of structures | None |
| FindAllScripts([ScriptAsset](script_asset) scriptAsset) | table<[Script](script)> | Find all scripts of the given script asset recursively on this entity and all child entities. Most often used where multiple scripts are used to simulate an array of structures | None |
| FindAllScripts([ScriptAsset](script_asset) scriptAsset, boolean recursive) | table<[Script](script)> | Find all scripts named scriptName on this entity (and optionally recursively on all child entities if recursive flag is set). Most often used where multiple scripts are used to simulate an array of structures | None |
| FindAllScripts(string scriptName, boolean recursive) | table<[Script](script)> | Find all scripts of the given script asset on this entity (and optionally recursively on all child entities if recursive flag is set). Most often used where multiple scripts are used to simulate an array of structures | None |
| FindWidget(string widgetName) | [Widget](widget) | This is alternative to entity.widgetName which is the preferred way of getting a widget | None |
| FindWidget(string widgetName, boolean recursive) | [Widget](widget) | This is alternative to entity.widgetName which is the preferred way of getting a widget. This can be recursive to find the widget on any child entities | None |
| FindWidget([WidgetAsset](widget_asset) widget) | [Widget](widget) | Find a widget by its widget asset | None |
| FindWidget([WidgetAsset](widget_asset) widget, boolean recursive) | [Widget](widget) |Find a widget by its widget asset. This can be recursive to find the widget on any child entities | None |
| IsLocalReady() | boolean | When called with an Entity that is owned by a particular client this sees if that Entity has been inited on that client (by calling LocalInit) | Server Only |
| SendTelemetry(string type, table parameters) | None | Send an type of telemetry event to the telemetry server with the given parametersTable for later analysis. Deprecated and will be removed - see Analytics.SendTelemetry | Deprecated |
| PlayTimeline(...) | number | Play a timeline from variable args | None |
| PlayTimelineLoop(...) | None | Loop a timeline from variable args. See [PlayTimeline](###PlayTimeline) | None |
| PlayTimelinePingPong(...) | None | Loop a timeline back and forth from variable args. See [PlayTimeline](###PlayTimeline) | None |
| PlayRelativeTimeline(...) | number | Play a timeline, relative to an entity's parent transform, from variable args. See [PlayTimeline](###PlayTimeline) | None |
| PlayRelativeTimelineLoop(...) | None | Loop a timeline, relative to an entity's parent transform, from variable args. See [PlayTimeline](###PlayTimeline) | None |
| PlayRelativeTimelinePingPong(...) | None | Loop a timeline back and forth, relative to an entity's parent transform, from variable args. See [PlayTimeline](###PlayTimeline) | None |
| CancelTimeline() | None | Cancel any running timeline	| None |
| GetTemplate() | [Template](template) | Given an entity, get the Template it is an instance of (if there is one). Warning - this will return the template even if lots of things have been adjusted on the instance | None |
| GetVelocity() | [Vector](vector) | Get Velocity. Centimeters per second | None |
| SetVelocity([Vector](vector) velocity) | None | Set Velocity. Centimeters per second | None |
| GetAngularVelocity() | [Rotation](rotation) | Get AngularVelocity. Degrees per second | None |
| SetAngularVelocity([Rotation](rotation) velocity) | Set AngularVelocity. Degrees per second | None |



## Properties

| Property Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| visible | boolean | Set whether any physical aspect of the Entity (generally a mesh or a light) is visible within the world | None |
| onInteract | [Event](event) | Called when this entity is interacted with by a player, with the player Character and the HitResult passed as arguments, as well as the Entity from which the onInteract event was sent. An alternative to listening for OnInteract in a script on the entity | None |
| onDestroy | [Event](event) | Called when this entity is destroyed, with the Entity which sent the event passed as an argument. An alternative to listening for OnDestroy in a script on the entity | None | 

### Overrides

| Override Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| index | object | Get a script or widget from the Entity by name, or a mesh, light, etc component on this entity. ie entity.myScript returns a script called myScript, entity.theHud returns a widget named theHud, entity.mesh returns the Mesh of this Entity, entity.light returns the property bag for a light component, etc | None |

## Examples

### AttachTo

Available sockets:

```
spine_01
spine_02
spine_03
spine_04
spine_05
neck_01
neck_02
head
clavicle_l
shoulder_l
upperarm_l
lowerarm_l
hand_l
weapon_l
clavicle_r
shoulder_r
upperarm_r
lowerarm_r
hand_r
weapon_r
thigh_l
calf_l
foot_l
thigh_r
calf_r
foot_r
```

### PlayTimeline 

The following example shows a simple timeline with three positions over a ten second timeline. This will play once when the code is executed. Each change of position is interpolated with EaseInOut.


self:GetEntity():PlayTimeline(
  0.0,                   -- time of first position
  Vector.New(0, 0, 0),   -- first position
  5.0,
  Vector.New(0, 0, 100),
  "EaseInOut",
  10.0,
  Vector.New(100, 0, 100),
  "EaseInOut"
)
The following example shows a timeline which changes both position and rotation of the script's entity.

```lua
self:GetEntity():PlayTimeline(
  0.0,
  Vector.New(0, 0, 0),
  Rotation.New(0, 0, 0),
  1.0,
  Vector.New(0, 0, 100),
  Rotation.New(180, 0, 0)
)
```

The following example shows a timeline which simulates a bouncing ball by moving linearly in the X axis but using EaseOut on the up movement and EaseIn on the down movement to simulate the top of a bounce.

```lua
self:GetEntity():PlayTimeline(
  0.0,
  Vector.New(0, 0, 0),
  1.0,
  Vector.New(100, 0, 100),
  { z = "EaseOut", },
  2.0,
  Vector.New(200, 0, 0),
  { z = "EaseIn", }
)
```

You can pass the values to PlayTimeline as a table, allowing for procedural generation of a path. This example generates a circlulr path by appending times and positions to a table, and then passes the resulting table to PlayTimeline

```lua
local timeline = {}
for time = 0, 8 do
  -- insert time of this keyframe into the timeline table
  table.insert(timeline, time)
  -- insert position into timeline table using some maths to make a circle
  table.insert(timeline,
    Vector.New(
      100 * math.cos(time * math.pi / 4),
      -100 * math.sin(time * math.pi / 4),
      0
       )
  )
end
self:GetEntity():PlayTimeline(timeline)
```