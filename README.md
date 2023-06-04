# flattool
Flattool is a command line script that should make dealing with flatpaks through the command line better.
## Flattool has 3 main uses.
1. Flattool can handle multiple installs in a loop instead of all at once, meaning that if a match is not found, your entire queue is not lost.
2. Flattool makes running apps from the command line easier. Instead of needing to use the app's full Application ID, you need only to type in a query for flattool to match.
3. Flattool can help clean up orphaned user files. Flattool will find any user data files that do not have an associated flatpak installed, and either trash the folder or attempt to install the flatpak, based on your choice.

## Important things to note:
This is my first big project, there's a reason the version number doesn't start with a 1, haha. All this to say that I foresee that there could be issues.
Flattool assumes that flatpak user data is stored within ~/.var/app (the default location for these folders).
Flattool is not a replacement for flatpak, it merely sends the appropriate flatpak commands for the action.

## How to install:
run `echo $PATH` in your terminal.
Place this script within any file mentioned in the output of that command.
