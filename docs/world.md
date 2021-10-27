# World

## Functions

| Function Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| RevertClientProperty(string propertyName) | None | Revert a property that's been changed on the client back to the server's value for it | Client Only |
| Raycast([Vector](vector) start, [Vector](vector) end, [Entity](entity) entityToIgnore, function callback) | None | Send a ray (line) from start position to end position, and call the collisionCallback with the entity that was hit and a HitResult structure if any Entity is hit along the way. Pass an entityToIgnore to tell it not to hit that one (for example ignore the player when doing a ray from a gun the player is holding) | None |
| Raycast([Vector](vector) start, [Vector](vector) end, table<[Entity](entity)> entitiesToIgnore, function callback) | None | Send a ray (line) from start position to end position, and call the collisionCallback with the entity that was hit and a HitResult structure if any Entity is hit along the way. Pass an array of entities to ignore | None |
| Raycast([Vector](vector) start, [Vector](vector) end, [Entity](entity) entityToIgnore, boolean highFidelityCollision, function callback) | None | Send a ray (line) from start position to end position, and call the collisionCallback with the entity that was hit and a HitResult structure if any Entity is hit along the way. Pass an entityToIgnore to tell it not to hit that one (for example ignore the player when doing a ray from a gun the player is holding). High fidelity collisions will ignore any collision with an entity's bounding box if it would not also collide with it's more complex inner collision | None |
| Raycast([Vector](vector) start, [Vector](vector) end, table<[Entity](entity)> entitiesToIgnore, boolean highFidelityCollision, function callback) | None | Send a ray (line) from start position to end position, and call the collisionCallback with the entity that was hit and a HitResult structure if any Entity is hit along the way. Pass an array of entities to ignore. High fidelity collisions will ignore any collision with an entity's bounding box if it would not also collide with it's more complex inner collision | None |
| Find(string name) | [Entity](entity) | Find a named Entity within the world. Generally an entity type property which is filled in in the editor is a better option | None |
| FindAll() | table<[Entity](entity)> | Return all entities in the world. Can be very slow | None |
| FindAll(table derivedType) | table<[Entity](entity)> | Return all entities in the world of the given type (Light, Mesh, etc). Can be very slow | None |
| FindAllScripts(string scriptName) | table<[Script](script)> | Find all scripts named scriptName recursively in the world. Most often used where multiple scripts are used to simulate an array of structures | None |
| FindAllScripts([ScriptAsset](script_asset) scriptAsset) | table<[Script](script)> | Find all scripts matching the script asset recursively in the world. Most often used where multiple scripts are used to simulate an array of structures | None |
| FindScript(string scriptName) | [Script](script) | Find any entity with a script named scriptName recursively in the world, returns the script if found | None | 
| FindScript([ScriptAsset](script_asset) scriptAsset) | [Script](script) | Find any entity with a script matching the script asset recursively in the world, returns the script if found | None |
| FindTemplate(string name) | [Template](template) | Find a Template in the world by name. Returns nil if not found | None |
| GetLocalUser() | [User](user) | Get the User that this client is owned by | Client Only |
| GetUsers() | table<[User](user)> | Get a table containing all the User entities within the current world. This works on the server or the client however the client version of the table might lag behind the server version | None |
| ForEachUser(function callback) | None | Call the given callback for each User with the User as the argument | None |
| ApplyPointDamage(number baseDamage, [Vector](vector) rayStart, [Vector](vector) direction, [Entity](entity) fromEntity) | None |  Applies point damage to the first Entity that intersects the given ray | Server Only |
| ApplyPointDamage(number baseDamage, [Vector](vector) rayStart, [Vector](vector) direction, [Entity](entity) fromEntity, table damageModifiers) | None | Applies point damage to the first Entity that intersects the given ray | Server Only |
| ApplyRadialDamage(number baseDamage, [Vector](vector) origin, number radius, number falloff, [Entity](entity) fromEntity) | None | Applies radial damage to all Entities within a radius of an origin | Server Only |
| ApplyRadialDamage(number baseDamage, [Vector](vector) origin, number radius, number falloff, [Entity](entity) fromEntity, table damageModifiers) | None | Applies radial damage to all Entities within a radius of an origin | Server Only |
| SetVoxelProperties(table properties) | None | Set the voxel properties of the world | Server Only |
| SetVoxelProperties(table properties, number defaultMaxHealth, number defaultHealTime) | None | Set the voxel properties of the world | None |
| GetTimeOfDay() | number | Get the time of day as a value between 0 and 1 | None |
| Spawn([Template](template) template, [Vector](vector) position, [Rotation](rotation) rotation) | [Entity](entity) | Spawn a new Entity from the template pointed at by templateAsset, at the given position and rotation | Server Only |
| Spawn([Template](template) template, [Locator](locator) locator) | Spawn a new Entity from the template pointed at by templateAsset, at the given locator's position and rotation | Server Only |
| BroadcastToScripts(string eventName, ...) | None | Try calling eventName on all scripts of all Entities within the World. When called on the server it sends to server scripts only, if called on the client it will send to client scripts only | None |
| GetServerTime() | number | Get server up time in seconds (can be called on client or server) | None |
| GetUTCTime() | number | Gets unit time (number of seconds that have elapsed since Jan 1 1970). This has an issue that it will start to overflow 32-bits in 2038 | None |
| GetGames(string railName, function callback) | None | Get all games from a specified rail | None |
| GetGames(table<string> railNames, function callback) | None | Get all games from the specified rails | None |
| GetActiveChallenges() | table | Gets the current active challenges | None |
| PlayCameraShakeEffectAtLocation([CameraShakeAsset](camera_shake_asset) cameraShake, number scale, [Vector](vector) location, number innerRadius, number outerRadius, number falloff, boolean orientToDirection) | None | Play a camera shake effect at this location in the world with a scale multiplier	| None |
| PlayCameraShakeEffectAtLocation([CameraShakeAsset](camera_shake_asset) cameraShake, [Vector](vector) location, number innerRadius, number outerRadius, number falloff, boolean orientToDirection) | None | Play a camera shake effect at this location in the world | None |
| GetWorldAsset() | [WorldAsset](world_asset) | Returns the WorldAsset that's currently loaded | None |


## Properties

| Property Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| startTime | number | Start time of day from 0.0 (midnight) - 0.5 (midday) - 1.0 (next midnight) | Read-Write |
| dayLength | number | Length of virtual 'day' in real-time seconds	| Read-Write |
| sunDirection | number | Angle of sun in degrees. Controls whether the sun rises from west to east, north to south, etc. | Read-Write |
| sunColor | [Color](color) | Color of the sun | Read-Write |
| sunIntensity | number | Intensity of the sun | Read-Write |
| heightFogStartDistance | number | Height fog start distance | Deprecated |
| heightFogFalloff | number | Height fog falloff | Deprecated |
| heightFogDensity | number | Height fog density | Deprecated |
| heightFogColor | [Color](color) | Color of the height fog	| Deprecated |
| skyLightIntensity | number | Intensity of the ambient light | Read-Write |
| skyLightColor | [Color](color) | Color of the ambient light | Deprecated |
| postProcess | [PostProcessAsset](post_process_asset) | Post Process effect | Read-Write |
| colorGrading | [ColorGradingAsset](color_grading_asset) | Color Grading effect | Read-Write |
| skydome | [SkydomeAsset](skydome_asset) | Skydome asset | Deprecated |
| innerHorizon | [HorizonAsset](horizon_asset) | Inner Horizon asset | Read-Write |
| outerHorizon | [HorizonAsset](horizon_asset) | Outer Horizon asset | Read-Write |
| skyMesh | [SkyMeshAsset](sky_mesh_asset) | Sky Mesh asset | Read-Write |
| enableShadows | boolean | Enable/Disable Shadows | Read-Write |
| fogStartDistance | number | Fog start distance | Read-Write |
| fogDensity | number | Fog density	| Read-Write |
| fogFalloff | number | Fog falloff	 | Read-Write |
| fogColor | [Color](color) | Color of the fog | Read-Write |
| fogAffectedByAtmosphere | boolean | Fog Affected by Atmosphere | Read-Write | 
| cloudDensity | number | Cloud Density | Read-Write |
| cloudCoverage | number | Cloud Coverage | Read-Write |
| cloudAltitude | number | Cloud altitude | Read-Write |
| cloudLayerThickness | number | Cloud Layer Thickness | Read-Write |
| atmosphereThickness | number | Set the thickness of the atmosphere. 1 = None, 2 = Thin, 3 = Earth-Like | Read-Write |
| atmosphericScatteringColor | [Color](color) | Atmospheric Scattering Color | Read-Write |
| atmosphereTint | [Color](color) | Atmosphere Tint | Read-Write |
| deathPlaneActive | boolean | Set whether the death plane is active or not	| Read-Write |
| deathPlaneZ | number | Height of the death plane, when active the game will send OnFellToDeath to any Player who falls below this, automatically putting the Player back to where they spawned if the event is not responded to by any scripts | Read-Write	

## Examples

### ApplyPointDamage

DamageModifiers is a table of 

```
{ 
    voxel = [VoxelAsset](voxelAsset), 
    damageMultiplier = number 
} 
```

tables, and/or scripts that have voxel and damageMultiplier properties: `{ name = "voxel", type = "voxelasset" } and { name = "damageMultiplier", type = "number" }`:

```
damageModifiers = { 
    { voxel = [VoxelAsset](voxel_asset), damageMultiplier = number }, 
    { voxel = [VoxelAsset](voxel_asset), damageMultiplier = number }, 
    [Script](script), 
    [Script](script) 
}
```

### SetVoxelProperties

VoxelProperties is a table of { voxel = <voxelasset>, health = <number>, healTime = <number> } tables, and/or scripts that have voxel, and optionally health and healTime properties: { name = "voxel", type = "voxelasset" }, { name = "health", type = "number", default = 100 }, { name = "healTime", type = "number", editor = "seconds", default = 3 }. voxelProperties = { { voxel = <voxelasset>, health = <number>, healTime = <number> }, { voxel = <voxelasset>, health = <number> }, { voxel = <voxelasset>, healTime = <number> }, <script>, <script> } Defaults are 100 for health, 3.0 for heal time.

### GetActiveChallenges

Example result table: result = {} result[1] = {id = <ChallengeId>, name = <LocalisedName>, icon = <IconUrl>, count = <TotalCountToComplete>} result[2] = {id...