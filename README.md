# dwl

This is my patched version of dwl.
This belongs to my larbs installation script and depends heavily on its scripts
and programs.
It is supposed to work in the environment after the
[larbs base installation](https://github.com/tiyn/larbs).
This repository is set up according to the
[suckless entry of my wiki](https://github.com/tiyn/wiki/blob/master/wiki/linux/suckless.md).

## Patches

The list below shows the currently applied patches to the master branch.

- attachtop.patch (new clients are attached at the top of the stack)
- bottomstack.patch (adds bottomstack and bottomstackhorizontal layouts)
- deck.patch (adds deck layout with one master and stacked clients)
- en-keycodes.patch (always uses the english keycodes)
- fakefullscreenclient.patch (enables per-client fake fullscreen)
- foreign-toplevel-management.patch (allows external programs to query/control windows)
- hide-behind-monocle.patch (hides unfocused windows in monocle layout)
- hide-behind-fullscreen.patch (hides other windows behind fullscreen clients)
- inputdevicerules-v0.7.patch (adds per-input-device configuration rules)
- ipc.patch (adds IPC for external control and scripting)
- pertag.patch (stores layout, mfact, nmaster, bar state per tag)
- swallow.patch (replaces terminal with spawned application)
- togglekblayoutandoptions.patch (toggles keyboard layouts and XKB options at runtime)
- unclutter.patch (hides cursor after inactivity)
- warpcursor.patch (moves cursor to the focused window)
- xwayland-handle-minimize.patch (improves minimize/restore handling for XWayland)

## Hotkeys

There are various shortcuts and hotkeys used in this version. Included in my
build are the following.

| ModKey | Shift | Key         | Function                                                |
| ------ | ----- | ----------- | ------------------------------------------------------- |
| Super  |       | h           | (Tiling/Deck) Focus window higher in stack than current |
| Super  |       | j           | (Tiling/Deck) Focus window lower in stack than current  |
| Super  |       | k           | (Tiling/Deck) Focus window higher in stack than current |
| Super  |       | l           | (Tiling/Deck) Focus window lower in stack than current  |
| Super  |       | 1/2/.../9/0 | Show tag 1/2/.../9/0                                    |
| Super  |       | .           | Show monitor lower in stack                             |
| Super  |       | ,           | Show monitor higher in stack                            |
| Super  | Shift | Escape      | Quit dwl with call for confirmation                     |
| Super  | Shift | c           | Enable deck(/card) layout                               |
| Super  | Shift | d           | Toggle floating/tiled for selected window               |
| Super  | Shift | f           | Toggle fullscreen                                       |
| Super  | Shift | h           | (Tiling/Deck) Make current window the master window     |
| Super  | Shift | j           | (Tiling/Deck) Make current window the master window     |
| Super  | Shift | k           | (Tiling/Deck) Make current window the master window     |
| Super  | Shift | l           | (Keyboard) Cycle through the keymap layouts             |
| Super  | Shift | m           | Enable monocle layout                                   |
| Super  | Shift | o           | (Tiling/Deck) Increase master window size               |
| Super  | Shift | q           | Close current window                                    |
| Super  | Shift | t           | Enable tiling layout                                    |
| Super  | Shift | u           | Enable bottomstack layout                               |
| Super  | Shift | v           | Enable bottomstackhorizontal layout                     |
| Super  | Shift | z           | (Tiling/Deck) Decrease master window size               |
| Super  | Shift | 1/2/.../9/0 | Add current window to tag 1/2/.../9/0                   |
| Super  | Shift | .           | Add to monitor lower in stack                           |
| Super  | Shift | ,           | Add to monitor higher in stack                          |
| Alt    |       | Tab         | (Tiling/Deck) Focus window lower in stack than current  |

Additionally the right hand side control key is set to be used as the compose key.

## Installation

The following programs are required to be installed for full functionality.

- [dmenu](https://github.com/tiyn/dmenu)

The most basic way is to clone the repository and then invoke make.

- `git clone https://github.com/tiyn/dwl`
- `make clean install`
