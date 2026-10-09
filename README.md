


# MerkUI

[Download MerkUI Installer here for easier install & auto updates ](https://github.com/MerkXL/MerkUI/releases/tag/MerkUI-Installer)


[Latest Version here](https://github.com/MerkXL/MerkUI/releases/tag/v1.1.13)

A custom user interface for Anarchy Online on the ProjectRK client.

MerkUI replaces AO's status, target, team and timer bars with clean, flat ones, adds buff and debuff trackers, combat text, a mission window and resizable action bars, gives the login and character screens a new look with moving backgrounds, and puts every setting in the game's own options window (F10).

**Version:** 1.1.10
**Status:** first community release of a personal UI, tested by a small number of players. Back up before you install.

---

## What you get

| Area | What it does |
|---|---|
| **Status Bars** | HP, Nano, XP and Alien XP as separate bars you can size and place. XP shown as a percentage. Optional black text outline. |
| **Target Bar** | Target name, level (in the same con colour AO's own Target Bar uses) and HP in percent and numbers. Optional black text outline. |
| **Team Bars** | Six team member bars with HP and Nano. Click a bar to target that member. |
| **Raid Bars** | Compact frames for the whole raid, shown when you are in a raid. |
| **Timer Bars** | Attack, Special, Nano, Item and Reload timers in matching colours, plus an **Equip** bar that shows equip time. |
| **Buffs and Debuffs** | Five independent trackers: Player Buffs, Player Debuffs, Target Buffs, Target Debuffs and Pet Buffs. Each has an icon that drains as the effect runs out, a timer, a tooltip and a duration filter. |
| **Pet Bars** | A bar for each of your pets with its name and HP: Attack Pet 1 and 2, Healing Pet, Support Pet and Charmed Pet, each with its own place, size and text settings (or set them all at once under Size → Global). Click a bar to target that pet. Pet Buffs can show or hide each kind of pet. |
| **Combat Text** | Damage dealt and healing received as floating text, with a separate large "sticky" number for critical hits. |
| **Missions** | A mission window with description, rewards and item icons, and an on-screen mission tracker. |
| **Action Bars** | Up to five bars, each with its own number of buttons, buttons per row, button size and spacing. |
| **Loading screen** | A custom loading image with a soft pulse. |
| **Login screen** | A new login box and a moving background (video). |
| **Character screen** | A new character list that grows with the number of characters, a new button bar, and a moving background. The "Please wait..." box during login is hidden. |
| **Renderer settings** | With the [ao-vk](https://github.com/wannabuh/ao-vk) renderer installed, its settings are under **F10 → MerkUI → Renderer**: presets and one page per section (Lighting, Shadows, HDR and effects, and so on). Changes apply at once and ao-vk saves them in `randy-vk.ini`. No AOReloaded `version.dll` is needed. Without ao-vk these pages are not shown. |

**With every preview enabled:**
<img width="2559" height="1439" alt="Preview" src="https://github.com/user-attachments/assets/f0351660-0eb5-404b-83c4-4d8790e841f2" />

**F10 settings:**

<img width="891" height="599" alt="F10" src="https://github.com/user-attachments/assets/1e41fb7a-cd9d-4fc0-ad79-acd90549c019" />

## Requirements

- Anarchy Online on the **ProjectRK** client, Windows.
- The exact client version MerkUI was built for. On any other version MerkUI's code checks the game files, finds they do not match and does nothing. The game then runs with only the graphics and layout files, without the bars and trackers.
- For the moving backgrounds: Windows' own video support (Media Foundation). It is part of normal Windows 10 and 11. On the "N" editions of Windows it has to be added with Microsoft's Media Feature Pack. Without it you get still pictures instead.

---

## Install

Everything goes in **one** place: the game folder, the one that contains `AnarchyOnline.exe`.

Anarchy Online keeps GUI skins in a profile folder under `%LOCALAPPDATA%\Funcom\Anarchy Online`, and there can be several of those with code names. You do not have to find the right one: MerkUI asks the game which one it uses and copies its skin there by itself.

1. **Close the game.**
2. Unpack the whole zip somewhere, for example your Desktop.
3. Double-click **`Install.bat`** in the unpacked `MerkUI` folder.
   - It looks for the game in the usual ProjectRK folder. If it does not find it, it asks you for the folder that contains `AnarchyOnline.exe`.
   - If Windows does not let it write to the game folder, it tells you so. Right-click `Install.bat` and choose **Run as administrator**.
   - If the game folder already has a `version.dll` from something else, it is kept as `version.dll.bak`.
4. **Start the game** and wait for the login screen. MerkUI now copies its skin into the profile folder this game uses.
5. **Quit the game.**
6. Open the **PRK launcher** and go to **Settings > GUI > GUI Skin**. Choose **MerkUI**.
7. **Start the game again.** From now on the login screen, the character screen and everything in game use MerkUI.

On the very first start, before you have chosen the skin, the login and character screens are only half dressed: backgrounds and frames are there, the new buttons are not. That is expected and is gone after step 7.

To check that it worked: press **F10** in game. There should be a **MerkUI** entry in the list on the left.

MerkUI's skin comes with its own starting values for a fresh profile: the Control Center fade settings (low fade, high fade, fade delay) at their maximum, and all sound volumes at 50%. Settings you have already changed yourself are kept.

### Manual install

1. Close the game.
2. If your game folder already has a `version.dll`, rename it to `version.dll.bak`.
3. Copy everything inside the `files` folder into the game folder, next to `AnarchyOnline.exe`. Then follow steps 4 to 7 above.

When you are done it should look like this:

```
<game folder>\
  AnarchyOnline.exe
  version.dll
  MerkUI_Skin\                      <- the skin, copied on by MerkUI itself
  MerkUI_LoginBackground.bmp
  MerkUI_LoginBackground.mp4
  MerkUI_CharacterBackground.bmp
  MerkUI_CharacterBackground.mp4
  MerkUI_LoginFrame.bmp
  MerkUI_CharacterPanelTop.bmp
  MerkUI_CharacterPanelMiddle.bmp
  MerkUI_CharacterPanelBottom.bmp
  MerkUI_CharacterBar.bmp
```

After the first start the skin is also here, put there by MerkUI:

```
%LOCALAPPDATA%\Funcom\Anarchy Online\<code>\client\Gui\MerkUI\
```

---

## First setup

Everything is under **F10 → MerkUI**. Nothing needs editing in files.

A good order for a first setup:

1. **Timer Bars** → turn on *Preview Bars* and drag the timers where you want them.
2. **Status Bars**, **Target Bar**, **Team Bars** → use each page's *Preview* to see the bars without needing a target or a team.
3. **Buffs and Debuffs → General** → turn on *Preview All Buffs and Debuffs*. All five trackers appear with sample effects and a name label. Drag each one into place, then turn preview off.
4. **Action Bars** → enable the bars you want and set buttons, rows and size.
5. **Combat Text** and **Missions** → enable and place.

### Moving things

- Most elements are dragged with the left mouse button while their **Preview** is on, or at any time if they are not locked.
- Every page also has X and Y sliders for exact placement.
- **Lock** options stop accidental dragging once you are happy.

### Useful to know

- **Shift + left click** on a buff or debuff opens AO's own Info window for it.
- **Copy from ...** on a tracker page copies the look (size, font, spacing) from another tracker without moving it.
- **Reset This Tracker** puts one tracker back to its defaults.
- Each tracker's **Duration Filter** hides effects longer than the number of minutes you set. 0 shows everything.

---

## Action Bars: how rows and hotkeys work

- **Number of Buttons** is 1 to 10 per bar.
- **Buttons Per Row** only accepts values that divide the number of buttons evenly, so every row is full. With 10 buttons that is 1, 2, 5 or 10. The slider jumps to the nearest valid value.
- **Button Size** uses even numbers only (16 to 64). 0 means AO's own size.
- **Hotkeys 1 to 10 follow what you see.** Key 6 is always the sixth button on screen, counted row by row.

One thing behaves differently from what you might expect. AO stores each page of a hotbar as one line of ten buttons, and a second row on screen is the next page's line. Buttons therefore **do not move** when you change Buttons Per Row. After changing the layout, drag your buttons into place once.

---

## Updating

1. Close the game.
2. Unpack the new zip and run its `Install.bat`.
3. Start the game, quit, and start it again. The first start copies the new skin; the second one uses it.

Your settings are kept. They are stored separately from the files that are replaced. Backgrounds you made yourself are overwritten if they use MerkUI's file names, so keep copies.

---

## Uninstall

1. Close the game.
2. Run **`Uninstall.bat`** and type YES when it asks.

It removes MerkUI's `version.dll`, pictures, videos and skin folder, and puts back `version.dll.bak` if there is one. A `version.dll` that is not MerkUI's is left alone.

### Uninstall by hand

1. Close the game.
2. Delete `version.dll`, the `MerkUI_Skin` folder and every file starting with `MerkUI_` from the game folder. If there is a `version.dll.bak`, rename it back to `version.dll`.
3. Delete the `MerkUI` folder in `%LOCALAPPDATA%\Funcom\Anarchy Online\<code>\client\Gui`, in every code folder that has one.

Two files in the game folder are left for you to delete if you want:

- `MerkUITimerBars.ini`: your MerkUI settings.
- `MerkUI.log`: a log file.

---

## Troubleshooting

**There is no MerkUI entry in F10.**
`version.dll` is not being loaded, or it is in the wrong folder. It must sit next to `AnarchyOnline.exe`. Also check that your antivirus has not removed it (see below).

**The MerkUI entry is there, but the bars are missing.**
Your client version does not match the one MerkUI was built for. MerkUI checks the game's files before it changes anything and stays off if they differ.

**The login screen looks like AO's own.**
The `MerkUI_Skin` folder or the pictures are not next to `AnarchyOnline.exe`, or you have not chosen the MerkUI skin and restarted yet. Run `Install.bat` again and follow steps 4 to 7.

**The backgrounds do not move.**
The `.mp4` files are missing from the game folder, or Windows cannot play them (see Requirements). The log file says which: look for lines with `video`.

**My antivirus flags `version.dll`.**
MerkUI works by placing a `version.dll` in the game folder, which the game loads at start. That is a common way to mod a game, and also a pattern some antivirus programs warn about on principle. If you do not trust the file, do not install it. The full source code is published with each release (the source zip) for anyone who wants to read or rebuild it.

**The game crashes at start or at login after installing.**
Remove `version.dll` (see Uninstall) to get back to a working game, then report it with the log file.

**A slider seems stuck on certain values.**
Buttons Per Row and Button Size only accept certain values on purpose. See the Action Bars section.

**Some F10 buttons cannot be clicked.**
An unlocked MerkUI element may be lying on top of the options window. Move the options window, or lock the element.

### Reporting a problem

Please include:

- The MerkUI version (top of this file).
- What you did, and what happened.
- A screenshot if it is a visual problem.
- The file `MerkUI.log` from your game folder.

---


## Credits

Made by Merk.
- Daddy & Dypfryst for helping out testing.

The Renderer pages use the settings interface of [ao-vk](https://github.com/wannabuh/ao-vk) and are built the way [AOReloaded](https://github.com/wannabuh/AOReloaded)'s Renderer tab builds them. Both are MIT licensed; see the `licenses` folder.
