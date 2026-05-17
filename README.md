# Nothing0-Slime-RNG-Auto-Gun-Multi-Instance-Anti-AFK

🔫 Nothing0 Auto Gun

Automated gun activation script for Roblox — External AutoHotkey tool that simulates key inputs every 60 seconds.


⚠️ Disclaimer

Use at your own risk.
This script automates external keyboard and mouse inputs. It does not inject or modify Roblox in any way.
However, using automation tools may violate Roblox's Terms of Service.
I (Nothing0) take absolutely no responsibility if your account gets banned or sanctioned.
By using this script, you acknowledge and accept all risks.


📋 Requirements
ToolDetailsAutoHotkey v1.1Download here — Must be version 1.1, NOT v2Windows 10/11Required for pixel detection and window managementRobloxRunning in windowed mode (not fullscreen)

⚠️ Important: Make sure you download AutoHotkey v1.1 and not v2. The script will not work on v2.


📁 Files
FilePurposeNothing0_Auto_Gun.ahk✅ Main script — run thisdetect_process.ahk🔍 Test — Lists all running processesdetect_roblox.ahk🔍 Test — Checks if Roblox is detecteddetect_resume_button.ahk🔍 Test — Checks Resume button color detectionsettings.ini⚙️ Auto-created on first launch — stores your hotkeys

🚀 How To Use
Step 1 — Install AutoHotkey v1.1
Download and install AutoHotkey v1.1 from autohotkey.com
Step 2 — Download the script
Click the green Code button → Download ZIP → Extract the folder anywhere on your PC
Step 3 — Launch Roblox
Open Roblox and make sure it runs in windowed mode

Press Alt + Enter in Roblox to switch between fullscreen and windowed

Step 4 — Run the script
Double-click Nothing0_Auto_Gun.ahk
The GUI will appear on your screen
Step 5 — Configure your hotkeys

Toggle Key — The key to turn the script ON/OFF (default: F1)
Detect Key — The key to manually scan for Roblox instances (default: F2)
Change any key using the selector, then click Save

Step 6 — Start the script
Press your Toggle Key (default F1) → Status turns GREEN (ON)
The script will automatically activate your gun every 60 seconds

🧪 How To Use The Test Scripts
Run these before using the main script to make sure everything works on your setup.
Test 1 — detect_process.ahk
Double-click to run it.
A window will appear listing all running programs.
Look for the line containing Roblox and note the exact .exe name.
Test 2 — detect_roblox.ahk
Double-click to run it.
It will immediately tell you if Roblox is detected.
Then press F2 to get the exact number of instances and their window IDs.
Test 3 — detect_resume_button.ahk

Open Roblox
Open the Escape menu inside the game (the menu with Resume / Leave / Respawn)
Press F3
If it says DETECTED → you are good to go ✅
If it says NOT detected → see the section below to fix the color


🎨 Resume Button Color — Fix For Your Screen
The script detects the blue Resume button in the Roblox Escape menu.
Depending on your screen resolution, monitor, or color settings, the color value may be slightly different.
How to find the correct color:

Install AutoHotkey v1.1 (includes Window Spy tool)
Right-click the AutoHotkey icon in your taskbar → Open Window Spy
Open Roblox → Open the Escape menu
Hover your mouse over the Resume button
Note the color value shown in Window Spy (example: 4C6EF5)

Where to change it in the main script:
Find this line in Nothing0_Auto_Gun.ahk (appears twice):
PixelSearch, Px, Py, 830, 640, 1050, 710, 0x4C6EF5, 30, Fast RGB
Replace 0x4C6EF5 with your color value (keep the 0x prefix).
Common color values by resolution:
ResolutionColor to try1920x10800x4C6EF52560x14400x4C6EF5OtherUse Window Spy to find it

🔄 Multi-Instance Support — BETA

⚠️ Multi-instance support is currently in BETA.

The script can detect and cycle through multiple Roblox windows automatically.
Use the Detect Key (default F2) at any time to scan how many instances are currently open.
Known limitations in beta:

Roblox must be in windowed mode for window switching to work
Very fast PC switching between instances may cause timing issues
The Resume button color detection may fail on some instances if screen scaling differs


⚙️ Settings
All settings are automatically saved to settings.ini in the same folder as the script.
You do not need to edit this file manually.
SettingDefaultDescriptionToggleKeyF1Turn script ON/OFFDetectKeyF2Manually scan for Roblox instances

❓ FAQ
The script launches but nothing happens?
→ Make sure Roblox is open and running in windowed mode, then press your Toggle Key.
The hotkeys make a Windows error sound?
→ Another program may be using the same key. Change your hotkey in the GUI and click Save.
Roblox is not detected?
→ Run detect_roblox.ahk first. If it says NOT found, try running the main script as administrator (right-click → Run as administrator).
The Escape menu stays open after the action?
→ Run detect_resume_button.ahk with the menu open and press F3. If NOT detected, follow the color fix guide above.
Does this work with multiple Roblox accounts?
→ Yes, open multiple Roblox windows and the script will cycle through each one. (BETA)

📜 License
Free to use and modify for personal use.
Do not redistribute or resell without credit.

Made by Nothing0
