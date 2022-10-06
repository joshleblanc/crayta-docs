# SoundHandle

Inherits from: [Handle](handle)

## Functions

| Function Name                                  | Return Type | Description                                                                           | Tags |
|------------------------------------------------|-------------|---------------------------------------------------------------------------------------|------|
| Stop()                                         | None        | Stop the sound represented by this handle                                             | None | 
| Stop(number fadeOut)                           | None        | Stop the sound represented by this handle, fading out over fadeOut seconds            | None |
| SetPitch(number pitch)                         | None        | Set the pitch on this sound (1 = Default pitch, 0.5 = half speed, 2 = 2 times faster) | None |
| SetVolume(number volume)                       | None        | Set the volume on this sound (0 = Silent, 1 = Full volume)                            | None |
| SetRange(number rangeMin, number rangeFallout) | None        | Given a sound Handle sets the attenuation range minimum and falloff                   | None |

## Examples