The intention of this repository is to be cloned into the `%AppData%\Sublime Text 3\Packages\User` folder.  You can forcibly clone into an existing repository with `git clone https://github.com/skparkes/sublimetext-config.git .` (notice the trailing `.`).

You'll likely need to install `Package Control` first.  In theory, it will then install all the other packages enumerated in its own configuration files.  The following packages still would need manual installation after that:
  * [SAS](https://github.com/rpardee/sas)

Notes on various packages:

### SublimeLinter

This package manhandles the configuration file directory somewhat.  In insists on manipulating the chosen theme to have the colors it desires, so you'll see it constantly making a modified copy of the theme into this directory.  It also forces the user settings file to always have all the options enumerated in it.
