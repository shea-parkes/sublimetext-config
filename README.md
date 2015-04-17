The intention of this repository is to be cloned into the `%AppData%\Sublime Text 3\Packages\User` folder.  You can forcibly clone into an existing repository with `git clone https://github.com/skparkes/sublimetext-config.git .` (notice the trailing `.`).

You'll likely need to install `Package Control` first.  In theory, it will then install all the other packages enumerated in its own configuration files.  The following packages still would need manual installation after that:
  * [SAS](https://github.com/rpardee/sas)

### Anaconda Python Distribution Integration (Not to be confused with the Anaconda Sublime Package for Python)

The following setup seems to work well for best results when integrating with linters and code completion:
  * Using `conda`, setup a new environment that has your chosen linters (e.g. `pylint`, `pep8`, `pyflakes` etc) and possible any commonly used packages you want to code complete
  * In your system `PATH`, include the following:
    * The `Scripts` subdirectory of your root Miniconda install.  This will make `conda` and `activate` available from the command line.
    * The root directory of your IDE environment described above.  This should be the path containing the corresponding `python.exe`
    * The `Scripts` directory of you IDE environment described above.  This should make the linters available from the command line.
  * It is **not** recommended to put the root path of your root Miniconda install because many plugins appear to get confused when they find the corresponding `python.exe` in that directory.
  * Most of the packages, especially the code completion packages, allow to explicitly specify extra paths/environments to scan/utilize.  You can specify these in the root Sublime settings for the corresponding package, or often in the project level settings file as well.

##Notes on various packages:

### SublimeLinter

This package manhandles the configuration file directory somewhat.  In insists on manipulating the chosen theme to have the colors it desires, so you'll see it constantly making a modified copy of the theme into this directory.  It also forces the user settings file to always have all the options enumerated in it.

## Shortcuts worth knowing
| Family | Keys | Effect |
| :----- | :--- | :----- |
| Root | `Ctl`+`Shift`+`P` | Command palette. |
| Root | `Ctl`+`P` | Goto anything. |
| Root | `Ctl`+` | Internal Sublime console. |
| Root | `Ctl`+`Alt`+`P` | Switch project. |
| Windows | `Ctl`+`PageUp` (or `PageDown`) | Switch tabs in current window. |
| Windows | `Alt`+`Shift`+`1` (or `2`) | Make 1 (or 2) windows. |
| Windows | `Ctl`+`1` (or `2`) | Move focus to first (or second) window. |
| Windows | `Ctl`+`K`,`Left` (or `Right`) | Move focus in the chosen direction. |
| Windows | `Ctl`+`Shift`+`1` (or `2`) | Move current view into first (or second) window. |
| Windows | `Ctl`+`K`,`B` | Show/hide sidebar. |
| Windows | `Ctl`+`Up` (or `Down`) | Scroll window without moving cursor. |
| Selection | `Ctl`+`Alt`+`Up` (or `Down`) | Extend multiple cursors up (or down). |
| Selection (~Quick) | `Ctl`+`D` (and repeat) | Select the current, then the next (and next) instance of a word. |
| Selection (~Quick) | `Ctl`+`U` (and repeat) | Undo the last `Ctl`+`D` (see above) |
| Selection (~Quick) | `Ctl`+`K`,`D` | Skip the current instance of the word and select the next. |
| Selection (~Quick) | `Alt`+`F3` | Select the current, and all other instances of a word. |
| Selection | `Ctl`+`Shift`+`Space` | Expand selection to scope. |
| Selection | `Ctl`+`Shift`+`M` | Expand selection to brackets. |
| Code Navigation | `Ctl`+`R` | Goto ~definition. |
| Text Manipulation | `Ctl`+`/` | Toggle comment. |
| Text Manipulation | `Ctl`+`Shift`+`/` | Toggle block comment. |
| Text Manipulation | `Ctl`+`K`,`U` (or `L`) | Convert selection to uppercase (or lowercase). |
| Text Manipulation | `Ctl`+`Space` | Force code completion. |
| Text Manipulation | `Ctl`+`]` (or `[`) | Indent (or unindent) |
| Text Manipulation | `Ctl`+`Shift`+`Up` (or `Down`) | Move current line/selection up (or down) |
| Text Manipulation | `F9` (or `Ctl`+`F9`) | Sort lines (or sort lines case-sensitive) |
