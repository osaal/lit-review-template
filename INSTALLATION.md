# Installation

This pipeline presumes the following installed software:

-   Zotero 7.0.27
-   Obsidian 1.12.4
-   Git 2.51.2

It also presumes the following services:

-   [GitHub account](https://github.com/) (or any other source countrol service)
-   [Zotero account](https://zotero.org/)

> [!WARNING]
> **Slightly outdated versions**
>
> This repository uses, for the most part, slightly outdated versions of the software. This is mainly because I use the NixOS operating system, whose default packages are updated generally only every half a year (excluding security updates). Make sure that you download the exact same versions to guarantee compatibility.

## Zotero

**Version:** 7.0.27

Install Zotero for your system [according to the instructions](https://www.zotero.org/download/).

NB: Make sure to install the correct version - the default version is version 8.x, which might not be compatible with this guide.

### Plugin: Better Notes for Zotero, by @windingwind

**Version:** 2.5.13

**NB:** Versions 3.x are no longer compatible with Zotero 7.

Install Better Notes for Zotero from the [GitHub repository](https://github.com/windingwind/zotero-better-notes) by following the instructions on the page, rewritten here for posterity:

1.  Download the correctly versioned `.xpi` file from the Releases tab.
2.  In Zotero, select `Tools > Plugins`.
3.  Under Extensions, press the gear icon and select "Install add-on from file".
4.  Find your `.xpi` file and select it.

> [!TIP]
> **Using Hyprland?**
>
> On at least Hyprland, the gear icon does not work. You can drag and drop the `.xpi` file onto the window instead.

> [!TIP]
> **Using Hyprland, and no drag and drop?**
>
> If you're weird like me, you might not even have a file explorer that allows for drag-and-drop. You can use [`dragon`] to make a draggable version of the file, and then drop it onto the area, e.g.:
>
> `dragon-drop better-notes-for-zotero.xpi`
>
> or
>
> `dragon better-notes-for-zotero.xpi`
>
> The former is NixOS-specific, the latter should be OS-independent.
>
> Don't ask me how long it took me to figure all of this out.

> [!TIP]
> **Still not working?**
>
> It might be possible to manually install a Zotero plugin, but I have not verified this method. Zotero seems to install its plugins directly as `.xpi` files (with possible renaming?) in the following path on Unix-like systems (Linux, MacOS):
>
> `$HOME/.zotero/$PROFILE_NAME/extensions/$PLUGIN_NAME.xpi`
>
> `$HOME` is the path to the user's home directory. `$PROFILE_NAME` seems to be a randomly generated profile name (you can have multiple user profiles in Zotero, it seems). `$PLUGIN_NAME` seems based on something the plugin author has registered themselves. For instance, on my system, Better Notes showed up as "Knowledge4Zotero@windingwind.com.xpi".
>
> Theoretically, then, you could simply create the `extensions` folder (if it does not exist), and copy the `.xpi` file there. No guarantees if this works, though!

## Obsidian

**Version:** 1.12.4

Install Obsidian by selecting the appropriate version and packaging format for your system (`.exe` for Windows) [from the GitHub release page](https://github.com/obsidianmd/obsidian-releases/releases).

## Git

**Version:** 2.51.2

Install Git [from the homepage](https://git-scm.com/) or using your system's package repository (Linux/MacOS with Homebrew/Windows with Chocolatey).

The version should not matter here, as Git pretty much never changes drastically. This pipeline also uses no advanced or new Git features - we simply need basics like `init`, `add`, `commit`, and `push`.
