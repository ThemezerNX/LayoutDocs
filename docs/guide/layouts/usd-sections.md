##### :octicons-arrow-left-16: [Back to Getting Started](index.md)

# USD Sections

This is a simplified example of a pane followed by a `usd` section:

```json
{
	"pic1 - P_Item": {
		"name": "P_Item",
		"x translation": 100.0,
		"y translation": 100.0,
		"width": 50.0,
		"height": 50.0,
		"material": "P_Item"
	},
	"usd1 - P_Item": {
		"entries": [
			{
				"name": "S_DropShadowDrawMode",
				"type": 1,
				"unk1": 0,
				"data": [1]
			},
			{
				"name": "S_DropShadowColor",
				"type": 2,
				"unk1": 0,
				"data": [0.0, 0.0, 0.0, 1.0]
			},
			{
				"name": "S_DropShadowAngle",
				"type": 2,
				"unk1": 0,
				"data": [1.5]
			},
			{
				"name": "S_DropShadowDistance",
				"type": 2,
				"unk1": 0,
				"data": [0.0]
			}
		]
	}
}
```

<!-- prettier-ignore -->
!!! Info
	The JSON code shown above is from 3DSKit and cannot be directly copied to a layout.

## Structure

A USD entry has a `name`, Type, `unk1` and Data section.

Name: `String`  
Type: `Int`

-   `0`: String
-   `1`: Int
-   `2`: Float

Unk1: _unknown, always `0`_  
Data: Array of values of specified type

## List of known USD sections

These are the USD sections found throughout the home menu. They cannot be applied to every pane.

### Color-related

---

#### **`C_W`**

A property that is used to give elements certain colors. These colors are dynamic and can change based on the system theme.
Used almost everywhere (all menus have to support dark and light theme).

Type: `1 Data: `[X, X, X, X]` Often only the first`X`is different from`0`. Sometimes multiple `X`s are non-zero, but changing them to `0` seems to have no effect on appearance.

##### Example

```json
{
	"name": "C_W",
	"type": 1,
	"unk1": 0,
	"data": [5, 0, 0, 0]
}
```

##### Tested values

<div class="color-table" markdown="1">

| Value | Light theme                   | Dark theme    | Usage                                |
| ----- | ----------------------------- | ------------- | ------------------------------------ |
| 0     | white (255,255,255)           | (255,255,255) |                                      |
| 1     | white (255,255,255)           | (29,32,37)    |                                      |
| 2     | black (0,0,0)                 | (0,0,0)       |                                      |
| 3     | green (114,201,0)             | (149,231,0)   |                                      |
| 4     | white (255,255,255)           | (255,255,255) |                                      |
| 5     | white (235,235,235)           | (45,45,45)    | Light/dark theme bg                  |
| 6     | white (255,255,255)           | (67,67,67)    |                                      |
| 7     | white (255,255,255)           | (98,99,103)   |                                      |
| 8     | white (255,255,255)           | (31,32,34)    |                                      |
| 9     | dark grey (45,45,45)          | (255,255,255) | Controller indicator and text color  |
| 10    | blue (50,80,240)              | (0,255,201)   |                                      |
| 11    | white (255,255,255)           | (31,32,34)    |                                      |
| 12    | grey (128,128,128)            | (160,160,160) |                                      |
| 13    | white (255,255,255)           | (45,45,45)    |                                      |
| 14    | white (255,255,255)           | (45,45,45)    |                                      |
| 15    | white (255,255,255)           | (70,70,70)    |                                      |
| 16    | green (114,201,0)             | (149,231,0)   |                                      |
| 17    | green (114,201,0)             | (200,255,0)   |                                      |
| 18    | blue (50,80,240)              | (0,255,201)   |                                      |
| 19    | light blue (110,191,225)      | (0,151,130)   |                                      |
| 20    | white (255,255,255)           | (45,45,45)    |                                      |
| 21    | grey/blue (129,140,160)       | (160,180,179) |                                      |
| 22    | green (114,201,0)             | (180,255,0)   |                                      |
| 23    | green (140,241,0)             | (101,170,0)   |                                      |
| 24    | red (240,19,0)                | (255,40,0)    |                                      |
| 25    | green (0,160,0)               | (180,255,0)   |                                      |
| 26    | white (255,255,255)           | (255,255,255) |                                      |
| 27    | pink (255,40,91)              | (255,250,0)   |                                      |
| 28    | grey (128,128,128)            | (200,200,200) |                                      |
| 29    | neon blue (192,119,193)       | (25,214,210)  | Cursor                               |
| 30    | light neon blue (112,255,231) | (131,250,255) |                                      |
| 31    | white (255,255,255)           | (80,80,80)    | System Applets circle background     |
| 32    | magenta (255,0,255)           | (255,0,255)   |                                      |
| 33    | green/blue (87,255,219)       | (157,255,251) |                                      |
| 34    | grey (110,120,121)            | (220,220,220) |                                      |
| 35    | blue/grey-ish (129,140,160)   | (160,180,179) |                                      |
| 36    | white (235,235,235)           | (22,22,22)    |                                      |
| 37    | blue (7,163,203)              | (42,125,193)  |                                      |
| 38    | blue (18,189,207)             | (2,136,199)   | Cursor                               |
| 39    | dark blue (15,89,114)         | (24,51,70)    |                                      |
| 40    | light blue (29,241,255)       | (0,220,225)   |                                      |
| 41    | light blue (29,241,255)       | (0,220,255)   | Blue highlight touch                 |
| 42    | light blue (0,190,200)        | (24,189,255)  | Game text                            |
| 43    | blue-ish (0,190,200)          | (24,189,255)  |                                      |
| 44    | white (240,240,240)           | (70,70,70)    |                                      |
| 45    | grey (255,255,255)            | (119,119,119) | Player select plate background       |
| 46    | magenta (255,0,255)           | (255,0,255)   |                                      |
| 47    | white (255,255,255)           | (90,90,90)    |                                      |
| 48    | dark blue (16,13,68)          | (0,0,0)       |                                      |
| 49    | blue (50,80,240)              | (0,255,201)   |                                      |
| 50    | white (255,255,255)           | (45,45,45)    |                                      |
| 51    | white (255,255,255)           | (0,61,140)    |                                      |
| 52    | white (235,235,235)           | (45,45,45)    |                                      |
| 53    | grey (190,190,190)            | (190,190,190) |                                      |
| 54    | white (240,240,240)           | (70,70,70)    |                                      |
| 55    | green (0,200,0)               | (180,255,0)   |                                      |
| 56    | green (140,240,28)            | (101,170,0)   |                                      |
| 57    | green (0,170,0)               | (180,255,0)   |                                      |
| 58    | dark grey (45,45,45)          | (255,255,255) | Lockscreen home icon                 |
| 59    | white (255,255,255)           | (45,45,45)    |                                      |
| 60    | grey (200,200,200)            | (120,120,120) |                                      |
| 61    | magenta (255,0,255)           | (255,0,255)   |                                      |
| 62    | dark grey (45,45,45)          | (83,87,86)    | Lockscreen three dots when unlocking |
| 63    | white (255,255,255)           | (29,32,37)    |                                      |
| 64    | dark blue (19,29,90)          | (0,0,0)       |                                      |
| 65    | green/blue (0,91,186)         | (46,161,205)  | Cursor                               |
| 66    | blue (90,190,255)             | (0,255,201)   |                                      |
| 67    | black (35,35,35)              | (45,45,45)    |                                      |
| 68    | grey (114,114,114)            | (200,200,200) |                                      |
| 69    | white (255,255,255)           | (45,45,45)    |                                      |
| 70    | grey (200,200,200)            | (170,170,170) |                                      |
| 71    | grey (45,45,45)               | (255,255,255) |                                      |
| 72    | magenta (255,0,255)           | (0,0,0)       |                                      |
| 73    | white (255,255,255)           | (45,45,45)    |                                      |
| 74    | grey (128,128,128)            | (190,190,190) |                                      |
| 75    | white (255,255,255)           | (255,255,255) |                                      |
| 76    | white (255,255,255)           | (45,45,45)    |                                      |
| 77    | blue (50,80,240)              | (0,255,201)   |                                      |
| 78    | magenta (255,0,255)           | (255,0,255)   |                                      |
| 79    | white (255,255,255)           | (45,45,45)    |                                      |
| 80    | blue (110,191,255)            | (0,151,130)   |                                      |
| 81    | blue/grey-ish (129,140,160)   | (160,180,179) |                                      |
| 82    | bright orange (240,19,0)      | (255,40,0)    |                                      |
| 83    | white (255,255,255)           | (56,61,67)    |                                      |
| 84    | white (255,255,255)           | (255,255,255) |                                      |
| 85    | grey (201,201,201)            | (255,255,255) |                                      |
| 86    | white (255,255,255)           | (56,61,67)    |                                      |
| 87    | dark blue (19,29,90)          | (0,0,0)       |                                      |
| 88    | red (255,59,69)               | (250,89,60)   | Notification applet                  |
| 89    | soft orange (255,140,65)      | (255,140,65)  |                                      |
| 90    | orange (255,160,0)            | (255,176,0)   | eShop applet                         |
| 91    | grey (45,45,45)               | (255,255,255) |                                      |
| 92    | blue (19,115,254)             | (30,160,255)  | Album applet                         |
| 93    | blue (0,162,195)              | (49,231,255)  |                                      |
| 94    | blue (60,160,255)             | (0,255,201)   |                                      |
| 95    | magenta (255,0,255)           | (255,0,255)   |                                      |
| 96    | white (255,255,255)           | (30,19,59)    |                                      |
| 97    | light blue (110,201,255)      | (99,255,231)  |                                      |
| 98    | (101,116,147)                 | (160,180,197) |                                      |
| 99    | green (140,241,0)             | (200,255,0)   |                                      |
| 100   | grey (128,128,128)            | (80,80,80)    |                                      |
| 101   | orange (255,140,65)           | (255,140,65)  |                                      |
| 102   | white (255,255,255)           | (255,255,255) |                                      |
| 103   | grey (190,190,190)            | (90,90,90)    |                                      |
| 104   | white (255,255,255)           | (180,180,180) |                                      |
| 105   | grey (154,154,154)            | (140,140,140) |                                      |
| 106   | grey (45,45,45)               | (255,255,255) |                                      |
| 107   | grey (148,148,148)            | (160,160,160) |                                      |
| 108   | grey (128,128,128)            | (190,190,190) |                                      |
| 109   | pink/orange (255,40,91)       | (255,250,0)   |                                      |
| 110   | magenta (255,0,255)           | (255,0,255)   |                                      |
| 111   | magenta (255,0,255)           | (255,0,255)   |                                      |
| 112   | magenta (255,0,255)           | (255,0,255)   |                                      |
| 113   | blue (50,80,240)              | (0,255,201)   |                                      |
| 114   | blue (50,80,240)              | (0,255,201)   |                                      |
| 115   | light green/blue (79,255,206) | (47,239,244)  |                                      |
| 116   | green (114,201,0)             | (180,255,0)   |                                      |
| ≥117  | black (0,0,0)                 | black (0,0,0) |                                      |

</div>

---

#### **`C_B`**

_Functionality unsure_

Used to give elements certain colors?
Doesn't really seem to do much. Seems to be used in e.g. cursor: is set to 37 somewhere.

Type: `1`  
Data: `[X, X, X, X]`

##### Example

```json
{
	"name": "C_B",
	"type": 1,
	"unk1": 0,
	"data": [0, 0, 0, 0]
}
```

---

#### **`C_Id`**

_Functionality unknown_

Color doesn't change when C_W is set to another color -> C_Id probably 'overlaps' C_W.
System theme color has almost no effect (except for DATA: 0 ('off') and 42 so far).
All stuff here was tested on the lockscreen, and does vary per menu.

Type: `1`  
Data: `[X]`

##### Example

```json
{
	"name": "C_Id",
	"type": 1,
	"unk1": 0,
	"data": [0]
}
```

##### Tested values

<div class="color-table" markdown="1">

| Value | Light theme                | Comments                                      |
| ----- | -------------------------- | --------------------------------------------- |
| 0     | white                      | default - probably 'off'                      |
| 1     | white                      |                                               |
| 2     | white                      |                                               |
| 3     | white                      |                                               |
| 4     | black                      |                                               |
| 5     | black                      |                                               |
| 6     | black                      |                                               |
| 7     | black                      |                                               |
| 8     | dark blue (19,29,90)       |                                               |
| 9     | black                      |                                               |
| 10    | grey                       |                                               |
| 11    | black                      |                                               |
| 12    | blue-purpleish (50,80,240) |                                               |
| 13    | blue-purpleish (50,80,240) |                                               |
| 14    | white                      |                                               |
| 15    | ligher grey                | Seems to overlap the entrance homebutton icon |
| 16    | white                      |                                               |
| 17    | white                      |                                               |
| 18    | white                      |                                               |
| 19    | black                      |                                               |
| 20    | white                      |                                               |
| 42    | grey                       | dark theme: white                             |

</div>

---

#### **`C_TI`**

_Functionality unknown_

Type: `1`  
Data: `[X]`

##### Example

```json
{
	"name": "C_Ti",
	"type": 1,
	"unk1": 0,
	"data": [0]
}
```

##### Tested values

| Value       | Comments |
| ----------- | -------- |
| 0           | nothing  |
| 1           | nothing  |
| 10          | nothing  |
| 99999999999 | freezes  |

---

### Border

#### **`S_RoundRadius`**

Changes the border radius of picture(!) panels.
Percentage/pixels?

Type: `2`  
Data: `[X]`

##### Example

```json
{
	"name": "S_RoundRadius",
	"type": 2,
	"unk1": 0,
	"data": [50.0]
}
```

---

#### **`S_BorderDrawMode`**

_Functionality unknown_

There are different drawmodes

Type: `1`  
Data: `[X]`  
Common value: `1`  
Example usage: `Cursor3`

##### Example

```json
{
	"name": "S_BorderDrawMode",
	"type": 1,
	"unk1": 0,
	"data": [1]
}
```

---

#### **`S_BorderVolume`**

Color intensity of the border.

Type: `2`  
Data: `[X]`  
Example usage: `Cursor3`

##### Example

```json
{
	"name": "S_BorderVolume",
	"type": 2,
	"unk1": 0,
	"data": [1.5]
}
```

---

#### **`S_BorderSize`**

Width of the border in pixels.

Type: `2`  
Data: `[X]`  
Example usage: `Cursor3`

##### Example

```json
{
	"name": "S_BorderSize",
	"type": 2,
	"unk1": 0,
	"data": [5.0]
}
```

---

#### **`S_BorderColorSelect0`**

_Functionality unknown_

Another kind of color. Used in the Cursor and has the same value for `C_W` somewhere in the cursor.

Type: `1`  
Data: `[X]`  
Example usage: `Cursor3`

##### Example

```json
{
	"name": "S_BorderColorSelect0",
	"type": 1,
	"unk1": 0,
	"data": [1]
}
```

---

#### **`S_BorderColor0`**

_Functionality unknown_

Yet another kind of color.

Type: `2`  
Data: `[X, X, X, X]`  
Common value: `[1.0, 1.0, 1.0, 1.0]`  
Example usage: `Cursor3`

##### Example

```json
{
	"name": "S_BorderColor0",
	"type": 2,
	"unk1": 0,
	"data": [5.0, 0, 0, 0]
}
```

---

### Drop Shadow

#### **`S_DropShadowDrawMode`**

_Functionality unknown_

There are different drawmodes.

Type: `1`  
Data: `[X]`  
Common value: `1`  
Example usage: `RdtBtnIconGame`

##### Example

```json
{
	"name": "S_DropShadowDrawMode",
	"type": 1,
	"unk1": 0,
	"data": [1]
}
```

---

#### **`S_DropShadowVolume`**

Color density of the shadow.

Type: `2`  
Data: `[X]`  
Example usage: `RdtBtnIconGame`

##### Example

```json
{
	"name": "S_DropShadowVolume",
	"type": 2,
	"unk1": 0,
	"data": [5.0]
}
```

---

#### **`S_DropShadowColorSelect`**

_Functionality unsure_
Color of the border, same values as C_W?

Type: `1`  
Data: `[X]`  
Example usage: `RdtBtnIconGame`

##### Example

```json
{
	"name": "S_DropShadowColorSelect",
	"type": 1,
	"unk1": 0,
	"data": [1]
}
```

---

#### **`S_DropShadowColor`**

Color of the drop shadow.

Type: `2`  
Data: `[X, X, X, X]`  
Common value: `[0.0, 0.0, 0.0, 1.0]` (R, G, B, A)?
Example usage: `RdtBtnIconGame`

##### Example

```json
{
	"name": "S_DropShadowColor",
	"type": 2,
	"unk1": 0,
	"data": [0.0, 0.0, 0.0, 1.0]
}
```

---

#### **`S_DropShadowAngle`**

Shadow direction in radians.

Type: `2`  
Data: `[X]`  
Example usage: `RdtBtnIconGame`

##### Example

```json
{
	"name": "S_DropShadowAngle",
	"type": 2,
	"unk1": 0,
	"data": [1.5]
}
```

##### Tested values

The first table is probably correct, but the second table is here just in case.

| Value         | Direction | Comment                                                    |
| ------------- | --------- | ---------------------------------------------------------- |
| 0             | right     |                                                            |
| 1.57079632679 | down      | GameIcon shadows are down, right? If yes, this is correct. |
| 3.14159265359 | left      |                                                            |
| 4.71238898038 | up        |                                                            |

OR

| Value         | Direction |
| ------------- | --------- |
| 0             | up        |
| 1.57079632679 | right     |
| 3.14159265359 | down      |
| 4.71238898038 | right     |

---

#### **`S_DropShadowDistance`**

Shadow fade/blur distance in pixels.

Type: `2`  
Data: `[X]`  
Example usage: `RdtBtnIconGame`

##### Example

```json
{
	"name": "S_DropShadowDistance",
	"type": 2,
	"unk1": 0,
	"data": [5.2]
}
```

---

#### **`S_DropShadowSize`**

Shadow width in pixels.

Type: `2`  
Data: `[X]`  
Example usage: `RdtBtnIconGame`

##### Example

```json
{
	"name": "S_DropShadowSize",
	"type": 2,
	"unk1": 0,
	"data": [10.0]
}
```

---

#### **`S_DropShadowFunction`**

_Functionality unsure_
How the `S_DropShadowDistance` is drawn. For example, blur or solid?

Type: `1`  
Data: `[X]`  
Common value: `5` and `4`
Example usage: `RdtBtnIconGame`

##### Example

```json
{
	"name": "S_DropShadowFunction",
	"type": 1,
	"unk1": 0,
	"data": [5]
}
```

---

#### **`S_DropShadowKnockout`**

_Functionality unsure_
Enables/disables shadow fading?

Type: `1`  
Data: `[X]`  
Common value: `1`
Example usage: `RdtBtnIconGame`

##### Example

```json
{
	"name": "S_DropShadowKnockout",
	"type": 1,
	"unk1": 0,
	"data": [1]
}
```

# [Continue to Animations](../diffing.md) :octicons-arrow-right-16:
