##### :octicons-arrow-left-16: [Back to Menu Files](menu-files.md)

# Filetypes

This page contains a list of all filetypes related to custom layouts and theming.

## SZS Files

`SZS` files are archives with a custom compression algorithm.
They are actually `SARC` (aka `ARC`) files. The compression algorithm that is used is Yaz0.

### Structure

The structure of a menu `SZS` file is generally the same:

```
๐ฆResidentMenu_11.0.1_original
โฃ ๐anim
โ โ ๐[filename].bflan
โฃ ๐bgsh
โ โฃ ๐__ArchiveShader.bnsh
โ โ ๐__ArchiveShader.bushvt
โฃ ๐blyt
โ โ ๐[filename].bflyt
โ ๐timg
  โ ๐__Combined.bntx
```

The folders contain the following:

-   `anim`: Animation files (`.bflan`)
-   `bgsh`: GPU shaders (`.bnsh`, `.bushvt`)
-   `blyt`: Layout files (`.bflyt`)
-   `timg`: Menu images (`.bntx`)

For custom layouts we only touch the files in `anim` and `blyt`. However, it is interesting to note that the NXTheme Installer internally injects the [nxtheme](../definitions.md#nxtheme) background image in the `__Combined.bntx` file.

#### bflan Files

`bflan` files, or _'**B**inary ca**F**e **L**ayout **AN**imation'_ files,

#### bflyt Files

`bflyt` files, or _'**B**inary ca**F**e **L**a**Y**ou**T**'_ files,

# [Continue to Layouts](layouts/index.md) :octicons-arrow-right-16:
