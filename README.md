# iTunes-Export
itunes-export is a small python utlity script that allows to export your iTunes playlists into M3U format. This allows to use or import these playlists into other media players such as VLC.

In order to use this script, iTunes must store your Library into XML format. If you don't see an .xml library file in `~/Music/iTunes`, you probably started using iTunes after version 12.2, and have never enabled sharing between iTunes and other apps. To generate one, go to iTunes Preferences | Advanced and select "Share iTunes Library XML with other applications." ([Apple docs](https://support.apple.com/en-us/HT201610))

## Usage:
```bash
itunes-export --output "X:\Playlists" --ignore "Downloads"
```
This command exports all your playlists except "Downloads" into the folder "X:\Playlists".

Available commands:
* --output, -o: mandatory, sets the folder to export to.
* --ignore: optional, allows to ignore a specifc playlist in the export. Multiple playlists can be ignored.
* --library, -l: optional, explicitly provide the path to the iTunes XML library file. By default the one of the current user is used. 
* --export-genius-playlists: optional, export genius playlists. By default they are not exported.
* --export-smart-playlists: optional, export smart playlists. By default they are not exported.
* --help, -h: optional, get the command line help.