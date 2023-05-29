##### :octicons-arrow-left-16: [Back ResidentMenu.szs](../index.md)

#BatteryConsole.bflyt

**File:** `ResidentMenu.szs/blyt/BatteryConsole.bflyt`<br>
**Main `bflyt` file:** [`RdtBase.bflyt`](../RdtBase.bflyt.md)

---

## Layout of `ResidentMenu.szs/blyt/BatteryConsole.bflyt`

<!-- prettier-ignore -->
!!! Info
    These aren't all the functions, most are unknown or the component is unimportant.

## Tree

-	**RootPane [pan 1]**
	-	**N_Root [pan 1]** 
		-	**N_Num [pan 1]**
			-	**N_Num_00 [prt 1]**
			-	**N_Num_01 [prt 1]**
			-	**N_Num_02 [prt 1]**
			-	**P_Per [pic 1]**
		-	**N_00 [pan 1]**
			-	**P_BatBase [pic 1]**
			-	**N_GaugeNml [pan 1]**
				-	**P_GaugeNml [pic 1]** `Inner Battery Element; color can be changed`
			-	**N_GaugeOther [pan 1]**
				-	**P_GaugeOther [pic 1]**
			-	**P_Charge [pic 1]** `Charger Icon Color`
			-	**P_Ico00 [pic 1]**
		-	**P_Ico00 [pic 1]** `Outer Battery Color`
	-	**B_Hit [bnd 1]**