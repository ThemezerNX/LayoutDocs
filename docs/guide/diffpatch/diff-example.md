##### :octicons-arrow-left-16: [Back to What is Diffing](index.md)

# Diffpatching

This guide is an example of Diffpatching using a pre made json (diffpatch).<br> 
it was made by sodasoba to patch Option.szs to make it match his switchdeck theme.

Option.szs has to be manually patched as it's not supported by NXThemesInstaller but can be patched in [switchlayouteditor](https://github.com/FuryBaguette/SwitchLayoutEditor/releases) the patched file is then copied to `SDMC:/atmosphere/contents/0100000001000/romfs/lyt` with the other szs files

!!! cite "patched SZS locations:"
	Refer to [Menu Files](../menu-files.md) page for szs and their locations within `atmosphere/contents/<TITLEID>/romfs/lyt`

Without the patch applied this is the unedited SZS
![unpatched](<00opt.jpg>)

similar to the example on the [diffing](index.md) page this diffpatch has settings that will change:

 * _`option.szs/blyt/Line_Root.bflyt` - Removed_
 * _`option.szs/blyt/OptMain.bflyt` - Background color theme matched & icon resized_
 * _`option.szs/blyt/BgPlate.bflyt` - Background color_
 * _`option.szs/blyt/OptNav.bflyt` - Moved down_
 * _`option.szs/blyt/LineHeader_Root.bflyt` Removed_
 * _`option.szs/blyt/BgNav_Root.bflyt` - Background color / darker_

after the diffpatch is applied the Option.szs will now look like this
![patched](<01opt.png>)

NXThemesInstaller extracts szs files on your switch SD card to the location: `SDMC:/themes/systemData/` Locate your version of _Option.szs_

![SDMC](<01-sdmc.png>)

Make a copy of Option.szs to your computer then download and extract the diffpatch

[Option-diffpatch-for-switchdeck.zip](Option-diffpatch-for-switchdeck.zip)

Open switchlayouteditor and open option.szs or drag option.szs into the switchlayouteditor

![loadszs](<04-load-option.png>)


once option.szs is open a smaller window will open, we only need to load our diffpatch and not actually edit anything in this example but you could load a diffpatch and use it as a base point for themeing.

Click `Tools` > `Load JSON patch`

![unpatched](<05-load-diff-switchdeck.png>)


locate the diffpatch you want to apply on your computer and open it

![unpatched](<6-open-diff-switchdeck.png>)

once it's loaded you will get a pop up stating it's loaded

![unpatched](<7-loaded-diff-switchdeck.png>)

now save the patched option.szs

by clicking `Save` > `Save`

![unpatched](<8-loaded-diff-switchdeck.png>)


paste the patched option.szs from your desktop onto the SD card

`SDMC:/atmosphere/contents/010000000001000/romfs/lyt/`

![unpatched](<9-loaded-diff-switchdeck.png>)

!!! cite "patched SZS locations:"
	Refer to [Menu Files](../menu-files.md) page for szs and their locations within `atmosphere/contents/<TITLEID>/romfs/lyt`
	
Reboot your switch and that's it.

# [Continue to Examples](../examples/index.md) :octicons-arrow-right-16: