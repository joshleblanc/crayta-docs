# CharacterBase

Inherits from: [Entity](entity)

## Functions

| Function Name                                                                                            | Return Type                                        | Description                                                                                                                                                                                                                                                                                                                                                                    | Tags                    |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| Attach([Entity](entity) entityToAttach, string socketName)                                               | None                                               | Deprecated, see [AttachTo](entity.md#AttachTo)                                                                                                                                                                                                                                                                                                                                 | Deprecated, Server Only |
| SetAlive(boolean alive)                                                                                  | None                                               | Set the character state to alive or dead                                                                                                                                                                                                                                                                                                                                       | Server Only             |
| IsAlive()                                                                                                | boolean                                            | Get whether a Player is alive. Return false for non-Player                                                                                                                                                                                                                                                                                                                     | None                    |
| SetGrip([GripAsset](../assets/grip_asset) gripAsset)                                                     | None                                               | Set the current grip animations used by this player. Passing nil is the same as calling SetNoGrip()                                                                                                                                                                                                                                                                            | None                    |
| SetNoGrip()                                                                                              | None                                               | Reverts the player back to the default 'unarmed' animations. Can also be achieved by calling SetGrip(nil)                                                                                                                                                                                                                                                                      | None                    |
| PlayAction(string action, table properties)                                                              | None                                               | Play an animation action, with properties specifying how it should be played                                                                                                                                                                                                                                                                                                   | None                    |
| PlayAction(string action)                                                                                | None                                               | Play an animation action with default properties                                                                                                                                                                                                                                                                                                                               | None                    |
| HasAction(string action)                                                                                 | boolean                                            | Returns true if the current grip can perform this type of action                                                                                                                                                                                                                                                                                                               | None                    |
| GetActions()                                                                                             | table                                              | Get the name of every available action for the current grip                                                                                                                                                                                                                                                                                                                    | None                    |
| GetActionEvents(string action)                                                                           | table                                              | Get the name of every available event for an action                                                                                                                                                                                                                                                                                                                            | None                    |
| HasActionEvent(string action, string event)                                                              | boolean                                            | Returns true if this action has an animation event of the specified name                                                                                                                                                                                                                                                                                                       | None                    |
| GetPlayLength(string action)                                                                             | number                                             | Returns the length of an animation, in seconds, assuming a playbackSpeed of 1 is set                                                                                                                                                                                                                                                                                           | None                    |
| Launch([Vector](../types/vector) vector)                                                                 | None                                               | Launch the character                                                                                                                                                                                                                                                                                                                                                           | None                    |
| AdjustAim(...)                                                                                           | [AdjustAimHandle](../handles/adjust_aim_handle.md) | Programmatically move the user's camera to look at specific points                                                                                                                                                                                                                                                                                                             | None                    |
| CancelAdjustAim([AdjustAimHandle](../handles/adjust_aim_handle.md) handle)                               | None                                               | Cancel an aim adjustment                                                                                                                                                                                                                                                                                                                                                       | None                    |
| IsAdjustAimActive()                                                                                      | boolean                                            | Returns whether the player's aim is currently being adjusted                                                                                                                                                                                                                                                                                                                   | None                    |
| IsCrouching                                                                                              | boolean                                            | Returns true if the character is crouching                                                                                                                                                                                                                                                                                                                                     | None                    |
| StartOccupy([Entity](entity) entityToOccupy)                                                             | None                                               | Occupying an entity will attach the character to it using animations associated with the occupy asset (sit, lie down, etc). If this entity has any occupy sockets, the character will be attached to the first socket using the occupy asset associated with this. Otherwise the character will attach to the entity position, and the default OccupyAsset (Seat) will be used | Server Only             |
| StartOccupy([Entity](entity) entityToOccupy, string socketName)                                          | None                                               | Occupying an entity will attach the character to it using animations associated with the occupy asset (sit, lie down, etc). Attach the character to the provided socket. If this socket is an occupy socket, the character will occupy it using the OccupyAsset associated with this socket. Otherwise the default OccupyAsset (Seat) will be used                             | Server Only             |
| StartOccupy([Entity](entity) entityToOccupy, [OccupyAsset](occupy_asset) occupyAsset, string socketName) | None                                               | Occupying an entity will attach the character to it using animations associated with the occupy asset (sit, lie down, etc). Attach the character to this socket using the animations from the Occupy Asset                                                                                                                                                                     | Server Only             |
| StartOccupy([Entity](entity) entityToOccupy, [OccupyAsset](occupy_asset) occupyAsset)                    | None                                               |                                                                                                                                                                                                                                                                                                                                                                                | Server Only             |
| EndOccupy()                                                                                              | None                                               | Detaches a character from the entity it was occupying from a previous StartOccupy                                                                                                                                                                                                                                                                                              | Server Only             |
| IsOccupying()                                                                                            | boolean                                            | Check if this character is currently occupying an entity                                                                                                                                                                                                                                                                                                                       | None                    |

## Properties


| Property Name                | Return Type | Description                                                                                                                             | Tags       |
|------------------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------|------------|
| speedMultiplier              | number      | Multiplier on movement speed (default is 1.0)                                                                                           | Read-Write |
| jumpHeightMultiplier         | number      | Multiplier on jump height (default is 1.0)                                                                                              | Read-Write |
| canSprint                    | boolean     | Turn on or off ability to sprint                                                                                                        | Read-Write |
| canRun                       | boolean     | Turn on or off ability to run                                                                                                           | Read-Write |
| canWalk                      | boolean     | Turn on or off ability to walk                                                                                                          | Read-Write |
| canMantle                    | boolean     | Turn on or off ability to mantle                                                                                                        | Read-Write |
| maxMantleHeight              | boolean     | Set the maximum height that a player can mantle                                                                                         | Read-Write |
| canSlide                     | boolean     | Turn on or off ability to slide                                                                                                         | Read-Write |
| canRelax                     | boolean     | Turn on or off ability to go into a grip's relaxed pose                                                                                 | Read-Write |
| breakFall                    | boolean     | Turn on or off ability to break fall on landing                                                                                         | Read-Write |
| breakFallSpeed               | boolean     | Turn on or off ability to break fall on landing                                                                                         | Read-Write |
| damageEnabled                | boolean     | Turn on or off damage (ie calling of entry point OnDamaged)                                                                             | Read-Write |

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

### PlayAction

The second argument for PlayAction is a table of properties.

| Name          | Type   | Description                                                                                                                                        |
|---------------|--------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| playbackSpeed | number | Sets the speed to play this animation at. 2 = double speed, 0.5 = half speed                                                                       |
| playbackTime  | number | Sets the time that this animation should take in seconds                                                                                           |
| events        | table  | Some actions trigger events – these are functions that will be triggered in your Lua code once the animation for an action reaches a certain point |

#### Grips

##### Cuff
###### Actions

| Action | Event       | Branching | Description                                                                                                         |
|--------|-------------|-----------|---------------------------------------------------------------------------------------------------------------------|
| Fire   | None        | None      | This will perform a 'interacting' animation with the cuff screen                                                    |
| Fire   | IsCompleted | Yes       | If false, the player will start another cycle of interacting with the screen. If true, then the animation will end. |
| Fire   | OnCompleted | No        | Triggers at the end of the animation (after `IsCompleted` returns true if the event is defined).                    |

###### Example

```lua
local animData = {}
animData.playbackSpeed = 1.0
animData.events =
    {
        IsCompleted = function ()
           Print("Checking if player is still looking at a menu")
           return not self.inMenu
        end,
        OnCompleted = function ()
            Print("Finished interacting with menu")
        end
    }
self:GetEntity():PlayAction("Fire", animData)
```

##### Unarmed
###### Actions

None

##### Knife
###### Events

| Action | Event       | Branching | Description                                                                                        |
|--------|-------------|-----------|----------------------------------------------------------------------------------------------------|
| Melee  | None        | None      | This will perform a ‘slashing’ animation                                                           |
| Melee  | MeleeImpact | No        | This will trigger at the point in the animation when the knife looks like it should hit its target |

##### Pistol
###### Actions

| Action | Event       | Branching | Description                                                                                            |
|--------|-------------|-----------|--------------------------------------------------------------------------------------------------------|
| Fire   | None        | None      | This will perform a ‘shooting’ animation                                                               |
| Reload | None        | None      | This will perform a ‘reload’ animation                                                                 |
| Reload | AmmoAdded   | No        | This will trigger at the point in the animation when the pistol clip has been inserted into the pistol |
| Melee  | None        | None      | This will perform a ‘pistol whip’ animation                                                            |
| Melee  | MeleeImpact | No        | This will trigger at the point in the animation when the pistol looks like it should hit its target    |

##### Rifle
###### Actions

| Action | Event     | Branching | Description                                                                                     |
|--------|-----------|-----------|-------------------------------------------------------------------------------------------------|
| Fire   | None      | None      | This will perform a ‘shooting’ animation                                                        |
| Relaod | None      | None      | This will perform a ‘reload’ animation                                                          |
| Reload | AmmoAdded | No        | This will trigger at the point in the animation when the clip has been inserted into the pistol |

##### RPG
###### Actions

| Action | Event | Branching | Description |
| ---- | ------ | --------- | ----------- | 
| Fire | None  | None | This will perform a ‘rocket launch’ animation |
| Reload | None | None | This will perform a ‘reload’ animation |
| Reload | AmmoAdded | No | This will trigger at the point in the animation when the rocket has been inserted into the RPG |

##### Shotgun
###### Actions

| Action | Event            | Branching | Description                                                                                                                                                                        |
|--------|------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fire   | None             | None      | This will perform a ‘shooting’ animation                                                                                                                                           |
| Reload | None             | None      | This will perform a ‘reload’ animation                                                                                                                                             |
| Reload | AmmoAdded        | No        | This will trigger at the point in the animation when a shell has been inserted into the shotgun                                                                                    |
| Reload | IsReloadComplete | Yes       | If false, another shell will be inserted into the barrel without playing the intro of the animation again. If true, the reload animation will play its outro sequence and complete |

###### Example

```lua
local animData = {}
animData.playbackSpeed = 2.0
animData.events =
    {
        IsReloadComplete = function ()
           Print("Checking if full")
           return self.bullets == self.properties.maxBullets
        end,
        AmmoAdded = function ()
            self.bullets = self.bullets + 1
            Print("Added Bullets, current ammo = " .. self.bullets )
        end
    }
self:GetEntity():PlayAction("Reload", animData)
```
