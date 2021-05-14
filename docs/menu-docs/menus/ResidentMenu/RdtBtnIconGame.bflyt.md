## Tree

[](index.md)

-   `N_Root`
    -   `N_Delete`
        -   `N_DecideKey`
            -   `N_DecideTouch`
                -   `P_BtnBase`: the white background hidden behind a game icon. Can shortly be seen after boot.
                -   `P_IconGame`: the game's icon
                -   `P_Blank`
                    -   `L_Loading`: the loading icon displayed on top of P_BtnBase`
                -   `N_Suspend`
                    -   `N_SuspendPos`
                        -   `N_TextPos`
                            -   `P_Suspend_00`: the white oval background behind the text
                            -   `T_Suspend`: the 'Playing' text when a game is opened
                        -   `P_account_[03-00]`: the usericon displayed on the left of the 'Playing' indicator
                -   _N_DL: loading bars you don't have to care about_
                -   `P_BtnDecideKey`: the blue overlay which can be seen when a game is launched via the controller
                -   `P_BtnTouch`: the blue overlay which can be seen when tapping/holding the game icon
                -   `P_InnerCursor`: the white ring displayed between the blue cursor and the game icon
                -   `N_BtnFocusKey`
                    -   `UF_Cursor`: the blue cursor displayed around the game icon
                -   `P_EffectDecide`: the effect when a game is launched, a second game icon can be seen dissolving
                -   `N_Promotion`
                    -   `L_Promotion`: the not-yet-in-use 'test' or 'try' function for games
-   `N_Tip`
    -   [`RdtBalloon.bflyt`](RdtBalloon.bflyt.md): the game's name/text in blue
-   `B_Hit`: hitbox of all the items in N_DecideKey
