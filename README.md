<h1 align="center">Colemak Wide for EPKL (Ergonomic Mod)</h1>

<p align="center">
    <img width="152" height="152" src="https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/EPKL-icons/Black.png">
    <img width="152" height="152" src="https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/EPKL-icons/Gold.png">
    <img width="152" height="152" src="https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/EPKL-icons/White.png">
</p>

# 1. Project Information

## 1.1 Description

This project is an implementation of the Wide Ergonomic Modification (or simply, ‘ergo mod’) of the Colemak alternative keyboard layout for the EPKL Portable Keyboard Layout software (‘EPiKaL’ or ‘EPKL’ for short) running on Windows operating system (supports Windows 7+).

The ergo mod moves the right hand position one key closer to <kbd>Enter</kbd>. This change allows for easier and more comfortable access to <kbd>AltGr</kbd> (or <kbd>RAlt</kbd>) to use dead keys and extend layers (keyboard layers with extended functionalities). It also changes the position of some keys with punctionation marks, bringing them to the centre of the keyboard. This allows for removing some strains off of the pinky fingers. The ergo mod also helps to maintain a better back posture due to the typer's hands being placed further apart letting their shoulders to distribute weight more evenly.

The project was published on GitHub in 2020, but its creation goes a few years back. Its conception was inspired by other, similar Colemak ergonomic modifications; specifically, the implementations of Øystein Bech ‘[DreymaR](https://github.com/DreymaR)’ Gadmar and [stevep99](https://github.com/stevep99). Some of the files are forked from these people's source codes. The goal is to provide compatibility between my implementation of the Colemak Wide Ergonomic Mod and the EPKL application, while supporting physical keyboards of the US ANSI 101/104-key and European ISO 102/105-key form factors.

## 1.2 Keyboard Layouts

Key changes on the keyboard layouts from the original Colemak layout were kept to a minimum to help typists with easier transition when switching between the original Colemak layout and its Wide ergonomic implementation. This is one of the arguments as to why the position of the apostrophe key (<kbd>'</kbd>) was not changed with the backslash (<kbd>\\</kbd>) on ISO keyboards, which would have made the apostrophe more comfortable to type. The ISO 102 key (not available on ANSI boards) kept its original key maps of standard Colemak, too. Another argument is that once a modification of any software moves further away from the original source the less support it can receive and only limited help may be provided to solve problems.

Modificationss done to the keyboard layouts' configuration files made it possible to apply additional layout mods using the `mapSC_layout` variable in the `Layout.ini` files. Read the files' documentation to learn more about this variable and its sister: `mapSC_extend`. Therefore, it is now possible to combine the Wide Ergo Mod with the DH and Angle mods, too.

### 1.2.1 Colemak Wide (US)

The US variant of the Wide Ergo Mod for Colemak follows the original key maps of Colemak. Check out the Colemak website's [Multilingual](https://colemak.com/Multilingual) page or `Layouts\Colemak-Wide\Layout.ini` for an overview of the available dead keys. So it is basically the original Colemak layout with only the Wide mod applied.

The image below showcases the keyboard layout for US ANSI 101/104-key keyboards, but it can be used on European ISO 102/105-key boards, too. The ISO 102 key (between <kbd>LShift</kbd> and <kbd>Z</kbd> on ISO boards) follows the same key maps of the <kbd>-</kbd> key on the numeral row, so that ISO board users wouldn't have any benefits over typists on ANSI boards.

![ANSI standard keyboard layout image](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/Keyboard-layouts/Keyboard-layout-ansi-layer0.png)

### 1.2.2 Colemak Wide (UK)

The UK variant of the Wide Ergo Mod for Colemak follows the original key maps of Colemak with the additional benefit of having some punctuation marks and characters in their UK QWERTY positions:

* <kbd>Shift+2</kbd> produces "

* <kbd>Shift+3</kbd> produces £

* <kbd>Shift+’</kbd> produces @

* The US <kbd>\\</kbd> key is replaced with the UK <kbd>#</kbd> key.

* The ISO 102 key follows the same key maps of the UK QWERTY keyboard layout.*

The image below showcases the keyboard layout for European ISO 102/105-key keyboards, but it can also be used on US ANSI 101/104-key boards.

![ISO standard keyboard layout image](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/Keyboard-layouts/Keyboard-layout-iso-layer0.png)

\* Even though US ANSI keyboards lack the ISO 102 key, typing backslash (\\) and bar (|) characters is still possible on the <kbd>#</kbd> key – it follows the `# ~ \ |` maps on base (layer 0), Shift (layer 1), AltGr (layer 6), and AltGr+Shift (layer 7).

### 1.2.3 Colemak Wide (Mini)

This variant of the Wide Ergo Mod for Colemak is a minimalist implementation. It only moves the keys around on the keyboard, but they follow the host layouts punctuation mark, Shift (layer 2), AltGr (layer 6), and AltGr+Shift (layer 7) key maps. Examples:

* If the Windows keyboard layout is US QWERTY, <kbd>AltGr+S</kbd> produces nothing

* If the Windows keyboard layout is Polish (Programmers), <kbd>AltGr+S</kbd> produces ś

* If the Windows keyboard layout is Dutch (QWERTY), <kbd>AltGr+S</kbd> produces ß

It is important to note that some characters of the host layout located on the ISO 102 key are lost on ANSI boards. Also, it is very important to always select the correct layout type for your keyboard as ANSI and ISO layouts send different VirtualKey codes – refer to section [2.4.3 Colemak Wide (Mini): ANSI vs ISO Keyboards](https://github.com/szabog/colemak-wide-epkl/blob/main/README.md#243-colemak-wide-mini-ansi-vs-iso-keyboards) for instructions.

The image below showcases the keyboard layout for European ISO 102/105-key keyboards. The keys with the ‘OEM’ text follow the character maps of the host layout.

![ISO Mini standard keyboard layout image](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/Keyboard-layouts/Keyboard-layout-mini-iso-layer0.png)

### 1.2.4 Colemak Wide (SymGr)

My personal implementation of an alternative AltGr and dead key mod for Colemak's Wide Ergo Mod. The goals of the modification are:

1. Move the symbols that are found under the shifted positions of the numeral keys to the AltGr (layer 6) and AltGr+Shift (layer 7) layers of the alphabetical keys. As a consequence, the <kbd>[</kbd> and <kbd>]</kbd> keys have lost their dedicated key positions – their characters (the brackets) are now accessible on the AltGr layer – allowing dead keys to be placed onto these keys.

2. Group majority of dead keys onto deadicated keys to provide easier access to them and allow for quicker typing of foreign languages other than English.

**Notes:**

* This keyboard layout is under active development – keys and characters may switch positions any time as I'm fine tuning things.

* The dead key positions are designed to my liking – as I frequently type in languages other than English, the dead key positions are placed in accordance with my preferences.

* You're welcome to fork it – if you find this mod inspiring, but want to make your own changes on it, then go ahead and modify it!

The image below showcases the keyboard layout for US ANSI 101/104-key keyboards, but it can be used on European ISO 102/105-key boards, too.

![ANSI SymGr standard keyboard layout image](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/Keyboard-layouts/Keyboard-layout-symgr-ansi-all-layers.png)

## 1.3 File and Directory Overview

#### Directory Tree

```
../
├── Assets/
│   ├── Icons/
│   │   ├── C/..
│   │   └── Paint.NET project files/..
│   └── Images/
│       ├── EPKL-icons/..
│       ├── Extend-layers/..
│       └── Keyboard-layouts/..
├── Files/
│   ├── Icons/..
│   ├── Languages/..
│   ├── _eD_Remap.ini
│   └── EPKL_Tables.ini
├── Layers/
│   ├── Dead_Keys.ini
│   └── Extend_Layers.ini
├── Layouts/
│   ├── Colemak-Wide
│   │   └── Layout.ini
│   ├── Colemak-Wide-Mini
│   │   └── Layout.ini
│   ├── Colemak-Wide-SymGr
│   │   └── Layout.ini
│   └── Colemak-Wide-UK
│       └── Layout.ini
├── EPKL_Layouts_Default.ini
├── EPKL_Settings_Default.ini
├── LICENSE
├── README.md
└── .gitignore
```

| ***EPKL files*** |  |  |
| :--- | :--- | :--- |
| **File name** | **Description** | **Comments** |
| `EPKL_Layouts_Default.ini` | EPKL global default keyboard layout configuration file with settings for Colemak with hardcoded Wide Ergo Mod. Settings of this file will be overwritten by `Layout.ini` and `EPKL_layouts_override.ini`. | This project does not contain an `EPKL_layouts_override.ini` file. To check which settings are being overwritten by a `Layout.ini` file, you must compare `EPKL_Layouts_Default.ini` and the correct `Layout.ini` files. |
| `EPKL_Settings_Default.ini` | EPKL settings and behaviour configuration file for the app and extend layer modifiers. | Controls the general behaviour of EPKL, the shortcuts to access its different functions, and the keys that provide access to different extend layers as well as these modifier keys' behaviour. |
| `Files\_eD_Remap.ini` | Key remap definitions. | Responsible for defining remap rotations. This file is pulled without changes from DreymaR's [BigBagKbdTrixPKL](https://github.com/DreymaR/BigBagKbdTrixPKL) repository. All rights belong to its author, © DreymaR (Øystein B Gadmar, 2015–). |
| `Files\EPKL_Tables.ini` | EPKL Information table definitions | Fixes a rare error when launching `EPKL.exe`. This file is pulled without changes from DreymaR's [BigBagKbdTrixPKL](https://github.com/DreymaR/BigBagKbdTrixPKL) repository. All rights belong to its author, © DreymaR (Øystein B Gadmar, 2015–). |
| `Files\Icons` | EPKL icon files. | The EPKL notifiation area icon may be customised for every keyboard layout individually. These files are Public Domain. |
| `Layers\Dead_Keys.ini` | Dead key definitions for the project's keyboard layouts (US and UK variants). | EPKL dead key configuration file with the original dead keys from PKL for Colemak keyboard layout. |
| `Layers\Extend_Layers.ini` | EPKL extend layer configuration file for Colemak keyboard layout with hardcoded Wide Ergo Mod. | Extend layer modifiers are defined in `EPKL_Settings_Default.ini`. Extend key is defined in `EPKL_Layouts_Default.ini`. |
| `Layouts\*` | Directory for storing keyboard layout files. | Each layout has its own folder. |
| `Assets\*` | Holds miscellaneous data files for the GitHub repository. | These files aren't used or detected by EPKL. The keyboard layout image files were created using [Keyboard Layout Editor](http://keyboard-layout-editor.com), and the EPKL app icons were created in [Paint.NET](https://getpaint.net). |

:arrow_heading_up: [**Back to top**](https://github.com/szabog/colemak-wide-epkl#1-project-information)

# 2 Installation and Configuration

## 2.1 EPKL Installation

I don't use Windows anymore, therefore don't have the time to test future EPKL versions.

~~EPKL Portable Keyboard Layout (‘EPKL’), as the name implies, is a portable program that does not require installation or administrator privileges to run. To download and run EPKL head over to DreymaR's [BigBagKbdTrixPKL](https://github.com/DreymaR/BigBagKbdTrixPKL) repository and follow his instructions. I recommend downloading the latest binary release from the repository as this project's configuration files are kept up-to-date with those versions only. They are rarely in-sync with EPKL's ‘in between’ version commits.~~

**NOTICE:** This project is not planning to contain the `EPKL.exe` or any other binary executables to run EPKL.

## 2.2 Project Files Setup

If you haven't downloaded EPKL Portable Keyboard Layout (‘EPKL’) software yet, then check out the section above to get it.

### Stable Releases (‘Production Ready’):

~~I recommend downloading a release of this repository that matches your EPKL software version (enclosed in parenthesis) - see [Releases](https://github.com/szabog/colemak-wide-epkl/releases) page. These releases have been tested to work with the intended EPKL version, and are certified to be ready for day-to-day use without causing any major disturbances.~~

The currently supported EPKL version is 1.3.1.

### Snapshot Releases (‘Experimental’):

**IMPORTANT!** Follow the instructions below if you're 100% sure you want to get the latest version of the project files (usually compatible with the latest release version of EPKL). Otherwise download the release that matches your current EPKL version (instructions are above). Having mismatching project file and EPKL versions may lead to reduced functionality, software instability, and may introduce unintended bugs.

1. Download the contents of this repository by clicking the ‘:arrow_down: Code’ button then selecting ‘Download ZIP’. Save the zip archive anywhere to your computer.

2. Extract the archive and copy its content to the folder where `EPKL.exe` is located. **Important:** Make a backup of the current content of the folder as several files must be overwritten in order to make Colemak with the Wide Ergo Mod work. You may also try to implement Colemak with Wide Ergo Mod into the original EPKL files, but that requires advanced knowledge EPKL's configuration.

3. Double click `EPKL.exe` to run the software and activate the keyboard layout.

**To quit EPKL completely:** Right click on EPKL's icon ![PKL on icon](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/EPKL-icons/Black-small-on.png) in the notification area and select **Exit**.

**To suspend EPKL (disables the active keyboard layout without closing the app):** Press the <kbd>Ctrl+Shift+Del</kbd> key combinations or right click on EPKL's icon ![PKL on icon](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/EPKL-icons/Black-small-on.png) in the notification area and select **Suspend**. If EPKL's icon changes to ![PKL off icon](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/EPKL-icons/Black-small-off.png) it means only your Windows layout is active.

## 2.3 EPKL Configuration

The configuration of EPKL Portable Keyboard Layout software is primarily performed in 2 files: `EPKL_Settings_Default.ini` and `EPKL_Layouts_Default.ini`. Head over to DreymaR's [BigBagKbdTrixPKL](https://github.com/DreymaR/BigBagKbdTrixPKL) repository which explains in great detail what the different settings in these files do and what their possible values are, then you can make your own changes.

## 2.4 Project Files Configuration

You can make any desired changes to the project files, but if you don't know what you're donig and mess something up, I or other people may not be able to assist you.

The `EPKL_Layouts_Default.ini` file is configured to load the Colemak Wide (US variant), Colemak Wide (Mini), and Colemak Wide (SymGr) keyboard layouts by default. Check out the sections below how to add and remove layouts or switch to the UK variant of the Colemak Wide Ergo Mod.

### 2.4.1 Add or Remove Keyboard Layouts

1. Open `EPKL_Layouts_Default.ini` and navigate to the line that starts with `layout =`.

2. To add a new keyboard layout for EPKL to load: Add the name of the folder where the `Layout.ini` resides (`Layouts\<layout-name>\Layout.ini`) after the equal (=) sign. To add multiple layouts, separate them with commas (,) without spaces (e.g., `Keyboard-Layout1,Keyboard-Layout2,Keyboard-Layout3`).

3. To remove a keyboard layout: Simply delete its name after the equal (=) sign.

4. Save your changes, then restart EPKL or right click on EPKL's icon ![PKL on icon](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/EPKL-icons/Black-small-on.png) in the notification area and select **Refresh EPKL**.

If you add multiple keyboard layouts for EPKL to load, you can switch between them using the <kbd>Ctrl+Shift+PgUp</kbd> key combination. Alternatively, right click on EPKL's icon ![PKL on icon](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/EPKL-icons/Black-small-on.png) in the notification area and hover your mouse cursor over **Layouts**. Then click the name of the keyboard layout you wish to activate.

If you receive a message from EPKL that says *“EPKL_Settings_Default.ini: Non-existing menu item specified as default!?”*, it's only a warning and you can dismiss it. EPKL is notifying you that the assigned action when EPKL's icon ![PKL on icon](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/EPKL-icons/Black-small-on.png) in the notification area is double clicked points to a not existing menu entry. You can specify a new action or change the default one in the `EPKL_Settings_Default.ini` file at the line that starts with `trayMenuDefault	=`. Check out DreymaR's [BigBagKbdTrixPKL](https://github.com/DreymaR/BigBagKbdTrixPKL) repository for the possible values of this setting.

### 2.4.2 Activate or Switch to UK Variant

1. Open `EPKL_Layouts_Default.ini` and navigate to the line that starts with `layout =`.

2. Rename `Colemak-Wide` to `Colemak-Wide-UK`.

3. If you only wish to run the UK variant without the US, Mini or SymGr ones, then you may comment out the line with `layout = Colemak-Wide-Mini,Colemak-Wide` (put a semicolon (;) to the beginning of the line), and uncomment the one under it that says `layout = Colemak-Wide-UK`.

4. Save your changes, then restart EPKL or right click on EPKL's icon ![PKL on icon](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/EPKL-icons/Black-small-on.png) in the notification area and select **Refresh EPKL**.

### 2.4.3 Colemak Wide (Mini): ANSI vs ISO Keyboards

The Mini keyboard layout variant of the Colemak Wide Ergo Mod is configured for ANSI keyboards by default (because that's what I use), but if you have an ISO keyboard, you must change the keyboard layout type in `Layout.ini`. Instructions:

1. Open `EPKL_Layouts_Default.ini`.

2. Find the line that starts with `KbdType =`.

3. Change the `ANS` value to `ISO` for European ISO 102/105-key keyboards.

4. Save your changes, then restart EPKL or right click on EPKL's icon ![PKL on icon](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/EPKL-icons/Black-small-on.png) in the notification area and select **Refresh EPKL**.

:arrow_heading_up: [**Back to top**](https://github.com/szabog/colemak-wide-epkl#1-project-information)

# 3. Extend Layers

Another important aspect of the Colemak Wide Ergo Mod (besides its implementation) is the utilisation of multiple ‘extend layers’. They provided extended functionalities of your keyboard using AutoHotkey technology. The backslash (<kbd>\\</kbd> or <kbd>#</kbd> on UK variant) and ISO 102 key (between <kbd>LShift</kbd> and <kbd>Z</kbd>) do not have any functions mapped to them, because backslash changes positions between US ANSI 101/104-key and European ISO 102/105-key keyboards, and the ISO key is absent on ANSI boards.

* To access the base extend layer: Hold the extend key (<kbd>Caps Lock</kbd> by default).

* To access additional extend layers: Hold a modifier key and hold the extend key, then release the modifier key and only hold extend. Release the extend key to go back to the base keyboard layout.

Extend key is defined in `EPKL_Layouts_Default.ini`.  
Extend layer modifiers are defined and configured in `EPKL_Settings_Default.ini`.  
Extend layers are configured in `Layers\Extend_Layers.ini`.

## 3.1 Base Layer

![Base extend layer image](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/Extend-layers/Extend-layer-base-image.png)

| ***Legends*** |  |  |
| :--- | :---: | :--- |
| **Keys** | **Category** | **Description** |
| ![Base layer Ctrl shortcuts image](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/Extend-layers/Extend-layer-base-ctrl-shortcuts.png) | Ctrl Shortcuts | <kbd>Ctrl+A</kbd> (select all), <kbd>Ctrl+X</kbd> (cut), <kbd>Ctrl+C</kbd> (copy), <kbd>Ctrl+V</kbd> (paste)<br><kbd>Ctrl+F</kbd> (find), <kbd>Ctrl+S</kbd> (save), <kbd>Ctrl+Z</kbd> (undo), <kbd>Ctrl+Y</kbd> (redo) |
| ![Base layer F1 key image](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/Extend-layers/Extend-layer-base-f-function-f1.png) .. ![F12 key image](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/Extend-layers/Extend-layer-base-f-function-f12.png)| F* Function Keys | <kbd>F1</kbd> to <kbd>F12</kbd> |
| ![Base layer misc. keys image](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/Extend-layers/Extend-layer-base-misc.png) | Miscellaneous | Activate the Base Extend Layer (<kbd>Caps Lock</kbd> by default)<br><kbd>Escape</kbd>, <kbd>Insert</kbd>, <kbd>Ctrl+Break</kbd><br><kbd>Scroll Lock</kbd>, <kbd>Pause/Break</kbd>, <kbd>Num Lock</kbd><br><kbd>PrintScreen</kbd> |
| ![Base layer modifier keys image](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/Extend-layers/Extend-layer-base-modifiers.png) | Modifiers | <kbd>Win</kbd>, <kbd>Alt</kbd>, <kbd>Ctrl</kbd>, <kbd>Shift</kbd> |
| ![Base layer multimedia keys image](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/Extend-layers/Extend-layer-base-multimedia.png) | Multimedia | Mute, volume down, volume up, open default media player<br>Play, previous, next, pause/stop |
| ![Base layer navigation keys image](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/Extend-layers/Extend-layer-base-navigation.png) | Navigation | Left, down, up, right<br><kbd>Home</kbd>, <kbd>End</kbd>, go back, go forward<br><kbd>PgDn</kbd>, <kbd>PgUp</kbd>, scroll down, scroll up |
| ![Base layer text editing keys image](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/Extend-layers/Extend-layer-base-text-editing.png) | Text Editing | <kbd>Tab</kbd>, <kbd>Caps Lock</kbd>, <kbd>Backspace</kbd>, <kbd>Delete</kbd><br><kbd>Enter</kbd> |
| ![Unmapped keys image](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/Extend-layers/_extend-layer-unmapped.png) | Unmapped Keys | Keys without any functions mapped to them. |

## 3.2 Numpad Layer

![Numpad extend layer image](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/Extend-layers/Extend-layer-numpad-image.png)

| ***Legends*** |  |  |
| :--- | :---: | :--- |
| **Keys** | **Category** | **Description** |
| ![Numpad layer misc. keys image](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/Extend-layers/Extend-layer-numpad-misc.png) | Miscellaneous | Layer activator (<kbd>RShift</kbd>) |
| ![Numpad layers numerals, dividers and Unicode characters image](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/Extend-layers/Extend-layer-numpad-numerals.png) | Numerals, Dividers and Unicode Characters | <kbd>0</kbd> to <kbd>9</kbd><br>tilde, exclamation mark, at sign, pound<br>dollar sign, percent, equals, backslash<br>less than, greater than, colon, quote<br>comma, dot|
| ![Numpad layer operators image](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/Extend-layers/Extend-layer-numpad-math-operators.png) | Math Operators | Multiple, divide, add, subtract |

## 3.3 Mouse Layer

![Mouse extend layer image](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/Extend-layers/Extend-layer-mouse-image.png)

| ***Legends*** |  |  |
| :--- | :---: | :--- |
| **Keys** | **Category** | **Description** |
| ![Mouse buttons image](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/Extend-layers/Extend-layer-mouse-buttons.png) | Buttons | Left click<br>Middle click, right click |
| ![Mouse layer misc. keys image](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/Extend-layers/Extend-layer-mouse-misc.png) | Miscellaneous | Layer activator (<kbd>AltGr</kbd>/<kbd>RAlt</kbd>) |
| ![Mouse layer navigation image](https://raw.githubusercontent.com/szabog/colemak-wide-epkl/main/Assets/Images/Extend-layers/Extend-layer-mouse-navigation.png) | Navigation | Left, down, up, right |

:arrow_heading_up: [**Back to top**](https://github.com/szabog/colemak-wide-epkl#1-project-information)

# 4. Contributions

You may contribute to the project in the following ways through pull requests:

* Creation of EPKL Portable Keyboard Layout keyboard layout and extend layer help images.

* Creation of EPKL Portable Keyboard Layout app icons.

* Improving the project documentation.

:arrow_heading_up: [**Back to top**](https://github.com/szabog/colemak-wide-epkl#1-project-information)

# 5. Licenses and Forking

This project is generally licensed under GNU General Public License version 3.0 (also known as ‘GPLv3’) with the following exceptions:

* Contents of `Assets` and `Files\Icons` are Public Domain; however,

* Contents of `Files\Languages`, `Files\_eD_Remap.ini`, and `Files\EPKL_Tables.ini` retain their own licenses as they are pulled in directly from the EPKL Portal Keyboard Layout's repository.

Please note, source files of the EPKL Portable Keyboard Layout software won't be bundled in this repository or in its releases in source code, compiled binary or any other format.

The project files may be forked according to their license guidelines.

:arrow_heading_up: [**Back to top**](https://github.com/szabog/colemak-wide-epkl#1-project-information)
