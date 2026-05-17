# Nothing0-Slime-RNG-Auto-Gun-Multi-Instance-Anti-AFK

<div align="center">

# 🔫 Nothing0 Auto Gun

**Automated gun activation script for Roblox**

*External AutoHotkey tool that simulates key inputs every 60 seconds*

![AutoHotkey](https://img.shields.io/badge/AutoHotkey-v1.1-green?style=for-the-badge&logo=autohotkey)
![Platform](https://img.shields.io/badge/Platform-Windows%2010%2F11-blue?style=for-the-badge&logo=windows)
![Status](https://img.shields.io/badge/Multi--Instance-BETA-orange?style=for-the-badge)
![VirusTotal](https://img.shields.io/badge/VirusTotal-0%2F64%20Clean-brightgreen?style=for-the-badge&logo=virustotal)

**[🛡️ VirusTotal Scan — 0/64 Clean](https://www.virustotal.com/gui/file/789feb6d1a1922d03fba2891086a5bddd33c058e83a512ec87c83a54e6b900e6?nocache=1)**

</div>

---

## ⚠️ Disclaimer

> **Use at your own risk.**
>
> This script automates **external** keyboard and mouse inputs only. It does **not** inject, modify, or exploit Roblox in any way.
> However, using automation tools may violate **Roblox's Terms of Service**.
>
> **I (Nothing0) take absolutely no responsibility if your account gets banned or sanctioned.**
> By downloading and using this script, you acknowledge and accept all risks.

---

## 📋 Requirements

| Tool | Version | Link |
|------|---------|------|
| **AutoHotkey** | v1.1 only — NOT v2 | [Download](https://www.autohotkey.com/download/ahk-install.exe) |
| **Windows** | 10 or 11 | — |
| **Roblox** | Any version | Must run in **windowed mode** |

> 💡 To switch Roblox to windowed mode, press `Alt + Enter` inside the game.

---

## 📁 Files

| File | Description |
|------|-------------|
| `Nothing0_Auto_Gun.ahk` | ✅ **Main script** — run this |
| `detect_process.ahk` | 🔍 Test — Lists all running processes |
| `detect_roblox.ahk` | 🔍 Test — Checks if Roblox is detected |
| `detect_resume_button.ahk` | 🔍 Test — Checks Resume button color detection |
| `settings.ini` | ⚙️ Auto-created on first launch |

---

## 🚀 How To Use

**Step 1 — Install AutoHotkey v1.1**

Download and install from [autohotkey.com](https://www.autohotkey.com/download/ahk-install.exe)

> ⚠️ Make sure to install **v1.1**, not v2. The script will **not** work on v2.

---

**Step 2 — Download the script**

Click the green **`Code`** button → **`Download ZIP`** → Extract anywhere on your PC

---

**Step 3 — Launch Roblox in windowed mode**

Press `Alt + Enter` inside Roblox to switch to windowed mode

---

**Step 4 — Run the script**

Double-click `Nothing0_Auto_Gun.ahk` — the GUI will appear on screen

---

**Step 5 — Set your hotkeys**

- **Toggle Key** → turns the script ON / OFF *(default: `F1`)*
- **Detect Key** → scans for open Roblox instances *(default: `F2`)*

Change any key using the selector in the GUI, then click **Save**

---

**Step 6 — Start**

Press your **Toggle Key** → status turns 🟢 **ON**

The script will automatically activate your gun every **60 seconds**

---

## 🧪 Test Scripts

> Run these **before** the main script to verify everything works on your setup.

<details>
<summary><b>Click to expand</b></summary>

<br>

<h2>▶️ How to Use</h2>

<p>Double-click the script to run it.</p>

<p>
A window will appear showing all running programs with their
<code>.exe</code> names.
</p>

<p>Find the line containing <b>Roblox</b>.</p>

<hr>

<h2>💡 Important — Roblox Process Name</h2>

<p>
Depending on your Roblox version or installation, the process name may differ
from the default one used in the script.
</p>

<p>By default, the script uses:</p>

<pre><code>RobloxPlayerBeta.exe</code></pre>

<p>
However, during the test, you may see another process name such as:
</p>

<pre><code>RobloxPlayerInstaller.exe</code></pre>

<p>or another variation ending with <code>.exe</code>.</p>

<p>
If that happens, replace:
</p>

<pre><code>RobloxPlayerBeta.exe</code></pre>

<p>
with the exact process name displayed on your system.
</p>

<hr>

<h2>📌 Example</h2>

<table>
<tr>
<th>Detected Process</th>
<th>Action</th>
</tr>

<tr>
<td><code>RobloxPlayerBeta.exe</code></td>
<td>✅ No changes needed</td>
</tr>

<tr>
<td><code>RobloxPlayerInstaller.exe</code></td>
<td>🔁 Replace the name in the script</td>
</tr>

<tr>
<td>Any other Roblox <code>.exe</code></td>
<td>🔁 Use that exact name</td>
</tr>
</table>

<hr>

<h2>⚠️ Warning</h2>

<p>
The process name must match <b>exactly</b>.
</p>

<p>
Otherwise, the script will not detect Roblox correctly.
</p>

</details>

<details>
<summary><b>Test 2 — detect_roblox.ahk</b></summary>

Double-click to run it.
It will immediately tell you if Roblox is detected.
Then press **F2** to get the number of instances and their window IDs.

</details>

<details>
<summary><b>Test 3 — detect_resume_button.ahk</b></summary>

1. Open Roblox and open the **Escape menu** (Resume / Leave / Respawn)
2. Press **F3**
3. ✅ **DETECTED** → you are good to go
4. ❌ **NOT detected** → follow the color fix guide below

</details>

---

## 🎨 Resume Button Color Fix

The script detects the **blue Resume button** in the Roblox Escape menu.
The color may vary depending on your screen, resolution, or display settings.

**How to find your color:**

1. Right-click the AutoHotkey tray icon → **Open Window Spy**
2. Open Roblox → open the Escape menu
3. Hover your mouse over the **Resume button**
4. Copy the color value shown in Window Spy *(example: `4C6EF5`)*

**Where to change it:**

Find this line in `Nothing0_Auto_Gun.ahk` *(appears twice)*:

```ahk
PixelSearch, Px, Py, 830, 640, 1050, 710, 0x4C6EF5, 30, Fast RGB
```

Replace `0x4C6EF5` with your value *(keep the `0x` prefix)*.

| Resolution | Color to try |
|------------|-------------|
| 1920x1080 | `0x4C6EF5` |
| 2560x1440 | `0x4C6EF5` |
| Other | Use Window Spy |

---

## 🔄 Multi-Instance — BETA

> ⚠️ **Multi-instance support is currently in BETA and may be unstable.**

The script automatically detects and cycles through **all open Roblox windows**.
Press your **Detect Key** at any time to see how many instances are running.

**Known limitations:**

- Roblox must be in **windowed mode** for window switching to work
- Fast switching between many instances may cause timing issues
- Color detection may fail if instances have different screen scaling

---

## ⚙️ Settings

Settings are saved automatically to `settings.ini`. No need to edit it manually.

| Key | Default | Description |
|-----|---------|-------------|
| `ToggleKey` | `F1` | Turn script ON / OFF |
| `DetectKey` | `F2` | Scan for Roblox instances |

---

## ❓ FAQ

<details>
<summary><b>The script launches but nothing happens?</b></summary>

Make sure Roblox is open in windowed mode, then press your Toggle Key.

</details>

<details>
<summary><b>The hotkeys make a Windows error sound?</b></summary>

Another program may already be using that key. Change your hotkey in the GUI and click Save.

</details>

<details>
<summary><b>Roblox is not detected?</b></summary>

Run `detect_roblox.ahk` first. If it says NOT found, try right-clicking the `.ahk` file and selecting **Run as administrator**.

</details>

<details>
<summary><b>The Escape menu stays open after the action?</b></summary>

Run `detect_resume_button.ahk` with the Escape menu open, then press F3. If NOT detected, follow the color fix guide above.

</details>

<details>
<summary><b>Does this work with multiple Roblox accounts?</b></summary>

Yes — open multiple Roblox windows and the script will cycle through each one automatically. *(BETA)*

</details>

---

## 📜 License

Free to use and modify for personal use.
Do not redistribute or resell without credit.

---

<div align="center">

*Made by Nothing0*

</div>
