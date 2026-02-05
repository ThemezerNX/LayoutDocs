##### :octicons-arrow-left-16: [Back Psl.szs](../index.md)

#PslBtnCardPlayer.bflyt

**File:** `Psl.szs/blyt/PslBtnCardPlayer.bflyt`

---

## Layout of `Psl.szs/blyt/PslBtnCardPlayer.bflyt`

<!-- prettier-ignore -->
!!! Info
    These aren't all the functions, most are unknown or the component is unimportant.

## Tree

-	**RootPane [pan 1]**
	-	**N_Root_00 [pan 1]** 
		-	**N_BtnCardBase [pan 1]**
			-	**P_BtnCardBase [pic 1]**
		-	**N_BtnCntImg [pan 1]**
			-	**P_PlayerImage [pic 1]**
		-	**N_BtnCnt [pan 1]**
			-	**P_BgName [pic 1]** `background plate of player name`
			-	**T_PlayerName [txt 1]** `Player Name Text Color`
		-	**N_PlayerNameScroll [pan 1]**
			-	**N_Size [pan 1]**
				-	**N_Scissor [pan 1]**
					-	**N_Offset [pan 1]**
						-	**P_Reset [pic 1]**
						-	**N_Scroll [pan 1]**
							-	**T_Main [txt 1]**
							-	**N_Margin [pan 1]**
							-	**T_Sub [txt 1]**
						-	**W_Fade [wnd 1]**
						-	**P_Color [pic 1]**
		-	**N_InvalidAdditional [pan 1]**
			-	**P_Mask [pic 1]**
			-	**P_Check [pic 1]**
		-	**P_BtnDecideKey [pic 1]**
		-	**P_BtnTouch [pic 1]**
		-	**N_BtnFocusKey [pan 1]**
			-	**P_InnerCursor [pic 1]**
			-	**UF_Cursor [prt 1]**
	-	**B_Hit [bnd 1]**