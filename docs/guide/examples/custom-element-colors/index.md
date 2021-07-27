![Preview](preview.jpg)  
_[Blue Menu - Home](https://themezer.net/themes/homemenu/Blue-Menu-Home-bd2) by Maxu/Maximum_

---

Modifying the colors of for example buttons, text, lines icons is possible.
A theme that makes use of this functionality is [Blue by Mazu/Maximum](https://themezer.net/packs/Blue-Menu-1b4). Any color is supported.

<!-- prettier-ignore -->
!!! Tip
	Custom colors can be mixed with [custom applet icons](../custom-applet-icons/index.md).

## Example Code

Let's say you want the album icon to be red (`#FF0000`). The following example shows how to do that:

```json
{
	"TargetName": "ResidentMenu.szs",
	"Files": [
		{
			"FileName": "blyt/RdtBtnPvr.bflyt",
			"Patches": [
				{
					"PaneName": "P_Pict",
					"UsdPatches": [
						{
							"PropName": "C_W",
							"PropValues": ["0", "0", "0", "0"], // don't change this!
							"type": 1
						}
					],
					"ColorTL": "FF0000FF", // set your custom color in these four fields
					"ColorTR": "FF0000FF",
					"ColorBL": "FF0000FF",
					"ColorBR": "FF0000FF"
				}
			],
			"Materials": [
				{
					"MaterialName": "P_Pict",
					"BackgroundColor": "FFFFFFFF" // don't change this!
				}
			]
		}
	]
}
```

<!-- prettier-ignore -->
!!! Important
	-   Since the color format is actually `AABBGGRR` (alpha, blue, green, red) you'll have to use an inverse version of the normal hex color. For example, the hex color code `FF0000` (rgb)/`FFFF0000` (argb) would become `FF0000FF` (abgr).

<!-- prettier-ignore -->
!!! Info
	-   It is currently unknown how exactly to change the cursor's default blue pulse color, but `P_Grow` and `P_Main` in `Cursor3.bflyt` contain color codes. Changing these will change the secondary pulse color. The primary pulse color is probabily a combination of these panes and their [`usd` sections](../../../definitions.md#usd-section).

---

## Specific Examples

### Battery Percent sign

```json
{
	"FileName": "blyt/HudBatteryNum.bflyt",
	"Patches": [
		{
			"PaneName": "P_Per",
			"UsdPatches": [
				{
					"PropName": "C_W",
					"PropValues": ["0", "0", "0", "0"],
					"type": 1
				}
			],
			"ColorTL": "AABBGGRR",
			"ColorTR": "AABBGGRR",
			"ColorBL": "AABBGGRR",
			"ColorBR": "AABBGGRR"
		}
	],
	"Materials": [
		{
			"MaterialName": "P_Per",
			"BackgroundColor": "FFFFFFFF"
		}
	]
}
```

---

_Credits to Mazu/Maxim and Exelix_
