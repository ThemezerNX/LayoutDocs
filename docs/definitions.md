# Definitions

This page tries to explain as much of the theming jargon as possible.

## Word List

### SZS

An archive. In the Switch's menu files it contains the layout files, animations and textures. [_More Info_](guide/filetypes.md#szs-files)

### Applet

A kind of title/app/game. `Qlaunch`, `playerSelect`, `photoViewer` are all applets. [_More Info_](guide/menu-files.md#menu-files)

### nxtheme

Unfortunately `SZS` files from the Switch's firmware files contain copyrighted data and can't be shared online. In order to still share custom themes, the `nxtheme` format was developed. An `nxtheme` file contains theme details (name, author), images and the layout.

### exelixbg

The `exelixbg` is the name of the panel that is added to the menus when injecting an image into `__Combined.bntx` file in `SZS` files.

### Diffing, Diffed JSON, Layout JSON

A layout is created by comparing a modified `SZS` file with the original unmodified one. The changes that are detected are saved in a layout `json` file, which then only contains differential data. This way, sharing `nxthemes` is completely legal.

### Panes

Another term for elements in `bflyt` files. For example `P_Pict`, `N_Button`.

### usd section

`usd` (officially called 'extended user information') is a part of the `bflyt` file that holds extra data and defines, for example, shadows, radius, etc. Panes are often followed by `usd` sections. [_More Info_](guide/layouts/usd-sections.md)

### Sysupdate

Short for system update
