## USD sections

This is a simplified of a `usd` section:

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
				"data": [0.0, 0.0, 0.0, 1.0] // note that this is not rgba
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

## List of known USD sections

# [Continue to Animations](../animations/index.md) :octicons-arrow-right-16:
