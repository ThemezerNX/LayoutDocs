![Preview](preview.jpg)  
_Pulling panes to the front in an old version of [Careful Layout](https://themezer.net/layouts/homemenu/Careful-Layout-6) by Migush_

---

In the case that z-coordinates do not work, there is another way to pull panes to the front or push them to the back. This example shows how you can do that. It has to do with the order in which panes are listed in the `lyt` file. Panes are rendered from top to bottom in the hierary tree:

![Hierarchy tree](hierarchy-tree.jpg)

The two properties supported by the NXTheme Installer / Injector are:

-   `PushBackPanes` (array)
-   `PullFrontPanes` (array)

<!-- prettier-ignore -->
!!! Warning
    The Switch Theme Injector does not detect changes in pane positions made using the Switch Toolbox or Layout Editor. These changes must made in the final layout json **manually**!

## Example Code

This example pulls the `N_Tip` (the text) of the eShop button to the front as seen in the image at the top of the page.

```json
{
	"TargetName": "ResidentMenu.szs",
	"Files": [
		{
			"FileName": "blyt/RdtBtnShop.bflyt",
			"PushBackPanes": ["N_Tip"]
		}
	]
}
```

<!-- prettier-ignore -->
!!! Important
	Note the `PushBackPanes` instead of `PullFrontPanes`. This is correct, since internally "push back" means "push the pane back from the top to bottom".

### Before

![before.jpg](before.jpg)

### After

![After](after.jpg)
