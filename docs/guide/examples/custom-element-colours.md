# Custom Element Colors Example

Modifying the colours of for example buttons, text, lines icons is possible.
A theme that makes use of this functionality is [Blue by Mazu/Maximum](https://themezer.net/packs/Blue-Menu-1b4). Any colour is supported and the idea is the same in every menu.

## Example Code

```json
{
	"FileName": "blyt/RdtBtnSet.bflyt",
	"Patches": [
		{
			"PaneName": "P_PictBase",
			"Visible": false
		},
		{
			"PaneName": "L_Balloon",
			"Visible": false
		},
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
```

---

These main menu elements need to be changed in the common.szs, which is applied as a patch in Theme Injector.

Footer (Bottom Line) - blyt/LineFooter.bflyt

Footer (?) - blyt/FooterAll.bflyt

Controller/Switch Icon - blyt/FooterCtrl.bflyt

Start/A/Options/+ - blyt/FooterBtn.bflyt

## Important Notes

Notes:

-   Since the color format is actually "AABBGGRR" you'll have to swap the red and blue values to get the right color. For example, the hex color code "C02BE1" would become "FFE12BC0"
-   It is currently unknown know how to change the cursor's default blue pulse color, but adding the color code to `blyt/Cursor3.bflyt` will change the secondary pulse color.

-   To hide the default circle around the menu icon:

```json
{
	"PaneName": "L_Balloon",
	"Visible": false
},
```
