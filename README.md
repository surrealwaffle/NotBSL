# NotBSL
Reimplementation of the Blam Scripting Engine using modern C++ (17/early 20).

## About the Blam Scripting Language

BSL (Blam Scripting Language) is the name of the scripting language used in `Halo: Combat Evolved`.
It has a syntax similar to `Lisp`, but that is where the resemblance ends.
BSL's user primitives consist of globals and scripts; functions are all built-in and typically simply set values for the game engine to process later.
Each script is assigned a thread of execution in the scripting engine. There is therefore a correspondence between the script, which summarizes the flow of execution, and the thread, which contains the state of execution.
There is some cooperation between scripts, as some may be waiting on conditions set by other scripts.
In all, BSL is very limited as a language, but serves the purpose of triggering conditions and effects that would otherwise bog down the hard code.

## Project Scope
This project is intended to replicate the scripting engine used in `Halo: Combat Evolved` from a requirements perspective.
Given the date of the game and the language it was programmed in, there will be a number of differences and likely more as the project evolves.
The following is a rough list of features of the project should deliver upon:
 * basic primitives (boolean, integer, string, global, script);
 * basic operations on primitives (arithmetic, set/get, wake/sleep);
 * script threads operate in discrete steps (ticks);
 * serializable and deserializable script engine state.
