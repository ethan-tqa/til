# Unreal Engine async loading screen    

## Talks
- [Async Loading Screens and Transition Levels | Unreal Fest Europe 2019](https://youtu.be/ON1_dEHoNDg)

## Examples
- [Action RPG sample](https://www.unrealengine.com/marketplace/en-US/product/action-rpg)
- [truong-bui/AsyncLoadingScreen](https://github.com/truong-bui/AsyncLoadingScreen)

## Flow
- Create a separate thread for the loading screen.
- Call load level in the main thread.
- When load level finishes, stop the loading screen thread, switch back to main thread.

## Seamless travel
In non-seamless travel, the client disconnects from the sever, changes map, reconnects. In seamless travel, the client loads a transition map, load the new map in the background, once done remove the transition map & notify server.

By default, these actors will be kept alive:   
- Server: GameMode, GameState, controllers with PlayerState.
- Client & server: PlayerController.

To keep other actors alive, use `GameModeBase::GetSeamlessTravelActorList()` on server and `APlayerContro11er::GetSeam1essTravelActorList()` on client.\
Note that seamless travel cannot be used when the first map is being loaded or connecting to a new server.\
The main drawback of seamless travel is difficulties in debugging.

## Relevant information
- Slate runs on its own thread.
- It is advisable to implement the feature inside a separate module, and the game logic should invoke this module for map changes instead of calling the engine directly. The module should be set to load early, e.g. `PreLoadingScreen`.