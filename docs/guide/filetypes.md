##### :octicons-arrow-left-16: [Back to Menu Files](menu-files.md)

# Filetypes

This page contains a list of all filetypes related to custom layouts and theming.

## SZS Files

`SZS` files are archives with a custom compression algorithm.
They are actually `SARC` (aka `ARC`) files. The compression algorithm that is used is Yaz0.

### Structure

The structure of a menu `SZS` file is generally the same:

```
📦ResidentMenu_11.0.1_original
┣ 📂anim
┃ ┗ 📜[filename].bflan
┣ 📂bgsh
┃ ┣ 📜__ArchiveShader.bnsh
┃ ┗ 📜__ArchiveShader.bushvt
┣ 📂blyt
┃ ┗ 📜[filename].bflyt
┗ 📂timg
  ┗ 📜__Combined.bntx
```

The folders contain the following:

- `anim`: Animation files (`.bflan`)
- `bgsh`: GPU shaders (`.bnsh`, `.bushvt`)
- `blyt`: Layout files (`.bflyt`)
- `timg`: Menu images (`.bntx`)

For custom layouts we only touch the files in `anim` and `blyt`. However, it is interesting to note that the NXTheme
Installer internally injects the [nxtheme](../definitions.md#nxtheme) background image in the `__Combined.bntx` file.

### Filetypes

Nintendo has been using its own formats to design menus, animations and shaders, often stored in these (s)arc archives.
Heres a table of some formats that have emerged throughout the years:

| Console                                           | Format    | Description                                          | Extra Docs and Resources                                                                                                                                                                                                                 |
|---------------------------------------------------|-----------|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Wii (Rev/**R**evolution)                          | `(b)rlyt` | (**B**inary) **R**evolution **L**a**Y**ou**T**       |                                                                                                                                                                                                                                          |
|                                                   | `(b)rlan` | (**B**inary) **R**evolution **L**ayout **AN**imation |                                                                                                                                                                                                                                          |
| DS (NTR/Nitro)                                    | -         | -                                                    |                                                                                                                                                                                                                                          |
| 3DS (**C**TR)                                     | `(b)clyt` | (**B**inary) **C**TR **L**a**Y**ou**T**              |                                                                                                                                                                                                                                          |
|                                                   | `(b)clan` | (**B**inary) **C**TR **L**ayout **AN**imation        |                                                                                                                                                                                                                                          |
| Wii U (**C**afe), but also used by 3DS and Switch | `(b)flyt` | (**B**inary) ca**F**e **L**a**Y**ou**T**             | [Switch Toolbox](https://github.com/KillzXGaming/Switch-Toolbox/blob/c9e74e0be114885f347789f3bd348baccacf0842/File_Format_Library/FileFormats/Layout/CAFE/BFLYT.cs), [3DSkit](https://github.com/Tyulis/3DSkit/blob/master/doc/BFLYT.md) |
|                                                   | `(b)flan` | (**B**inary) ca**F**e **L**ayout **AN**imation       | [Switch Toolbox](https://github.com/KillzXGaming/Switch-Toolbox/blob/c9e74e0be114885f347789f3bd348baccacf0842/File_Format_Library/FileFormats/Layout/CAFE/BFLAN.cs), [3DSkit](https://github.com/Tyulis/3DSkit/blob/master/doc/BFLAN.md) |
| Switch (NX)                                       | `(b)ntx`  | (**B**inary) **N**x **T**e**X**ture                  | [Switch Toolbox](https://github.com/KillzXGaming/Switch-Toolbox/blob/c9e74e0be114885f347789f3bd348baccacf0842/File_Format_Library/FileFormats/Texture/BNTX.cs), [3DSkit](https://github.com/Tyulis/3DSkit/blob/master/doc/BNTX.md)       |

(If you're interested in more Nintendo device codenames, check
out [this page](https://salty-salty-studios.com/shiz/misc/codenames.html))

All these formats are based on the same underlying format, but simply use different names for different consoles.
The underlying format simply goes through several versions. For example, `BFLAN` appears as version such as 7.1.0/7.2.1
on 3DS and
8.6.0 on Switch.

There are a lot more file formats used in all these systems. For a comprehensive list, check
out [this folder on github](https://github.com/KillzXGaming/Switch-Toolbox/tree/master/File_Format_Library/FileFormats),
which can at least give you an idea of all the different formats. Actual documentation will have to be searched for
elsewhere.

Check out these wikis for more information on all kinds of Nintendo file formats:
- [Deep Sea Knowledge/OatMealDome Wiki](https://wiki.oatmealdome.me/Category:File_formats)
- [3DBrew](https://www.3dbrew.org/wiki/Category:File_formats)
- [Custom Mario Kart Wiiki](https://wiki.tockdom.com/wiki/List_of_File_Formats)
- [Switchbrew](https://switchbrew.org/)


### **[Continue to Layouts (bflyt)](layouts/index.md) :octicons-arrow-right-16:**

### **[Continue to Animations (bflan)](animations/index.md) :octicons-arrow-right-16:**