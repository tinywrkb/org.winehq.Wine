# Flatpak Wine App

This is a Flatpak Wine app that makes use of the experimental [Flatpak Wine Runtime](https://github.com/tinywrkb/flatpak-wine-runtime).  
The App was create for testing and evluating the runtime, and integration with the host system.  

While multi-prefix management would be nice, it's not on the todo's list.  
If you need a dedicated prefix for a Windows app, then consider packaging it as a Flatpak,
which is possible with the Flatpak Wine runtime.


## Tips & tricks

### Execute Windows binaries from the host system

See [wine-flatpak-wrapper](https://github.com/tinywrkb/pkgbuilds/tree/main/wine-flatpak-wrapper).


## TODO
* [ ] Use a shared winetricks cache. Maybe add this to the runtime, e.g. `--filesystem=xdg-cache/winetricks:Create`
* [ ] Handle xdg-data export. from the .var folder to a dedicated export folder of selected resources.
  * Possible export folders
    * `xdg-data/wine/FLATPAK_ID/{applications,desktop-directories,icons,mime}`
    * `xdg-data/applications/flatpak-FLATPAK_ID/`
* [ ] More desktop files and mimetypes for [Wine programs](https://wiki.winehq.org/List_of_Commands)
  * Control panel
  * Desktop, e.g.`explorer /desktop=shell,1920x1080`
  * Explorer
  * Internet Explorer
  * Notepad
  * Regedit
  * Wordpad
  * clock
  * cmd
  * hh
  * msiexec
  * progman
  * taskmgr
  * uninstaller
  * view
  * wineconsole
  * winefile
  * winemine
  * winhelp/winhlp32
