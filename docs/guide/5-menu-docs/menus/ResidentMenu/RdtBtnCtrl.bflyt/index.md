##### :octicons-arrow-left-16: [Back ResidentMenu.szs](../index.md)

#RdtBtnCtrl.bflyt

**File:** `ResidentMenu.szs/blyt/RdtBtnCtrl.bflyt`<br>
**Main `bflyt` file:** [`RdtBase.bflyt`](../RdtBase.bflyt.md)

---

## Layout of `ResidentMenu.szs/blyt/RdtBtnCtrl.bflyt`

<!-- prettier-ignore -->
!!! Info
    These aren't all the functions, most are unknown or the component is unimportant.
	
## Tree

-   **N_Root [pan 1]**
	-	**N_DecideKey [pan 1]**
		-	**N_DecideTouch [pan1]**
			-	**N_Pict [pan 1]**
				-	**P_Form [pic 1]** `Controller outline or replaced icon`
				-	**P_Stick [pic 1]**
				-	**P_Y [pic 1]**
				-	**P_X [pic 1]**
				-	**P_A [pic 1]**
				-	**P_B [pic 1]**
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
	-	**0: P_Form**
	-	**1: P_Effect**
	-	**2: P_BtnTouch**
	-	**3: P_BtnDecideKey**
	-	**4: P_B**
	-	**5: P_A**
	-	**6: P_X**
	-	**7: P_Y**
	-	**8: P_Stick**
	-	**9: P_PictBase** `( Icon Background; Change BackgroundColor not `_`ForegroundColor`_`)`

---
	
##### :octicons-arrow-left-16: [Back ResidentMenu.szs](../index.md)

**File:** `ResidentMenu.szs/blyt/RdtBtnCtrl.bflyt`<br>
**Main `bflyt` file:** [`RdtBase.bflyt`](../RdtBase.bflyt.md)