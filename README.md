# UnityDoorstop for Linux

This is a quick and dirty [UnityDoorstop](https://github.com/NeighTools/UnityDoorstop) equivalent for Linux and macOS.

## How to build

You need gcc to build this binary

Linux:
```sh
gcc -shared -fPIC -o doorstop.so doorstop.c
```

macOS:
```sh
gcc -shared -fPIC -o doorstop.dylib doorstop.c
```

## How to use

1. Put the built `doorstop.so` (or `.dylib`) and `run.sh` to the same directory as the game
2. Edit `run.sh` to configure Doorstop to work correctly
3. Run `run.sh` when you want to run your game modded
4. When you want to run vanilla game, run the game normally

## Note for macOS users

You cannot directly run the `Game.app`, as it is just a folder. Instead, you must edit `run.sh` to execute `Game.app/Contents/MacOS/Game` (or other game executable depending on the Unity game).