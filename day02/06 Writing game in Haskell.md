Writing a game in Haskell
=========================

Elise Huard
https://leanpub.com/gameinhaskell
@elie_huard

## Graphics
- Binding to OpenGL in Haskell is relatively easy (c library)
- [GLFW-b](https://github.com/bsl/GLFW-b)
- ThreadDelay: so your cpu can rest
- FRP
    + the position of the player is a stream of signal
    + FRP and level, some part of the game needs to die when level end
    + SignalGen for the level
- Texture
- Sound: OpenAL
    + Non thread-safe

## Animation
- Keyframe animation
    + Skeletal animation for more complex
- **Blender!**

## Physics
- 2d physics library: chipmunk
    + Haskell binding: hipmunk

## Haskell 
- Types
- Pattern Matchings
- nice bindings

## Unanswered question
- packaging, porting?
- performance?
- gettings started was painful (library didn't compile, etc)
- compilation (slow work flow)

## Reference
The art of game design by jesse schell

## Example 
- Nikie and robot
- Mobile games in haskell
- Wayward Tides (chuklefish)
