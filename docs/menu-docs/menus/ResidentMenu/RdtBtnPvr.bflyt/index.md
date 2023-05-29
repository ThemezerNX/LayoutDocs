##### :octicons-arrow-left-16: [Back ResidentMenu.szs](../index.md)

#RdtBtnPvr.bflyt

**File:** `ResidentMenu.szs/blyt/RdtBtnPvr.bflyt`<br>
**Main `bflyt` file:** [`RdtBase.bflyt`](../RdtBase.bflyt.md)

---

## Layout of `ResidentMenu.szs/blyt/RdtBtnPvr.bflyt`

<!-- prettier-ignore -->
!!! Info
    These aren't all the functions, most are unknown or the component is unimportant.
	
## Tree

-   **N_Root [pan 1]**
	-	**N_DecideKey [pan 1]**
		-	**N_DecideTouch [pan1]**
			-	**N_PictBase [pic 1]** `icon background`
			-	**N_02 [pan 1]**
				-	**P_PictMask [pic 1]**
			-	**N_01 [pan 1]**
				-	**P_Pict_01 [pic 1]** 
				-	**P_Color [pic 1]**
			-	**N_00 [pan 1]**
				-	**P_Pict_00 [pic 1]** `main album icon color`
			-	**N_ScaleDecide [pan 1]**
				-	**P_BtnDecideKey [pic 1]**
				-	**P_BtnTouch [pic 1]**
			-	**N_Limit [pan 1]**
				-	**N_BtnFocusKey [pan 1]**
					-	**UF_Cursor [prt 1]**
			-	**P_Effect [pic 1]**
	-	**N_Tip [pan 1]**
		-	**L_Balloon [prt 1**]
-	**B_Hit [bnd 1]**	
---

<!-- prettier-ignore -->
!!! Info
    Material Editing colors can be tricky, edit background colors (RGBA) `255;255;255;AAA` (Alpha 0-255 for opacity)



-	**Materials**
	-	**0: P_BtnDecideKey
	-	**1: P_BtnTouch
	-	**2: P_Effect
	-	**3: P_Pict_00
	-	**4: P_Pict_01
	-	**5: P_PictMask**
	-	**6: P_Color**
	-	**7: P_PictBase** `( Icon Background; Change BackgroundColor not `_`ForegroundColor`_`)`

---
	
##### :octicons-arrow-left-16: [Back ResidentMenu.szs](../index.md)

**File:** `ResidentMenu.szs/blyt/RdtBtnPvr.bflyt`<br>
**Main `bflyt` file:** [`RdtBase.bflyt`](../RdtBase.bflyt.md)
