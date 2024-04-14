# World Partition

## Streaming sources
A streaming source is an object that will be used by the world partition system to determine which cells to load or unload at runtime.

By default, a player controller is a streaming source. Any actor can become a streaming source if it has a World Partition Streaming Source component added to it.

## Tips
- Console commands related to world partition starts with `wp.`