##### :octicons-arrow-left-16: [Back ResidentMenu.szs](../index.md)

#RdtBalloonCtrl.bflyt

**File:** `ResidentMenu.szs/blyt/RdtBalloonCtrl.bflyt`<br>
**Main `bflyt` file:** [`RdtBase.bflyt`](../RdtBase.bflyt.md)

---

## Layout of `ResidentMenu.szs/blyt/RdtBalloonCtrl.bflyt`

<!-- prettier-ignore -->

## Tree

-	**RootPane [pan 1]**
	-	**N_Change [pan 1]**
		-	**P_Base [pic 1]** `the controller popup background`
		-	**P_Tip [pic 1]** `the arrow on the controller popup`
			-	**P_TipShdw [pic 1]** `the arrow shadow on the controller popup`
		-	**N_Ctrl [pan 1]** `Root panel of all the related icons`
			-	**P_CtrlJointH [pic 1]** `controller / horizontal joycon icon`
			-	**N_CtrlL [pan 1]** `Left controller root panel`
				-	**N_CtrlLPos [pic 1]**
					-	**P_CtrlJointVL [pic 1]** `left controller icon`
				-	**N_BtnL [pan 1]** `trigger button root panel`
					-	**P_BtnL [pic 1]** `L trigger button`
					-	**P_CtrlJointVLGhost [pic 1]** `ghost/greyed joycon image`
			-	**N_CtrlR [pan 1]** `Right controller root panel`
				-	**N_CtrlRPos [pic 1]**
					-	**P_CtrlJointVR [pic 1]** `right controller icon`
				-	**N_BtnR [pan 1]** `trigger button root panel`
					-	**P_BtnR [pic 1]** `R trigger button`
					-	**P_CtrlJointVRGhost [pic 1]** `ghost/greyed joycon image`