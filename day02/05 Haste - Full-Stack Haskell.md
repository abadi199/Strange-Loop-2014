Haste: Full-Stack Haskell (For non-PhD Candidates)
==================================================

@lasericus
@coopernurse
http://github.com/laser/slides

## Haste
compiled to javascript with standard library

Demo Example:
- Interfacing with DOM
- Interacting with local storage
- Ajax
- HTML5 canvas
- MVC

## FFI (Foreign Function Interface)
- Call regular javascript from Haste
    + Wrap existing library
- Export Haste functions and call them from regular JS code

### ccall
write your .hs code
write a .js file containing global functions
include the global function in the .hs file

### ffi
- no external .js required
- ffi is unsafe function that wil lbe called at runtime, slower than ccall, but no external .js file required.

### JS calling haste function
use
in .hs

    export (toJSSString "addInt") addInt

in .js

    Haste.addInt();

## Errors, Testing, and Dependencies
- some errors handling is built in in the api.
- Debuggin: can't use browser debugger because the compiled code looks totally different.
- no words on source map support in the future
- Testing with HSpec
- Hspec is runnign in haskell, not running in js (might run in haskell but break in js)
    + Integer in haskell is different from js

## Hackage
Haste package manager, not using cabal (haskell package manager)

## Projects to watch
[Aleberto Corona's playground](http://tryoplayg.herokuap.com)

