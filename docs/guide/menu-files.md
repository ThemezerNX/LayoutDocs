##### :octicons-arrow-left-16: [Back to Introduction](index.md)

# Menu Files

In order to work efficiently, it is important to understand the structure of the Switch's menus and get familiar with the theming slang. This and a few following pages will introduce you to some basics.

The Switch's menus can be found in multiple firmware files. Separated into multiple [applets](../definitions.md#applet). The following table shows which menus (supported in themes) can be found where:

| Applet CodeName | TitleID            | Menus                                                   |
| --------------- | ------------------ | ------------------------------------------------------- |
| qlaunch         | `0100000000001000` | common, Home Menu, Lockscreen, All Apps, News, Settings |
| playerSelect    | `0100000000001007` | Player Select                                           |
| myPage          | `0100000000001013` | User Page                                               |

Almost all menu-related applets also have a `common.szs` file that defines structures that should be used throughout all menus in the applet. They often contain the bottom bar (controller status, buttons). Custom themes unfortunately only support modifying the `common.szs` file in the `qlaunch` applet, and not the ones in `playerSelect` or `myPage`.

## Filenames

Every menu has its own file. Here is a list of the supported menus and their filenames:

| Menu             | Filename           |
| ---------------- | ------------------ |
| common (qlaunch) | `common.szs`       |
| Home Menu        | `ResidentMenu.szs` |
| Lockscreen       | `Entrance.szs`     |
| All Apps         | `Flaunch.szs`      |
| News             | `Notification.szs` |
| Settings         | `Set.szs`          |
| Player Select    | `Psl.szs`          |
| User Page        | `MyPage.szs`       |

# [Continue to Filetypes](filetypes.md) :octicons-arrow-right-16:
