##### :octicons-arrow-left-16: [Back ResidentMenu.szs](../index.md)

#RdtBalloon.bflyt

**File:** `ResidentMenu.szs/blyt/RdtBalloon.bflyt`<br>
**Main `bflyt` file:** [`RdtBase.bflyt`](../RdtBase.bflyt.md)

---

## Layout of `ResidentMenu.szs/blyt/RdtBalloon.bflyt`

<!-- prettier-ignore -->
!!! Info
    These aren't all the functions, most are unknown or the component is unimportant.
	
## Tree

-   **N_Root [pan 1]**
    -   **N_Trans [pan 1]**
        -   **N_Size [pan 1]**
            -   **N_Scissor [pan 1]**
                -   **N_Offset [pan 1]**
                    -   **P_Reset [pic 1]**
                    -   **N_Scroll [pan 1]** `contains all scrolling parts in the balloon (so only the text really)`
                        -   **T_Main [txt 1]** `the icon's name`
                        -   **N_Margin [pan 1]**
                        -   **T_Sub [txt 1]**
					-	**W_Fade [wnd 1]**
					-	**P_Color [pic 1]** `Game text color`
        -   **N_Card**
            -   **P_Card**: `gamecard icon`
