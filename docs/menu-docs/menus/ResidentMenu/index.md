# Home Menu

**File:** `ResidentMenu.szs`  
**Main `bflyt` file:** `RdtBase.bflyt`

---

## General Parts in This Menu

-   **Cursor:** `Cursor3.bflyt`
-   **App Name Balloon:** `RdtBalloon.bflyt`
-   **Time (Numbers):** `GTNumL.bflyt` and `GTNumM.bflyt`
-   **Time (AM, PM, Colon):** `HudTime.bflyt`
-   **Wifi Signal:** `HudSignal.bflyt`
-   **Battery (Icon):** `BatteryConsole.bflyt`
-   **Battery (Percent):** `HudBatteryNum.bflyt`
-   **Full Launcher (All Apps):** `RdtBtnFullLauncher.bflyt`

## Tree

-   **RdtBase.bflyt**
    -   **[L_BgNml](./BgNml.bflyt.md)**: `contains the original light/dark background, but the 'exelixbg' panel as well after being patched with a custom background`
    -   **N_Root**
        -   **N_GameRoot**: `contains all items that will be scrolled`
            -   **[N_Icon[00-11]](./RdtBtnIconGame.bflyt.md)**: `all 12 game icons. They make use of the same layout`
            -   **N_Icon_12**
                -   **[L_BtnFlc](./RdtBtnFullLauncher.bflyt.md)**: `the 13th icon in the gameroot: the 'all apps' button`
        -   **N_System**: `contains all six system applets`
            -   **[L_BtnNoti](./RdtBtnNtf.bflyt.md)**: `the notifications button`
            -   **[L_BtnShop](./RdtBtnShop.bflyt.md)**: `the eshop button`
            -   **[L_BtnCtrl](./RdtBtnPvr.bflyt.md)**: `the album button`
            -   **[L_BtnPvr](./RdtBtnCtrl.bflyt.md)**: `the controllers button`
            -   **[L_BtnSet](./RdtBtnSet.bflyt.md)**: `the settings button`
            -   **[L_BtnPow](./RdtBtnPow.bflyt.md)**: `the power button`
        -   **[L_ChildLock/RdtBtnChildLock.bflyt](./RdtBtnChildLock.bflyt.md)**: `the childlock button`
        -   **[N_Balloon](./RdtBalloon.bflyt.md)**
        -   **N_MyPage**
            -   **[L_BtnAccount\_[00-07]](./RdtBtnMyPage.bflyt.md)**: `all usericons which make use of a single layout`
        -   **[L_Hud](./Hud.bflyt.md)**: `the hud (clock, network, battery)`
        -   **[L_BalloonCtrl](./RdtBalloonCtrl.bflyt.md)**: `the balloon that pops up when (dis)connecting a controller`

---

## All files in `ResidentMenu.szs`

| Filename                                                     | Hypothetical full name          |
| ------------------------------------------------------------ | ------------------------------- |
| [BatteryConsole.bflyt](BatteryConsole.bflyt)                 | BatteryConsole                  |
| [BgNml.bflyt](BgNml.bflyt)                                   | BackgroundNormal                |
| [Cursor3.bflyt](Cursor3.bflyt)                               | Cursor3                         |
| [GTNumL.bflyt](GTNumL.bflyt)                                 | GeneralTimeNumberLarge          |
| [GTNumM.bflyt](GTNumM.bflyt)                                 | GeneralTimeNumberMedium         |
| [Hud.bflyt](Hud.bflyt)                                       | Hud                             |
| [HudBatteryNum.bflyt](HudBatteryNum.bflyt)                   | HudBatteryNumber                |
| [HudSignal.bflyt](HudSignal.bflyt)                           | HudSignal                       |
| [HudTime.bflyt](HudTime.bflyt)                               | HudTime                         |
| [RdtBalloon.bflyt](RdtBalloon.bflyt)                         | ResidentMenuBalloon             |
| [RdtBalloonCtrl.bflyt](RdtBalloonCtrl.bflyt)                 | ResidentMenuBalloonController   |
| [RdtBalloonSystemApplet.bflyt](RdtBalloonSystemApplet.bflyt) | ResidentMenuBalloonSystemApplet |
| [RdtBase.bflyt](RdtBase.bflyt)                               | ResidentMenuBase                |
| [RdtBtnChildLock.bflyt](RdtBtnChildLock.bflyt)               | ResidentMenuButtonChildLock     |
| [RdtBtnCtrl.bflyt](RdtBtnCtrl.bflyt)                         | ResidentMenuButtonController    |
| [RdtBtnFullLauncher.bflyt](RdtBtnFullLauncher.bflyt)         | ResidentMenuButtonFullLauncher  |
| [RdtBtnIconGame.bflyt](RdtBtnIconGame.bflyt)                 | ResidentMenuButtonIconGame      |
| [RdtBtnMyPage.bflyt](RdtBtnMyPage.bflyt)                     | ResidentMenuButtonMyPage        |
| [RdtBtnNtf.bflyt](RdtBtnNtf.bflyt)                           | ResidentMenuButtonNotification  |
| [RdtBtnPow.bflyt](RdtBtnPow.bflyt)                           | ResidentMenuButtonPower         |
| [RdtBtnPvr.bflyt](RdtBtnPvr.bflyt)                           | ResidentMenuButtonPictureviewer |
| [RdtBtnSet.bflyt](RdtBtnSet.bflyt)                           | ResidentMenuButtonSettings      |
| [RdtBtnShop.bflyt](RdtBtnShop.bflyt)                         | ResidentMenuButtonShop          |
| [RdtIconPromotion.bflyt](RdtIconPromotion.bflyt)             | ResidentMenuIconPromotion       |
