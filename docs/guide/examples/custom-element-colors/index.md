![Preview](preview.jpg)
_[Blue Menu - Home](https://themezer.net/themes/homemenu/Blue-Menu-Home-bd2) by Maxu/Maximum_

---

Modifying the colors of for example buttons, text, lines icons is possible.
A theme that makes use of this functionality is [Blue by Mazu/Maximum](https://themezer.net/packs/Blue-Menu-1b4). Any color is supported and the idea is the same in every menu.

## Example Code

```json
{
	"TargetName": "ResidentMenu.szs",
	"Files": [
		{
			"FileName": "blyt/RdtBtnSet.bflyt",
			"Patches": [
				{
					"PaneName": "P_Pict",
					"UsdPatches": [
						{
							"PropName": "C_W",
							"PropValues": ["0", "0", "0", "0"],
							"type": 1
						}
					],
					"ColorTL": "FFF2C100",
					"ColorTR": "FFF2C100",
					"ColorBL": "FFF2C100",
					"ColorBR": "FFF2C100"
				}
			],
			"Materials": [
				{
					"MaterialName": "P_Pict",
					"BackgroundColor": "FFFFFFFF"
				}
			]
		}
	]
}
```

<!-- prettier-ignore -->
!!! Important
	-   Since the color format is actually `AABBGGRR` you'll have to swap the red and blue values to get the right color. For example, the hex color code `C02BE1` would become `FFE12BC0`.

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
