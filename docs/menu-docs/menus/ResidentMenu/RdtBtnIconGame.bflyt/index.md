##### :octicons-arrow-left-16: [Back ResidentMenu.szs](../index.md)

#RdtBtnIconGame.bflyt

**File:** `ResidentMenu.szs/blyt/RdtBtnIconGame.bflyt`<br>
**Main `bflyt` file:** [`RdtBase.bflyt`](../RdtBase.bflyt.md)

---

## Layout of `ResidentMenu.szs/blyt/RdtBtnIconGame.bflyt`

<!-- prettier-ignore -->
!!! Info
    These aren't all the functions, most are unknown or the component is unimportant.
	
## Tree

-   **RootPane [pan 1]**
	-    **N_Root [pan 1]**
		-   **N_Delete [pan 1]**
			-   **N_DecideKey [pan 1]**
				-   **N_DecideTouch [pan 1]**
					-   **P_BtnBase [pic 1]** `the white background hidden behind a game icon. Can shortly be seen after boot`
					-   **P_IconGame [pic 1]** `the game's icon`
					-   **P_Blank [pic 1]**
						-   **L_Loading [prt 1]** `the loading icon displayed on top of P_BtnBase`
					-   **N_Suspend [pan 1]**
						-   **N_SuspendPos [pan 1]**
							-   **N_TextPos [pan 1]**
								-   **P_Suspend_00 [pic 1]** `the white oval background behind the text`
								-   **T_Suspend [txt 1]** `the 'Playing' text when a game is opened`
							-   **P_account_03 [pic 1]** `the usericon displayed on the left of the 'Playing' indicator`
							-	**P_account_02 [pic 1]** `the usericon displayed on the left of the 'Playing' indicator`
							-	**P_account_01 [pic 1]** `the usericon displayed on the left of the 'Playing' indicator`
							-	**P_account_00 [pic 1]** `the usericon displayed on the left of the 'Playing' indicator`
					-   **N_DL [pan 1]** `loading bars you don't have to care about`
						-	**N_DlNml [pan 1]**
							-	**L_ProgressBarNml [prt1]**
						-	**N_DlErr [pan 1]**
							-	**L_ProgressBarErr [prt1]**
							-	**N_Offkine [pan 1]**
							-	**L_ProgressBarOffline [prt1]**
					-   **P_BtnDecideKey [pic 1]** `the blue overlay which can be seen when a game is launched via the controller`
					-   **P_BtnTouch [pic 1]** `the blue overlay which can be seen when tapping/holding the game icon`
					-   **P_InnerCursor [pic 1]** `the white ring displayed between the blue cursor and the game icon`
					-   **N_BtnFocusKey [pan 1]**
						-   **UF_Cursor [prt 1]** `the blue cursor displayed around the game icon`
					-   **P_EffectDecide [pic 1]** `the effect when a game is launched, a second game icon can be seen dissolving`
					-   **N_Promotion [pan 1]**
						-   **L_Promotion [prt 1]** `the not-yet-in-use 'test' or 'try' function for games`
-   **N_Tip [pan 1]** `can be used to position RdtBalloon`
    -   **L_Balloon [prt 1]** - [`RdtBalloon.bflyt`](RdtBalloon.bflyt.md): the game's name/text in blue
-   **B_Hit [bnd 1]** `hitbox of all the items in N_DecideKey`

---

##### :octicons-arrow-left-16: [Back ResidentMenu.szs](../index.md)

**File:** `ResidentMenu.szs/blyt/RdtBtnIconGame.bflyt`<br>
**Main `bflyt` file:** [`RdtBase.bflyt`](../RdtBase.bflyt.md)
