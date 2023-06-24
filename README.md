![Flattool Logo](flattool_logo-name.png)

Flattool is a command line script designed to improve the experience of working with flatpaks through the command line.

## Main Features:
1. **Handling Multiple Installs**: Flattool allows you to handle multiple flatpak installs in a loop, ensuring that if a match is not found, your entire queue is not lost.
2. **Simplified App Execution**: Running apps from the command line becomes easier with Flattool. Instead of using the app's full Application ID, you can simply enter a query for Flattool to match.
3. **Cleanup of Orphaned User Files**: Flattool helps you clean up orphaned user data files. It identifies user data files that are not associated with any installed flatpak and offers options to either trash the folder or attempt to install the associated flatpak.

## Important Notes:
- This is my first major project, currently at version 1.0. As a new developer, I appreciate your understanding if there are any bugs.
- Flattool assumes that flatpak user data is stored within the default location: `~/.var/app`.
- Flattool is not meant to replace flatpak; it simply sends appropriate flatpak commands for the desired actions.
- To delete folders, Flattool uses `gio trash` instead of `rm`, so remember to empty your trash to reclaim disk space. This prevents accidental permanent deletion of files.

## Dependencies:
- gio: Flattool uses `gio trash` for deleting folders, so make sure gio is installed. gio is part of glib2.
- flatpak: Since this script is for managing flatpak applications, flatpak itself must be installed.

## Installation Steps:
1. Run the command `printf $PATH` in your terminal to view the directories in your PATH.
2. Download the flattool script to one of the directories shown in the previous step. You can use the following command: `wget -P /path/to/bin/directory https://raw.githubusercontent.com/heliguy4599/flattool/main/flattool`
3. Navigate to the directory where you downloaded the flattool file and run `chmod +x flattool` to make it executable.

You're all set! Now you can run flattool using the command `flattool --help`.
