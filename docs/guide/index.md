# Getting Started

For this guide it is expected that you already have basic knowledge on how to install themes. If you don't, it is recommended to read [this page](https://nh-server.github.io/switch-guide/extras/theming/) to at least get a basic idea of what you're getting yourself into ;P

### What You'll Need

-   A hacked Switch, connected to LAN (use, for example, [90dns](https://gbatemp.net/threads/90dns-dns-server-for-blocking-all-nintendo-servers.516234/) to block connections to Nintendo)
-   A Windows computer
-   [NXThemes Installer](https://github.com/exelix11/SwitchThemeInjector/releases/latest) version ≥2.6.2 (not out yet)
    -   You probably already have this.
    -   You only need the `NXThemesInstaller.nro`.
    -   You can also install this homebrew app from the HB App Store.
-   [LayoutKit](https://github.com/ThemezerNX/LayoutKit/releases/latest)
    -   LayoutKit requires a Windows installation. While this guide might be built around LayoutKit, everything should be doable without it.
-   [sys-ftpd with reboot support](https://github.com/ThemezerNX/sys-ftpd-light-reboot/releases/latest)

<!-- prettier-ignore -->
!!! Info
    LayoutKit comes packed with the most-used tools. If you are unable to or don't want to use LayoutKit, see [this list of tools](../extras/tools.md), which includes the ones used by LayoutKit.

## Initial Setup

1. Download and install LayoutKit.
2. Install the NXThemes Installer.
3. Make sure the NXThemes Installer is working and you're running version ≥2.6.2.

    <!-- prettier-ignore -->
    !!! Warning
        This version has not been released yet. Currently, the player select and user page menu are only extracted when you install a theme for them. You can do that, or wait for the new version to release. When it has, you can go to `Firmwares`, click 'Open Folder' and place `Psl.szs` and `MyPage.szs` there.

4. Open the NXThemes Installer and follow the instructions if this is the first time you open it.
5. Copy the `SD://themes/systemData` folder to your computer.
6. Copy the contents of the sys-ftpd archive to the root of your MicroSD.
    - It is recommended that you change sys-ftpd's password. Do this by editing `SD://config/sys-ftpd/config.ini`. Remember the value you set.

## Configuring LayoutKit

1. Read the 'Info' tab to get familiar with LayoutKit's features.
2. Go to the 'Settings' tab and fill in your Switch's IP address. You can find it by going to `System Settings > Internet` under 'Connection status'.
3. Configure the password if you changed it from the default (`nxthemer`). Changes are saved automatically.
    - The loader in the top right of the application should now stop spinning and turn green. If it does not, check your FTP details.
4. Go to the 'Firmwares' tab and click 'Import'. CLick the box that says 'ver.cfg path' and navigate to the `ver.cfg` in the `systemData` folder you copied earlier.
    - The version should automatically be configured.
    - If you already have this version imported, there is no need to do so again. LayoutKit will make sure the stock files stay unmodified (except if you manually start editing the application data ofcourse).
5. Click 'Import'.
6. Go to the 'Projects' tab and modify the settings on the 'Quick Settings' card to your likings. You can see that there also is a button to manually restart the console when it is connected. The install
7. On the 'Project Browser' tab click 'New' and fill in the fields. Select the menus you want to include in your environment (you can change this later). The new project is automatically selected.
8. You can apply an existing layout to any of the menus by clicking 'Apply JSON'. This will overwrite the file.

    <!-- prettier-ignore  -->
    !!! Important
        You will always have to re-open Switch-Toolbox (see next step) after having applied a layout.

9. Click any of the blue buttons with a wrench icon. This will open the Switch-Toolbox, in which you can make modifications to the menus.
    1. Go to `Settings > Main Settings > Editor`, check `Always compress on save`, and click 'Save'. This will decrease the amount of clicks required when saving a file.
    2. If you now double-click any of the `bflyt` or `bflan` files in the respective `blyt` and `anim` folders, Switch-Toolbox will open a second window.
    3. After you made changes, go to `File > Save Layout` in the second window.
    4. When you're done making changes to the `bflyt` or `bflan` files, go to `File > Save` in the first window.
    5. The file on the disk is now updated.
10. LayoutKit will detect changes made to the files of the current active project, meaning that after you saved an `szs` the 'Install' button on the 'Quick Settings' card will light up.
    - If you enabled 'Install on Change', the button show a loading animation automatically and become greyed out again.
11. You can export all changes that were made as a layout by clicking 'Save JSON'. Make sure you edit it afterwards and set the your name as author!

### Optional Steps

-   If you did not include all menu's when creating the project you can click the green pencil button next to 'Copy' and select more.
-   You can copy a project if you want to test something and not mess up your original. You can do so by clicking 'Copy'.
-   You can delete firmwares, projects, or project menus by clicking the red delete button.

<!-- prettier-ignore -->
!!! Tip
    Any item that is deleted will be moved to the trash, so if you were to accidentally delete something you're in luck! Restoring the files from your trash and clicking the refresh button is enough.

# [Continue to Menu Files](menu-files.md) :octicons-arrow-right-16:
