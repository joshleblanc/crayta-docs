# Thruster

## Functions

| Function Name                                        | Return Type | Description                                                                                                     | Tags |
|------------------------------------------------------|-------------|-----------------------------------------------------------------------------------------------------------------|------|
| SetForce([Vector](../types/vector.md) force)         | None        | Set the Force of the thruster, either in world space or relative space depending on the type of thruster        | None |
| SetTorque([Rotation](../types/rotation.md) rotation) | None        | Set the torque, or rotation force, of the thruster                                                              | None |
| SetPosition([Vector](../types/vector.md) position)   | None        | Set the position of the thruster. A force that is not applied at the center of mass will also apply some torque | None |
| SetAutoDestroy(number lifeTime)                      | None        | When set the thruster will be destroyed after the lifetime is up                                                | None |
| SetIgnoreMass(boolean ignoreMass)                    | None        | When true this will turn the force or torque in to accelerational changes, ignoring the mass of the object      | None |

## Examples