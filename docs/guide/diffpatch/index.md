##### :octicons-arrow-left-16: [Back to USD Animations PaiTags and Targets](../animations/paitags-and-targets.md)

# Diffing

Diffing is the process of making a JSON file
with a set of changes between the original and a modified SZS

This can be done with [Switch Theme injector](https://github.com/exelix11/SwitchThemeInjector)

![diffing.png](<diffing.png>)

the output of a diffpatch may look like the example below:

<font size="0">
<pre><code>
{
	"PatchName": "Example DIFFPATCH",
	"AuthorName": "SodaSoba",
	"TargetName": "ORIGINAL.szs",
	"ID": "123456789",
	"Files": [
		{
			"FileName": "blyt/FlcGrpList.bflyt",
			"Patches": [
				{
					"PaneName": "N_PosAll",
					"Position": {}
				},
				{
					"PaneName": "NH_Root",
					"Position": {
						"Y": -50
					}
				},
				{
					"PaneName": "N_Top",
					"Position": {
						"Y": 50
					}
				}
			],
			"Materials": [
				{
					"MaterialName": "T_00",
					"ForegroundColor": "00000000"
				}
			]
		}
	]
}
</code></pre>
</font>
this JSON (diffpatch) can be applied to a SZS file either with [Switch Theme injector](https://github.com/exelix11/SwitchThemeInjector) or with [LayoutKit](https://github.com/ThemezerNX/LayoutKit)

Here is an example by sodasoba on how a diffpatch can be applied:

# [Continue to Diffpatching](diff-example.md) :octicons-arrow-right-16:
