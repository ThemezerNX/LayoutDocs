##### :octicons-arrow-left-16: [Back ResidentMenu.szs](../index.md)

#RdtBtnFullLauncher.bflyt

**File:** `ResidentMenu.szs/blyt/RdtBtnFullLauncher.bflyt`<br>
**Main `bflyt` file:** [`RdtBase.bflyt`](../RdtBase.bflyt.md)

---

## Layout of `ResidentMenu.szs/blyt/RdtBtnFullLauncher.bflyt`

<!-- prettier-ignore -->
!!! Info
    These aren't all the functions, most are unknown or the component is unimportant.
	
## Tree

-   **RootPane [pan 1]**
	-	**N_Root [pan 1]**
		-	**N_DecideKey [pan 1]**
			-	**N_DecideTouch [pan1]**
				-	**P_PicBase [pic 1]** `full launcher background color`
				-	**N_Pict [pan1]**
					-	**P_Pict_00 [pic1]** `four square icons - Top Left`
						-	**P_PictBase_00 [pic 1]
					-	**P_Pict_01 [pic1]** `four square icons - Top Right`
						-	**P_PictBase_01 [pic 1]
					-	**P_Pict_02 [pic1]** `four square icons - Bottom Left`
						-	**P_PictBase_02 [pic 1]
					-	**P_Pict_03 [pic1]** `four Square icons - Bottom Right`
						-	**P_PictBase_03 [pic 1]
				-	**N_ScaleDecide [pan 1]**
					-	**P_BtnDecideKey [pic 1]**
					-	**P_BtnTouch [pic 1]**
				-	**N_BtnFocusKey [pan 1]**
					-	**UF_Cursor [prt 1]**
		-	**N_Tip [pan 1]**
		-	**L_Balloon [prt 1]**
	-	**B_Hit [bnd 1]**

---

<!-- prettier-ignore -->
!!! Info
    Material Editing colors can be tricky, edit background colors (RGBA) `255;255;255;AAA` (Alpha 0-255 for opacity)



-	**Materials**
	-	**0: P_BtnDecideKey**
	-	**1: P_Btn_Touch**
	-	**2: T_Main**
	-	**3: P_Effect**
	-	**4: P_Pict_00**
	-	**5: P_Pict_01**
	-	**6: P_Pict_02**
	-	**7: P_Pict_03**
	-	**8: P_PictBase_00**
	-	**9: P_PictBase_01**
	-	**10: P_PictBase_02**
	-	**11: P_PictBase_03**
	-	**12: P_PictBase** `( Background launcher; Change BackgroundColor not `_`ForegroundColor`_`)`


---
##### :octicons-arrow-left-16: [Back ResidentMenu.szs](../index.md)
**File:** `ResidentMenu.szs/blyt/RdtBtnFullLauncher.bflyt`<br>
**Main `bflyt` file:** [`RdtBase.bflyt`](../RdtBase.bflyt.md)
