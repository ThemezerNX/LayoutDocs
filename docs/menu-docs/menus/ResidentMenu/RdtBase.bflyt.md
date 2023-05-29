##### :octicons-arrow-left-16: [Back ResidentMenu.szs](index.md)

#RdtBase.bflyt (Main bflyt)

**File:** `ResidentMenu.szs/blyt/RdtBase.bflyt`<br>
**This is the Main `bflyt` file**

---

## Layout of `ResidentMenu.szs/blyt/RdtBase.bflyt `

<!-- prettier-ignore -->

## Tree

-	**RootPane [pan 1]**
    -   **L_BgNml [prt 1]** `contains the original light/dark background, but the 'exelixbg' panel as well after being patched with a custom background`
    -   **N_Root [pan 1]**
		-	**N_ScrollArea [pan 1]** `game icon scroll area`
		-	**N_ScrollWindow [pan 1]** `game icon scroll window "Touch related"`
		-	**T_Blank [txt 1]**
        -   **N_GameRoot [pan 1]** `panel contains all items that will be scrolled`
			-	**N_Game [pan 1]**
				-   **[`N_Icon[00-11] [pan 1]`](RdtBtnIconGame.bflyt.md)** `all 12 game icons. They make use of the same layout`
					-	**L_BtnChangeUser [prt 1]** `contains "`:material-alpha-y-circle:` Switch user" RdtBtnChangeUser.bflyt`
				-   **N_Icon_12 [pan 1]** `The 13th icon : All Apps Root panel`
					-   **L_BtnFlc [prt 1]** `All Apps button` [`RdtBtnFullLauncher.bflyt`](RdtBtnFullLauncher.bflyt/index.md)
        -   **N_System [pan 1]** `contains all Nintendo system applets`
			-	**L_BtnLR [prt 1]** `Nintendo Switch Online button not able to be hidden via visibility`
            -   **L_BtnNoti [prt 1]** `the notifications button RdtBtnNtf.bflyt`
            -   **L_BtnShop [prt 1]** `the eshop button RdtBtnShop.bflyt`
            -   **L_BtnPvr [prt 1]** `the album button RdtBtnPvr.bflyt`
            -   **L_BtnCtrl [prt 1]** `the controllers button RdtBtnCtrl.bflyt`
            -   **L_BtnSet [prt 1]** `the settings button RdtBtnSet.bflyt`
            -   **L_BtnPow [prt 1]** `the power button RdtBtnPow`
        -   **L_ChildLock [prt 1]** `the childlock button`
        -   **N_Balloon [pan 1]**
        -   **N_MyPage [pan 1]** `usericons root panel`
            -   **L_BtnAccount_[00-07] [prt1]** `all usericons which make use of a single layout`
        -   **L_Hud [prt 1]** `the hud (clock, network, battery) Hud.bflyt`
        -   **L_BalloonCtrl [prt 1]** `the balloon that pops up when (dis)connecting a controller RdtBalloonCtrl.bflyt`
