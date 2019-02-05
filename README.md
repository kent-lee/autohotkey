# AutoHotKey Script

This is a collection of my AHK scripts, with `Daily.ahk` being the main script that I run daily. Some files specified in the `#include` commands in `Daily.ahk` are not uploaded (i.e. `AutoCorrect.ahk`) because they contain private information.

## Windows Configuration

### Auto Startup (no admin privilege)

1. create script shortcut and put it in startup folder

2. folder location: <kbd>Win</kbd>+<kbd>r</kbd> &rightarrow; `shell:common startup`

### Auto Startup (admin privilege)

1. use built-in task scheduler (avoids UAC prompt): <kbd>Win</kbd> &rightarrow; `task scheduler`

2. `Create Task`

    - `General` &rightarrow; enter task name &rightarrow; check `run with highest privileges`

    - `Triggers` &rightarrow; `New` &rightarrow; `at log on`

    - `Actions` &rightarrow; `New` &rightarrow; `Browse` for script location

## Issues

- **file path**: some programs need to specify full path to run

- **conflicting titles**:

    - `Discord` and `Google Chrome` have the same `ahk_class`

    - `File Explorer` and `Taskbar` have the same `ahk_exe`

    - `File Explorer` and `Control Center` have the same `ahk_class`

    - `File Explorer` has no consistent title (i.e. `- window title`)

    - `Discord` home page is `Discord` instead of `... - Discord`

## Todo

- <kbd>Capslock</kbd>+<kbd>Space</kbd>: cycle group (<kbd>Win</kbd>+<kbd>1~9</kbd>)

- use <kbd>Shift</kbd> as secondary function

- <kbd>Capslock</kbd>+<kbd>wasd</kbd>: move window to position (top left, bottom left, right side)

- <kbd>Capslock</kbd>+<kbd>t</kbd>: terminal opened in specific directory

## Notes

Some command parameters do not allow expression syntax, so legacy syntax is needed (i.e. `%Var%` or `% Var`)

All function parameters allow expression syntax, meaning variables do not need to be wrapped with percent sign

**Variables**: variables store everything on the right side as _String_. Not case sensitive. No need to declare/specify type of variables

**Hotstring**:

- `{{}` = `{`
- `{}}` = `}`
- `{Return}`,`{Enter}`,`` `n`` = new line
- `{Tab}`,`` `t`` = tab