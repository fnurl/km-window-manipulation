# README

Macros for [Keyboard Maestro](https://www.keyboardmaestro.com) for
manipulating windows (moving and resizing).

The following macro groups are used, so if you have groups with these
names, the macros will be imported into them (spaces are used for
organization):

- `Window Management:  Main`: main activation macro + state changing
  macros) 
- `Window Management:  Move/Resize`: Selectable actions in the Palette
- `Window Management: Helpers`: Macros that do the actual moving, resizing
  and setting values variables that are used during window manipulation


## Variables and config

- All macro variables used by the macro start with the prefix `WINDOW_`
- The macro `Config/Init Window Management` macro contains two configurable variables:
    - `WINDOW_INITIAL_COUNTDOWN` defines how many seconds to wait for
      keyboard trigger input.
    - `WINDOW_SHOW_PALETTE`: the palette is shown if the value of
      `WINDOW_SHOW_PALETTE` is anything except for 0.


## States

1. Show menu palette or activate in background.
2. When activated, the user can select one action to perform.
3. If an action has been performed within `WINDOW_INITIAL_COUNTDOWN` seconds,
   the menu palette is re-activated. GOTO State 2.
4. If no action was selected, hide the menu palette and deactivate window
   manipulation hotkeys.
