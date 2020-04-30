# NotBSL
Reimplementation of the Blam Scripting Engine using modern C++ (17/early 20).

## Scope
This project is intended to replicate the scripting engine used in `Halo: Combat Evolved` from a requirements perspective.
Given the date of the game and the language it was programmed in, there will be a number of differences and likely more as the project evolves.

 * By-tick advance: Time advances for each script thread in discrete steps.
 * Core dump and load: The state of the scripting engine must be serializable and deserializable. 
 * Dynamic core address: Rather than allocating the core to a fixed location like `Halo`, `NotBSL` must be able to reposition across core dumps and loads.