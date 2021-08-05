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

## Example Code for all Home Menu elements

For this, you have to replace `AABBGGRR` with the color you want. Most editors allow you to replace multiple occurrences at once.

```json
{
	"TargetName": "ResidentMenu.szs",
	"Files": [
		{
			"FileName": "blyt/RdtBtnCtrl.bflyt",
			"Patches": [
				{
					"PaneName": "P_Form",
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
				},
				{
					"PaneName": "P_Stick",
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
				},
				{
					"PaneName": "P_Y",
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
				},
				{
					"PaneName": "P_X",
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
				},
				{
					"PaneName": "P_A",
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
				},
				{
					"PaneName": "P_B",
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
					"MaterialName": "P_Form",
					"BackgroundColor": "FFFFFFFF"
				},
				{
					"MaterialName": "P_B",
					"BackgroundColor": "FFFFFFFF"
				},
				{
					"MaterialName": "P_A",
					"BackgroundColor": "FFFFFFFF"
				},
				{
					"MaterialName": "P_X",
					"BackgroundColor": "FFFFFFFF"
				},
				{
					"MaterialName": "P_Y",
					"BackgroundColor": "FFFFFFFF"
				},
				{
					"MaterialName": "P_Stick",
					"BackgroundColor": "FFFFFFFF"
				}
			]
		},
		{
			"FileName": "blyt/HudTime.bflyt",
			"Patches": [
				{
					"PaneName": "P_A",
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
				},
				{
					"PaneName": "P_M",
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
				},
				{
					"PaneName": "P_P",
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
				},
				{
					"PaneName": "P_Colon",
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
				},
				{
					"PaneName": "P_Dot",
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
				},
				{
					"PaneName": "P_Comma",
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
			]
		},
		{
			"FileName": "blyt/RdtBtnFullLauncher.bflyt",
			"Patches": [
				{
					"PaneName": "P_Pict_00",
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
				},
				{
					"PaneName": "P_Pict_01",
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
				},
				{
					"PaneName": "P_Pict_02",
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
				},
				{
					"PaneName": "P_Pict_03",
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
			]
		},
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
					"ColorTL": "AABBGGRR",
					"ColorTR": "AABBGGRR",
					"ColorBL": "AABBGGRR",
					"ColorBR": "AABBGGRR"
				}
			],
			"Materials": [
				{
					"MaterialName": "P_Pict",
					"BackgroundColor": "FFFFFFFF"
				}
			]
		},
		{
			"FileName": "blyt/RdtBtnPvr.bflyt",
			"Patches": [
				{
					"PaneName": "P_PictMask",
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
				},
				{
					"PaneName": "P_Pict_01",
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
				},
				{
					"PaneName": "P_Color",
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
				},
				{
					"PaneName": "P_Pict_00",
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
				},
				{
					"PaneName": "P_Effect",
					"UsdPatches": [
						{
							"PropName": "C_W",
							"PropValues": ["34", "0", "0", "0"],
							"type": 1
						}
					]
				}
			],
			"Materials": [
				{
					"MaterialName": "P_Pict_00",
					"BackgroundColor": "FFFFFFFF"
				},
				{
					"MaterialName": "P_Pict_01",
					"BackgroundColor": "FFFFFFFF"
				}
			]
		},
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
				},
				{
					"PaneName": "L_GTNum_00",
					"UsdPatches": [
						{
							"PropName": "C_W",
							"PropValues": ["0", "0", "0", "0"],
							"type": 1
						}
					]
				},
				{
					"PaneName": "L_GTNum_01",
					"UsdPatches": [
						{
							"PropName": "C_W",
							"PropValues": ["0", "0", "0", "0"],
							"type": 1
						}
					]
				},
				{
					"PaneName": "L_GTNum_02",
					"UsdPatches": [
						{
							"PropName": "C_W",
							"PropValues": ["0", "0", "0", "0"],
							"type": 1
						}
					]
				}
			],
			"Materials": [
				{
					"MaterialName": "P_Per",
					"BackgroundColor": "FFFFFFFF"
				},
				{
					"MaterialName": "P_GTNum_00",
					"BackgroundColor": "FF8080FF"
				},
				{
					"MaterialName": "P_GTNum_00",
					"BackgroundColor": "FF8080FF"
				},
				{
					"MaterialName": "P_GTNum_00",
					"BackgroundColor": "FF8080FF"
				}
			]
		},
		{
			"FileName": "blyt/HudSignal.bflyt",
			"Patches": [
				{
					"PaneName": "P_Plane",
					"UsdPatches": [
						{
							"PropName": "C_W",
							"PropValues": ["0", "0", "0", "0"],
							"type": 1
						}
					],
					"ColorTL": "FF8080FF",
					"ColorTR": "FF8080FF",
					"ColorBL": "FF8080FF",
					"ColorBR": "FF8080FF"
				},
				{
					"PaneName": "P_Wifi",
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
				},
				{
					"PaneName": "P_Local",
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
				},
				{
					"PaneName": "P_WireLine",
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
			]
		},
		{
			"FileName": "blyt/RdtBtnNtf.bflyt",
			"Patches": [
				{
					"PaneName": "P_PictNtf_00",
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
				},
				{
					"PaneName": "P_PictNtf_01",
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
				},
				{
					"PaneName": "P_Effect",
					"UsdPatches": [
						{
							"PropName": "C_W",
							"PropValues": ["34", "0", "0", "0"],
							"type": 1
						}
					]
				}
			],
			"Materials": [
				{
					"MaterialName": "P_PictNtf_00",
					"BackgroundColor": "FFFFFFFF"
				},
				{
					"MaterialName": "P_PictNtf_01",
					"BackgroundColor": "FFFFFFFF"
				}
			]
		},
		{
			"FileName": "blyt/RdtBtnShop.bflyt",
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
					"ColorTL": "AABBGGRR",
					"ColorTR": "AABBGGRR",
					"ColorBL": "AABBGGRR",
					"ColorBR": "AABBGGRR"
				},
				{
					"PaneName": "P_Effect",
					"UsdPatches": [
						{
							"PropName": "C_W",
							"PropValues": ["34", "0", "0", "0"],
							"type": 1
						}
					]
				}
			],
			"Materials": [
				{
					"MaterialName": "P_Pict",
					"BackgroundColor": "FFFFFFFF"
				}
			]
		},
		{
			"FileName": "blyt/RdtBtnPow.bflyt",
			"Patches": [
				{
					"PaneName": "P_Pict_00",
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
				},
				{
					"PaneName": "P_Pict_01",
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
					"MaterialName": "P_Pict_00",
					"BackgroundColor": "FFFFFFFF"
				},
				{
					"MaterialName": "P_Pict_01",
					"BackgroundColor": "FFFFFFFF"
				}
			]
		},
		{
			"FileName": "blyt/BatteryConsole.bflyt",
			"Patches": [
				{
					"PaneName": "P_Ico00",
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
				},
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
				},
				{
					"PaneName": "P_BatBase",
					"Visible": false
				},
				{
					"PaneName": "P_Charge",
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
				},
				{
					"PaneName": "P_Error",
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
				},
				{
					"PaneName": "P_GaugeNml",
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
				},
				{
					"PaneName": "P_GaugeOther",
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
			]
		},
		{
			"FileName": "blyt/GTNumL.bflyt",
			"Patches": [
				{
					"PaneName": "P_GTNum_00",
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
					"MaterialName": "P_GTNum_00",
					"BackgroundColor": "FFFFFFFF"
				}
			]
		},
		{
			"FileName": "blyt/GTNumM.bflyt",
			"Patches": [
				{
					"PaneName": "P_GTNum_00",
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
					"MaterialName": "P_GTNum_00",
					"BackgroundColor": "FFFFFFFF"
				}
			]
		}
	]
}
```

---

_Credits to Mazu/Maxim and Exelix_
