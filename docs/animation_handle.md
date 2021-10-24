# AnimationHandle

## Functions

| Function Name | Return Type | Description | Tag |
| ------------- | ----------- | ----------- | --- |
| IsPlaying() | boolean | returns true if this animation is still playing | None |
| GetPlaybackSpeed() | number | get the current playback speed of the animation | None |
| SetPlaybackSpeed(number speed) | None | set the current playback speed of the animation	| None
| IsLooping() | boolean | get whether this animation is set to loop	 | None |
| SetLooping(bool looping) | None | set whether this animation should loop	 | None |
| Stop() | None | stops/cancels the animation on this mesh, this will invalidate this handle as the animation it relates to is no longer playing | None |
| SetProgress(number normalizedTime) | None | Set the progress of the animation. 0.0 = the start of the animation, 0.5 = 50% of the way through the animation, 1.0 = the end of the animation, etc | None |
| GetProgress() | number | Returns the progress of the animation. 0.0 = the start of the animation, 0.5 = 50% of the way through the animation, 1.0 = the end of the animation, etc |


## Examples