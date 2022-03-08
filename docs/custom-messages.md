# Custom Messages/Text/Translations

It's possible to edit any text shown in a menu by editing the strings file

## Info

The messages strings are stored in `0100000000001000\romfs\message\<lang code>\<menu>.msbt.szs`

## What You'll Need

-   qlaunch romfs files (extract firmare, extract qlaunch)
-   [Kuriimu v1](https://github.com/IcySon55/Kuriimu/releases)

## Example steps to change the eShop button label

1. Copy the `qlaunch.msbt.szs` of the language you want to edit from the qlaunch romfs (see path above)
2. Open Kuriimu and follow this path: ![image](https://cdn.discordapp.com/attachments/495784470377398282/495850689394638848/unknown1.png)
3. Pick `qlaunch.msbt.szs`
4. It will ask you where to decompress it. It will retain the "szs" in the end, but it will say decomp.szs so its unpackaged
5. Now open up the `qlaunch.msbt.decomp.szs` in Kuriimu and it should look like this screenshot (with a list of string names on the left) ![image](https://cdn.discordapp.com/attachments/495784470377398282/495850914872295424/unknown.png)
6. To change the eShop button label, go down to the ones labeled `RdtSystemTitle_Shop`
7. Change it to whatever, save it. Then repeat the "Decompress" steps but instead to Compress this time
8. Rename the compressed `.szs` to `qlaunch.msbt.szs`
9. Copy the modified `qlaunch.msbt.szs` to `SD:\atmosphere\contents\0100000000001000\romfs\message\<lang code>\qlaunch.msbt.szs`
