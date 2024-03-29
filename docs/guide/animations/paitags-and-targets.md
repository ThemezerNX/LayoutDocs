##### :octicons-arrow-left-16: [Back to Animations: extras](./going-further.md)

# PaiTags and targets for FLAN Animations

---

## PaiTags

All kinds of different animations exist, from simple transformations to changing shadows or color. The table below shows
all encountered types of animation in the (b)flan filetype. The `PaiTag` indicates which types of animations will be
used, while the `AnimationTarget` specifies a specific property.

- Items with a ✅ are properly understood and documented and supported by many tools.
- Items with a 🟧 are partially understood and documented.
- Items with a ⛔ have never really been tested, documented, nor implemented in any tool. Their exact workings are
  unknown.

| `PaiTag`      |   | Name                                  | Used for                                                                                                 |
|---------------|---|---------------------------------------|----------------------------------------------------------------------------------------------------------|
| [FLPA](#FLPA) | ✅ | **PA**ne SRT                          | Basic transformations                                                                                    |
| [FLVI](#FLVI) | ✅ | **VI**sibility                        | Visibility (shown or hidden)                                                                             |
| [FLTS](#FLTS) | ✅ | **T**exture **S**RT                   | Texture transformations                                                                                  |
| [FLVC](#FLVC) | ✅ | **V**ertex **C**olor                  | Vertex color                                                                                             |
| [FLMC](#FLMC) | ✅ | **M**aterial **C**olor                | Material Color                                                                                           |
| [FLTP](#FLTP) | 🟧 | **T**exture **P**attern               | Texture pattern                                                                                          |
| [FLIM](#FLIM) | ✅ | **I**ndirect Texture SRT              | Indirect(?) texture transformations                                                                      |
| FLAC          | ⛔ | **A**lpha Test                        | _unknown_                                                                                                |
| [FLCT](#FLCT) | 🟧  | Font Shadow                           | Font shadows                                                                                             |
| FLCC          | ⛔ | Per-**C**haracter Transform **C**urve | _unknown_                                                                                                |
| [FLEU](#FLEU) | ⛔ | **E**xtended **U**ser Information     | USD patches (e.g. battery color based on charge level). These animations are controlled from the application's code |

Next a `PaiTag` has to be specified. This is the object that will be animated. The table below
shows all known types of targets in the (b)flan filetype. Next, the `AnimationTarget` indicates what specific property will be modified (
e.g. x position, y rotation, etc.).

!!! Info
    Note that SwitchLayoutEditor does not support all PaiTags and PaiTargets, although the most important ones are
    supported.

For more info about these tags and the different versions among consoles, check
out [this file](https://github.com/KillzXGaming/Switch-Toolbox/blob/c9e74e0be114885f347789f3bd348baccacf0842/File_Format_Library/FileFormats/Layout/Common.cs)
from Switch Toolbox.

### <a href="#FLPA"></a>FLPA (Pane SRT)

Related to basic transformations listed below.

| `AnimationTarget` | Name                         | Type  | Values        | 
|-------------------|------------------------------|-------|---------------|
| `0`               | X-axis translation           | float | any (px)      |
| `1`               | Y-axis translation           | float | any (px)      |
| `2`               | Z-axis translation           | float | any (px)      |
| `3`               | X-axis rotation (vertical)   | float | any (radians) |
| `4`               | Y-axis rotation (horizontal) | float | any (radians) |
| `5`               | Z-axis rotation (flat)       | float | any (radians) |
| `6`               | X-axis scale                 | float | any           |
| `7`               | Y-axis scale                 | float | any           |
| `8`               | X-axis size                  | float | any (px)      |
| `9`               | Y-axis size                  | float | any (px)      |

- Translations are relative to the (x, y) coordinates defined in your `.json` layout, so a (0, 0) translation means that
  the pane keeps its base position
- Scaling is also relative to what is defined in your `.json` layout. To keep your pane size at a 1:1 ratio, KeyFrame `value`s should be set to `1`

### <a href="#FLVI"></a>FLVI (Visibility)

| `AnimationTarget` | Name    | Type | Values                      |
|-------------------|---------|------|-----------------------------|
| `0`               | Visible | int  | `0` (hidden), `1` (visible) |

### <a href="#FLTS"></a>FLTS (Texture SRT)

| `AnimationTarget` | Name               | Type  | Values        |
|-------------------|--------------------|-------|---------------|
| `0`               | U-axis translation | float | any (px)      |
| `1`               | V-axis translation | float | any (px)      |
| `2`               | Rotation           | float | any (radians) |
| `3`               | U-axis scale       | float | any           |
| `4`               | V-axis scale       | float | any           |

### <a href="#FLMC"></a>FLMC (Material Color)

| `AnimationTarget` | Name                       | Type  | Values | 
|-------------------|----------------------------|-------|--------|
| `0`               | Black Color Red            | int   | 0-255  |
| `1`               | Black Color Green          | int   | 0-255  |
| `2`               | Black Color Blue           | int   | 0-255  |
| `3`               | Black Color Alpha          | int   | 0-255  |
| `4`               | White Color Red            | int   | 0-255  |
| `5`               | White Color Green          | int   | 0-255  |
| `6`               | White Color Blue           | int   | 0-255  |
| `7`               | White Color Alpha          | int   | 0-255  |
| `8`               | Texture Color Blend Ratio  | float | any    |
| `9`               | Tev Color 0 Red            | int   | 0-255  |
| `10`              | Tev Color 0 Green          | int   | 0-255  |
| `11`              | Tev Color 0 Blue           | int   | 0-255  |
| `12`              | Tev Color 0 Alpha          | int   | 0-255  |
| `13`              | Tev Color 1 Red            | int   | 0-255  |
| `14`              | Tev Color 1 Green          | int   | 0-255  |
| `15`              | Tev Color 1 Blue           | int   | 0-255  |
| `16`              | Tev Color 1 Alpha          | int   | 0-255  |
| `17`              | Tev Color 2 Red            | int   | 0-255  |
| `18`              | Tev Color 2 Green          | int   | 0-255  |
| `19`              | Tev Color 2 Blue           | int   | 0-255  |
| `20`              | Tev Color 2 Alpha          | int   | 0-255  |
| `21`              | Tev Konstant Color 0 Red   | int   | 0-255  |  
| `22`              | Tev Konstant Color 0 Green | int   | 0-255  |
| `23`              | Tev Konstant Color 0 Blue  | int   | 0-255  |
| `24`              | Tev Konstant Color 0 Alpha | int   | 0-255  |
| `25`              | Tev Konstant Color 1 Red   | int   | 0-255  |
| `26`              | Tev Konstant Color 1 Green | int   | 0-255  |
| `27`              | Tev Konstant Color 1 Blue  | int   | 0-255  |
| `28`              | Tev Konstant Color 1 Alpha | int   | 0-255  |
| `29`              | Tev Konstant Color 2 Red   | int   | 0-255  |
| `30`              | Tev Konstant Color 2 Green | int   | 0-255  |
| `31`              | Tev Konstant Color 2 Blue  | int   | 0-255  |
| `32`              | Tev Konstant Color 2 Alpha | int   | 0-255  |

### <a href="#FLVC"></a>FLVC (Vertex Color)

Related to vertex colors transformations listed below.

| `AnimationTarget` | Name               | Type | Values | 
|-------------------|--------------------|------|--------|
| `0`               | Top Left Red       | int  | 0-255  |
| `1`               | Top Left Green     | int  | 0-255  |
| `2`               | Top Left Blue      | int  | 0-255  |
| `3`               | Top Left Alpha     | int  | 0-255  |
| `4`               | Top Right Red      | int  | 0-255  |
| `5`               | Top Right Green    | int  | 0-255  |
| `6`               | Top Right Blue     | int  | 0-255  |
| `7`               | Top Right Alpha    | int  | 0-255  |
| `8`               | Bottom Left Red    | int  | 0-255  |
| `9`               | Bottom Left Green  | int  | 0-255  |
| `10`              | Bottom Left Blue   | int  | 0-255  |
| `11`              | Bottom Left Alpha  | int  | 0-255  |
| `12`              | Bottom Right Red   | int  | 0-255  |
| `13`              | Bottom Right Green | int  | 0-255  |
| `14`              | Bottom Right Blue  | int  | 0-255  |
| `15`              | Bottom Right Alpha | int  | 0-255  |

### <a href="#FLTP"></a>FLTP (Texture Pattern)

| `AnimationTarget`               | Name    | Values |
|---------------------------------|---------|--------|
| `0`                             | Image 1 |        |
| _the next rows are unconfirmed_ |         |        |
| `1`                             | Image 2 |        |
| `2`                             | Image 3 |        |
| etc.                            | etc.    |        |

### <a href="#FLIM"></a>FLIM (Indirect Texture SRT)

| `AnimationTarget` | Name     | Type  | Values        |
|-------------------|----------|-------|---------------|
| `0`               | Rotation | float | any (radians) |
| `1`               | U scale  | float | any           |
| `2`               | V scale  | float | any           |

### <a href="#FLCT"></a>FLCT (Font Shadow)

| `AnimationTarget` | Name              | Type | Values |
|-------------------|-------------------|------|--------|
| `0`               | Black Color Red   | int  | 0-255  |
| `1`               | Black Color Green | int  | 0-255  |
| `2`               | Black Color Blue  | int  | 0-255  |
| `3`               | Black Color Alpha | int  | 0-255  |
| `4`               | White Color Red   | int  | 0-255  |
| `5`               | White Color Green | int  | 0-255  |
| `6`               | White Color Blue  | int  | 0-255  |
| `7`               | White Color Alpha | int  | 0-255  |

### <a href="#FLEU"></a>FLEU (Extended User Information)

| `AnimationTarget` | Name                                     | Type                                                 | Values |
|-------------------|------------------------------------------|------------------------------------------------------|--------|
| `0`               | Pane SRT                                 |                                                      |        |
| `1`               | Visibility                               |                                                      |        |
| `2`               | Vertex Color / Transparency              |                                                      |        |
| `3`               | Material Color / Text Shadows            |                                                      |        |
| `4`               | Alpha Test                               |                                                      |        |
| `5`               | Texture Pattern                          |                                                      |        |
| `6`               | Texture SRT                              |                                                      |        |
| `7`               | Per-character transformation offset time |                                                      |        |
| `8`               | Extended User Information                | String, Integer value list or Real number value list |        |
| `9`               | Indirect                                 |                                                      |        |

# [Continue to Animations: szs, bflyt, bflan files](./szs-bflyt-bflan.md) :octicons-arrow-right-16:

---

## Special Thanks

- [Switch Toolbox](https://github.com/KillzXGaming/Switch-Toolbox/)
- [3DSkit](https://github.com/Tyulis/3DSkit/)