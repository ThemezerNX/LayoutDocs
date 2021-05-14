##### :octicons-arrow-left-16: [Back to Getting Started](index.md)

## USD sections

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

## List of known USD sections

_TODO_

# [Continue to Animations](../diffing.md) :octicons-arrow-right-16:
