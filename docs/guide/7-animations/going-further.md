# More on animations
---

## Useful tables

### PaiTag entries & AnimationTarget values

`AnimationTarget` values and subsequent animation behavior change depending on the defined `PaiTag`. A comprehensive list of animation Tags and Targets can be viewed on the following page:

##### **[PaiTags and AnimationTargets](./paitags-and-targets.md) :octicons-arrow-right-16:**

### bflyts, bflans, szs

Some `.bflyt`s, `.bflan`s and their corresponding `.szs` are also documented there:

##### **[szs, bflyt, bflan files](./szs-bflyt-bflan.md) :octicons-arrow-right-16:**

## Active and Inactive states

We can find specific pairs of `.bflan` files for some `.bflyt`s such as `<bflyt>_Active.bflan` / `<bflyt>_Inactive.bflan`.

In the main tutorial section, we worked on `RdtBtnIconGame_Active.bflan` / `RdtBtnIconGame_Inactive.bflan`, but there are a couple others as well, e.g. `RdtBtnSet_Active.bflan` / `RdtBtnSet_Inactive.bflan`.

##### **[szs, bflyt, bflan files](./szs-bflyt-bflan.md) :octicons-arrow-right-16:**

- `<bflyt>_Active.bflan` animates `<bflyt>` panes when the UI element is **selected**

- `<bflyt>_Inactive.bflan` animates `<bflyt>` panes when the UI element is **being unselected**

!!! info
      More `.bflan` files follow a similar logic, e.g. `<bflyt>_FocusKey.bflan` / `<bflyt>_UnFocusKey.bflan`. These aren't fully tested nor documented yet.

!!! warning
      Edits made for Inactive `.bflan`s will overwrite the values you might have defined in your `.json` layout. For example, if you've set the album button's x-coordinate to `660px` in your `.json` while it is set to `680px` in the Inactive `.bflan`, the `680px` value will take priority over the `660px` one and be applied.

## Looping animations

It is possible to make looping animations. These can be seen
in [Migush](https://themezer.net/creators/123859829453357056)'
s [JAG layout](https://themezer.net/layouts/homemenu/JAG-Layout-2) where selected game icons follow a scale up and down
idle animation. All you have to do to make a looping animation is to set the `Flags` value to `1` (while `0` disables
the loop) in the `Pai1 section` of a `.bflan` file. Unfortunately, **more complex animations that combine multiple
transformations can't be achieved properly** since the flag is applied to the whole `.bflan`. More explicitly, a
game icon wouldn't be able to move `10px` above AND THEN follow a looping scale up and down. In such a case, the y-displacement would also be looped.

## Fade in and fade out animations

Let's say I want a blinking cursor for the navigation menu in the settings applet. This involves using `FLVC` and `AnimationTarget` = `16`. I will briefly describe the process but it is basically the same as in the main tutorial:

1. Open `Set.szs` then `BtnNav_Root_Active.bflan`. **As always when creating custom animations,** do the proper modifications to
   the `Pat1` and `Pai1` sections. Add the `N_BtnFocusKey` entry (cursor pane) to the list, create a **`FLVC` entry** (
   not `FLPA`!) right under it, and then another entry under `FLVC`. I chose to set my key frames as shown on the screenshots below.
2. We'll also edit `BtnNav_Root_Inactive.bflan`, otherwise navigating the tabs will interrupt the cursor animation and
   lock it to a certain frame (same behavior as in our previous game icon animation). Considering that, we simply "
   reset" `N_BtnFocusKey`'s state (after adding this pane to the list) by setting its alpha channel to `0` at frame `0`.
3. For each `.bflan` file, create properly named groups in the `RootGroup` section of `BtnNav_Root.bflyt`. **Don't forget to save all your edits.**
4. Layout diff, compile and install, and there you go — you now have a working blinking cursor.

| ![Settings (1)](tuto14.jpg "Settings (1)") | ![Settings (2)](tuto15.jpg "Settings (2)") |
|--------------------------------------------|--------------------------------------------|
| Adding `FLVC` entry (Active)               | Adding `FLVC` entry (Inactive)             |

## Animated backgrounds

Animated backgrounds have been in the trends lately (as of the time of writing). The truth is, there is some intricacy behind animated background themes, so **let's make it clear once and for all**.

**There is no *proper* nor easy known way to make animated backgrounds.** Switch Theme Injector only supports `.dds`
and `.jpg` files.
An alternative solution would be to animate the pane that contains your custom background image. That *indeed* works,
and there are a few themes that already have achieved this out there. To do so, working with `ResidentMenu.szs`, you
need to add `L_BgNml` to the pane list in `RdtBase_Enter.bflan` and make your edits to your convenience. However, this
solution has its limitations:

- `RdtBase_Enter.bflan` contains the home screen unlocking animation. Try to loop your animation using the `Flags` item
  and maybe you can guess what will happen (boot loop, UI and sound glitches). The only thing you can do to sort of
  reproduce a looping behavior is to duplicate your animation pattern all the way through an absurd amount of key
  frames. [Zhi](https://themezer.net/creators/239384767785730048) actually did this in
  his [Patterns theme](https://themezer.net/packs/Patterns.-58f) with a frame limit of 64000 (which makes it about 8
  minutes). If you are interested in learning the whole process, you can read
  through [his own documentation there](https://github.com/zzzribas/Patterns/wiki). As a side note, you might want to
  stay tuned for Zhi's next releases because he comes up with quite some good ideas!

- You're still stuck with a static background image since there is no support for animated images of any kind, nor for
  video files
- You could make a collage of frames in a single background (each corner a 360p image). This way you could use an animation to focus on different corners and make it look like your background has four frames. You could make it two frames by putting the images simply next to each other. You will probably have to reduce quality of each picture to ~480p. You will still have to rely on manually adding many frame entries.
- You can make gradient animations by animating Top/Bottom Left/Right corner colors, and not use a background image. Still, manually repeating the frames is required.
- On firmware versions 5.x and below you could very easily loop background animations, as the `loop` flag did not affect the 'enter' animation when coming from the lockscreen.

For the other applets (e.g. settings, user page, etc.), there is actually no known way at all to apply any kind of animation to a custom background image.

## Animations *may* overwrite things</a>

If you spent some time editing `.json` layouts, you may have encountered cases where, no matter what you do, the
changes you make to a pane (e.g. colors, position, etc.), even while having the `C_W` and `C_B` patches enabled, lead to
no result. **In such cases, chances are that an animation is overwriting your edits.**

One notable case is the Redownload Software button at the bottom of the full launcher applet's main
page (`Flauncher.szs`). The panes corresponding to this button are `L_ReDL` (`L_Shop` before 20.x.x) and `T_Empty`, and these won't hide by
simply attaching the `Visible: false` property to them. This is due to the `FLVI` entries in `FlcCntMain_Type.bflan`
that overwrite any modification attempt made within your `.json` code. To sort this out, the `KeyFrames` values under each `FLVI` entry
must be set to `0` (`1` by default).

| ![Shop (1)](tuto16.jpg "Shop (1)") | ![Full launcher (2)](tuto17.jpg "Shop (2)") |
|------------------------------------|---------------------------------------------|
| `L_ReDL` > `FLVI` > `KeyFrames`    | `T_Empty` > `FLVI` > `KeyFrames`            |

| ![Full launcher (1)](flaunch1.jpg "Full launcher (1)") | ![Full launcher (2)](flaunch2.jpg "Full launcher (2)") |
|--------------------------------------------------------|--------------------------------------------------------|
| Visible Redownload Software button                     | Hidden Redownload Software button                      |

Giving another example, take a look at my Unison R home menu theme: highlighted games have a white rounded card around their icon. These cards' corresponding pane is `P_BtnBase` from `RdtBtnIconGame.bflyt`. This pane actually has some transparency defined through animations by default. So in order to make this pane fully opaque, we need to look into the animations of `P_BtnBase` and change its `KeyFrames` value to `255` under the `FLVC` entry.
