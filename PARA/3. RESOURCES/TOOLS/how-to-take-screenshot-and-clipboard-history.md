---
id: how-to-take-screenshot-and-clipboard-history
aliases: []
tags: []
---

I have created a robust, all-in-one script based on your requirements. It brings together the functionality from the inspiration scripts and
enhances it with a seamless menu experience using Rofi.

I've saved the tool as an executable script at clipboard-tool.sh.

### Features

1. Copy/Paste Texts: Uses an add command to read the current clipboard and save text persistently.
2. Partial Screenshotting: Uses a screenshot command. It uses maim or import to capture a selected area.
3. Images in the Clipboard Menu: The menu command opens a visual Rofi menu. The script utilizes Rofi's icon feature (\0icon\x1f<path>) to
   dynamically display actual image thumbnails right next to the history items!
4. Auto-save: Every screenshot is automatically saved directly to ~/Screenshots with a timestamp.

### Prerequisites

Make sure you have these packages installed on your system:

• rofi (Required for the visual menu that supports images)
• xclip (Required for clipboard interactions)
• maim or imagemagick (Required for the screenshot functionality)
• libnotify (Optional, provides the notify-send command for desktop notifications)

### How to use it

he script has four primary commands. You should map these commands to your preferred keyboard shortcuts in your window manager or desktop
environment.

1. Screenshot: $mod+Shift+s (Replaced the previous commented-out
   rofi screenshot keybind).
2. Clipboard Menu: $mod+Shift+semicolon (Replaced the old copyq show
   keybind).
3. Save to History: Control+c (Runs the script to add your clipboard to history).
4. Clear History:
   /home/manish/clipboard-tool.sh clear

### ⚠️ CRITICAL WARNING ABOUT Ctrl+C ⚠️

Binding Control+c directly in your i3 config means the window
manager will intercept this shortcut globally.
Because of this, Ctrl+C will no longer reach your applications. This
means:

• You won't be able to use Ctrl+C to copy text in your browser or
text editors.
• You won't be able to use Ctrl+C to kill running commands in your
terminal (SIGINT).

If you find this breaks your workflow, I highly recommend modifying
the shortcut in ~/.config/i3/config (around line 227) to something
like $mod+c or $mod+Shift+c. If you'd like me to change it for you
right now, just let me know!
