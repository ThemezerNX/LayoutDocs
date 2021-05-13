# Stationary Game Icons

Examples of layouts that show what stationary game icons look like are [Doge Layout](https://themezer.net/layouts/homemenu/Doge-Layout-e) and [Two Row layout](https://themezer.net/layouts/homemenu/Two-Row-Layout-Compact--1c).

<!-- prettier-ignore -->
!!! Warning
    If you don't actually want to make the icons stationary, but want to *move* the gamerow, see [Repositioning and Scaling the Gamerow](./reposition-gamerow.md).

## Firmware ≥8.x

Ever since 8.0 came out, stationary game icons have been a bit of a mess to get working properly. This is because 8.0 introduced looped scrolling in the home menu. Another factor was that some behaviour regarding hitboxes was changed.

In order to get stationary icons to function properly from this version onwards, the following steps should be followed:

### `RdtBtnIconGame.bflyt`

1. Set the `x,y scale` of `RootPane` to a custom value. Remember this value and let's call it `p`.
2. Set the `x,y scale` of `B_Hit` to `1.0/p`
3. Set the `width,height` of `B_Hit` to `256*p`. `256` is the default value for width and height, but it might get changed in a future version.

### `RdtBase.bflyt`

4. Set the `width` of `N_ScrollWindow` to `100000.0`
5. Set the `x,y coordinates` of `N_GameRoot` to coordinate where you want your first game icon to be.
6. Set the `x scale` of `N_GameRoot` to `0.00001`
7. Set the `x coordinate` of `N_Game` to `0.0` (!)
8. Set the `x scale` of `N_Game` to `100000.0`
9. Set the `x,y coordinate` of `N_Icon_00` to `0.0`
10. Set the `x,y coordinate` of `N_Icon_[01-11]` to the positions you want. Move icons that you don't want to be shown to `(1;9999)`. If I remember correctly, the scale `p` has an influence on this.
11. Set the `x,y scale` of `L_BtnFlc` to `p`.
12. Change the `y scale` of `N_ScrollArea` and `N_ScrollWindow` to increase the size of the touch area. You will notice that some icons cannot be tapped if you haven't configured this correctly.
    - Optionally change the `y coordinate`

<!-- prettier-ignore -->
!!! Warning
    Even slightly deviating from the values above might cause the cursor not being able to reach the icon, or not being able to tap the icon on the touch screen. However, if you find that these values do not work in your case, the only option would be to mess around with the positions of the panes (not the scale).

## Firmware <8.x

On firware version 7.x and lower, it is fairly easy to move the game icons around. In order to make them stationary do the following:

1. Change the X,Y scale of `RootPane` in `RdtBtnIconGame.bflyt` to your likings
2. Change the X scale of `N_Game` in `RdtBase.bflyt` to `100000.0`
3. Reposition the game icons `N_Icon_XX` in `RdtBase.bflyt` to your likings
