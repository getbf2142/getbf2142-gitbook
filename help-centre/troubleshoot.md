---
description: Got issues ? Find answers here !
icon: gear
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: false
  metadata:
    visible: true
---

# Troubleshoot

This is your go-to spot for solutions to some of the most common problems you might run into. If you're facing something that isn't covered here, definitely head over to the [Reclamation FAQ page](https://battlefield2142.co/faq/) — you'll find even more helpful info there!

### (G) Graphics

<details>

<summary>G01: Running the game in windowed mode causes scaling issues or distortion</summary>

Related Article(s): [Apply OpenSpy patches](../getting-started/apply-openspy-patches.md)

Windows scaling settings can interfere with a game’s display due to non-functioning high DPI awareness.

**Symptom(s):**

* UI appears distorted, pixelated, or unreadable on modern high-resolution screens.
* UI looks oversized or bitmap-stretched.

**Solution(s)**

* Enable High DPI Aware ([A01](troubleshoot.md#a01-enable-high-dpi-aware)).
* Run the game once in fullscreen mode, then switch to windowed mode.

</details>

<details>

<summary>G02: Having weird graphics glitches like blackouts, see-through, inverted colors, or ghost objects</summary>

This usually happens because the old DirectX9 engine is trying to use anti-aliasing with a modern graphics card.

**Symptom(s):**

* See-through or x-ray visuals
* Ghost objects (e.g., invisible terrain or soldier units)
* Inverted colors
* Object blackouts

**Solution(s):**

* Turn off Anti-Aliasing ([A02](troubleshoot.md#a02-turn-off-anti-aliasing)).
* Delete Profile and Cache ([A03](troubleshoot.md#a03-delete-profile)).
* Use a lower resolution and refresh rate.
* Disable High DPI Aware ([A01](troubleshoot.md#a01-enable-high-dpi-aware)).

- Reinstall the game.

</details>

<details>

<summary>G03: Experiencing mouse skipping, stuttering, or a jumping aimpoint</summary>

Related Article(s): [Stuttering, mouse skipping & FPS cap](https://www.lost-soldiers.org/v2.php?site=forum_topic\&topic=81\&type=ASC\&page=2#bigNO)

This issue is likely tied to the game’s animation system or engine, not your mouse polling rate.

**Symptom(s):**

* Stutters when moving the mouse quickly or over a long horizontal distance
* Skipped frames during sideways movement

**Solution(s):**

* There’s currently no known fix.

</details>

### (C) Crashes

<details>

<summary>C01: Game crashes to desktop after a flashing black screen</summary>

BF2142 can run into issues on modern PCs, most commonly due to incompatible video modes or incorrect video settings.

**Symptom(s):**

* Crash after a brief black screen
* Crash before the intro or main menu appears

**Solution(s):**

* Delete Profile and Cache ([A03](troubleshoot.md#a03-delete-profile)).
* Enable High DPI Aware ([A01](troubleshoot.md#a01-enable-high-dpi-aware)).
* Run the game in windowed mode.
* Use a resolution and refresh rate your monitor supports.&#x20;
* Use the <mark style="color:blue;">GameUX Fix</mark> tool in BF2142 Hub (Windows 7 only).
* Run the [Vidcon Fix](https://battlefield2142.co/bf2142_vidcon_fix.exe) ([#blackscreen](https://battlefield2142.co/faq/#blackscreen)).
* Reinstall the game.

</details>

<details>

<summary>C02: Game crashes when adjusting audio settings</summary>

Crashes often occur when you have over 9 input audio devices. Tools like VirtualCable or Voicemeeter that add multiple inputs are common culprits.

**Symptom(s):**

* Game crashes when adjusting in-game audio settings
* Game crashes when joining a match, sometimes with a brief audio beep beforehand

**Solution(s):**

* In <mark style="color:blue;">Control Panel</mark> > <mark style="color:blue;">Sound</mark> > <mark style="color:blue;">Recording</mark>, disable unused input devices. Keep active inputs under 10.
* In <mark style="color:blue;">Device Manager</mark>, uninstall unused input audio interfaces; keep active under 10.
* Uninstall apps that add many inputs (e.g., VirtualCable, Voicemeeter).
* Set <mark style="color:blue;">Audio Renderer</mark> to <mark style="color:blue;">Software</mark> and <mark style="color:blue;">Enable EAX</mark> to <mark style="color:blue;">No</mark> in-game.

Special thanks to Edouard @ [Reclamation Discord](https://discord.com/invite/MEwBW9U) for discovering the solution to this issue.

</details>

<details>

<summary>C03: Runtime error or missing DLL error when starting the game</summary>

This usually occurs when the Microsoft Visual C++ Runtime Library is missing.

**Symptom(s):**

* "The code execution cannot proceed because MSVCP71.dll was not found. Reinstalling the program may fix this problem."
* "The code execution cannot proceed because dice\_py.dll was not found. Reinstalling the program may fix this problem."
* "Runtime Error! This application has requested the Runtime to terminate it in an unusual way."

**Solution(s):**

* Install [Microsoft Visual C++ Runtime Library](https://aka.ms/vs/17/release/vc_redist.x86.exe).
* Update Windows.

</details>

<details>

<summary>C04: "memory.dll sanity check" error when joining a game or loading a map</summary>

Related Article(s): [memory.dll sanity check.... error](https://forum.realitymod.com/viewtopic.php?t=80268)

**Symptom(s):**

* "memory.dll: sanity check: block size xxxxxxx (xxxxxx mb) doesn't seem sane"
* "memory.dll: all alloc attempts failed for size xxxxxxxxx"

**Solution(s):**

* Turn off Anti-Aliasing ([A02](troubleshoot.md#a02-turn-off-anti-aliasing)).
* Lower in-game graphics settings (set everything to Medium or Low).

- Set pagefile to be managed by the Operating System in `SystemPropertiesPerformance.exe`.
- Set the game’s CPU affinity to a single core in <mark style="color:blue;">Task Manager</mark>.
- Check for and install any BIOS updates for your motherboard.
- Reinstall the game.

</details>

<details>

<summary>C05: Game crashes when clicking "Host" or "Singleplayer" in BF2142Unlocker</summary>

Related Article(s): [BF2142Unlocker](../advanced/addons-tweaks/bf2142unlocker.md)

`127.0.0.1` is usually the culprit.

**Symptom(s):**

* Check [here](../advanced/addons-tweaks/bf2142unlocker.md) for details.

**Solution(s):**

* Check [here](../advanced/addons-tweaks/bf2142unlocker.md) for details.

</details>

### (S) Servers

<details>

<summary>S01: Account creation error when creating an account</summary>

Related Article(s): [Create an account](../getting-started/create-account.md)

**Symptom(s):**

* "A system error occured. Try again later. If problem persists, contact customer support."

**Solution(s):**

* Try a different account name or email; they may already be in use.
* Ensure your country code, postal code, and birthdate format are valid, and avoid non-standard characters in any fields.

</details>

<details>

<summary>S02: Could not connect to EA Online or EA Master Server when logging in or creating an account</summary>

Related Article(s): [Apply OpenSpy patches](../getting-started/apply-openspy-patches.md)

There are many potential causes for this issue — your internet connection, BF2142 Hub, OpenSpy patches, firewall/antivirus, DNS, ISP, or even the master server.

{% hint style="info" %}
If OpenSpy is down, switch to NovGames via BF2142 Hub, or play Singleplayer with all unlocks using [BF2142Unlocker](../advanced/addons-tweaks/bf2142unlocker.md).
{% endhint %}

**Symptom(s):**

* Stuck at "Contacting EA Master Server"

- "Could not connect to EA Online. Retry, or click OK to go into Offline mode. If you proceed, try logging in again later."
- "EA Master Server is down. Please use BF2142Unlocker"
- "You are not connected to the Internet. Click OK to select a soldier to play offline, or try to reconnect."

**Soution(s):**

* Ensure your internet connection is stable.

- Reinstall OpenSpy patches and confirm four green ticks.
- Install Openspy patches manually ([A05](troubleshoot.md#a05-install-openspy-patches-manually)).
- Fully close and restart BF2142 Hub.
- Use the <mark style="color:blue;">Reset Hub</mark> tool in BF2142 Hub, or reinstall the Hub.
- Allow BF2142 through <mark style="color:blue;">Windows Firewall</mark> (both private and public).
- Ensure your antivirus or firewall isn’t blocking BF2142 or the Hub.
- Ask in the [Reclamation Discord](https://discord.com/invite/MEwBW9U) if others have the same issue (the OpenSpy master server may be down or in maintenance).
- In <mark style="color:blue;">Command Prompt</mark>, run: `ipconfig /flushdns`
- Switch DNS to `1.1.1.1` or `1.0.0.1` (Cloudflare).
- Use a VPN (e.g., ExpressVPN or ProtonVPN) to bypass ISP restrictions.

</details>

<details>

<summary>S03: No servers showing in the server browser, even with the patches installed</summary>

Related Article(s): [Play Multiplayer](../getting-started/play-multiplayer.md)

**Symptom(s):**

* No servers visible in the server browser

**Solution(s):**

* Uncheck all filter options (see details [here](../getting-started/play-multiplayer.md#joining-a-public-wan-server)).

- Use the <mark style="color:blue;">Missing Servers</mark> tool in BF2142 Hub.

</details>

<details>

<summary>S04: "This map contains customised content" error when joining a Reclamation server</summary>

Related Article(s): [Install the map pack](../getting-started/install-map-pack.md)

You might have an outdated or missing map.

**Symptom(s):**

* "This map contains customized content. The map creator might have more information about the map on the community site."

**Solution(s):**

* Download the required map pack or the specific map the server is running.
* If you already have it, note the problematic map, uninstall it, then reinstall it using BF2142 Hub’s individual map option.
* If you’re kicked with this message during a map change, that’s normal — just rejoin the server.

</details>

<details>

<summary>S05: "This server only allows players with unmodified content to join" error when joining a server</summary>

Related Article(s): [Play Multiplayer](../getting-started/play-multiplayer.md)

You may have modified files in your current mod or tried to join with the wrong mod selected.

**Symptom(s):**

* "This server only allows players with unmodified content to join. Revert your version of Battlefield 2142 to the current version to join."

**Solution(s):**

* For Reclamation or any vanilla servers, use a clean vanilla BF2142 setup — no addons or file tweaks in `\mods\bf2142`.

- For modded servers, install the exact same mod and files the server is running.

</details>

<details>

<summary>S06: Invalid CD-Key error when joining a server</summary>

Related Article(s): [Install BF2142](../getting-started/download-and-install-bf2142.md)

This issue occurs when the game’s CD key isn’t found in your registry, likely due to skipped installation steps.

**Symptom(s):**

* "Invalid CD-Key"

**Solution(s):**

* Use the <mark style="color:blue;">CD-Key Fix</mark> tool in BF2142 Hub or Remaster Launcher.
* For NovGames servers, run the ACTIVATOR and click <mark style="color:blue;">Activate</mark>.
* Go to `C:\Program Files (x86)\Electronic Arts\Battlefield 2142\Support`, launch `Battlefield 2142_code.exe`, and enter a [CD key](#user-content-fn-1)[^1].

- Install the missing registry files ([A04](troubleshoot.md#a04-install-the-registry-files)).
- Reinstall the game.

</details>

### (H) BF2142 Hub

<details>

<summary>H01: Application exception or mdIBF error when starting BF2142 Hub</summary>

This usually happens when your ISP blocks certain IPs (preventing BF2142 Hub from reaching external services) or when the game’s info is missing from your registry due to skipped install steps.

**Symptom(s):**

* "mdIBF.ReadConfig: Unexpected character encountered while parsing value: <. Path ", line 0, position 0." (VPN)
* "mdIBF.Banner: Object reference not set to an instance of an object." (VPN)
* "mdIBF.ReadServer: Object reference not set to an instance of an object." (VPN)
* "mdIBF.CDKeyLaunch: Object reference not set to an instance of an object." (Registry)
* "the type initialisation function for b2142\_hub MDIBFclient has causes an exeption." (VPN)

**Solution(s):**

* Use a VPN (e.g., ExpressVPN or ProtonVPN) to bypass ISP restrictions.

- Install the missing registry files ([A04](troubleshoot.md#a04-install-the-registry-files)).
- Reinstall the game.

</details>

<details>

<summary>H02: BF2142 Hub scaling looks messed up or distorted</summary>

Windows scaling settings can interfere with an application’s display due to non-functioning high DPI awareness.

**Symptom(s):**

* UI appears distorted, pixelated, or unreadable on modern high-resolution screens.
* UI looks oversized or bitmap-stretched.

**Solution(s):**

* Enable High DPI Aware ([A01](troubleshoot.md#a01-enable-high-dpi-aware)).

</details>

<details>

<summary>H03: Unable to install OpenSpy patches – no green ticks after clicking install</summary>

**Symptom(s):**

* No response after clicking Install
* Not all components show green ticks

**Solution(s):**

* Run BF2142 Hub as an administrator.
* Install OpenSpy patches manually ([A05](troubleshoot.md#a05-install-openspy-patches-manually)).

</details>

### (A) Common Actions

<details>

<summary>A01: Enable High DPI Aware</summary>

If you’re fixing scaling for the game, do this for `BF2142.exe`. For BF2142 Hub, do it for `BF2142 Hub.exe`.

* Game: `C:\Program Files (x86)\Electronic Arts\Battlefield 2142`
* Hub: `C:\Program Files (x86)\BF2142 Hub 2`

Steps:

1. Right-click the `.exe` and select <mark style="color:blue;">Properties</mark>.
2. Go to the <mark style="color:blue;">Compatibility</mark> tab > <mark style="color:blue;">Change high DPI settings</mark>.
3. Under <mark style="color:blue;">High DPI scaling override</mark>, check <mark style="color:blue;">Override high DPI scaling behavior</mark>.
4. Set <mark style="color:blue;">Scaling performed by:</mark> to <mark style="color:blue;">Application</mark>.
5. Click <mark style="color:blue;">Apply</mark>, then <mark style="color:blue;">OK</mark>.

Notes:

* You’ll need to repeat these steps each time you click <mark style="color:blue;">Install</mark> in BF2142 Hub. **\[**[**?**](#user-content-fn-2)[^2]**]**
* To disable High DPI Aware, just uncheck <mark style="color:blue;">Override high DPI scaling behavior</mark> in step 3.

</details>

<details>

<summary>A02: Turn off Anti-Aliasing</summary>

There are two ways to do this:

* Turn off <mark style="color:blue;">Anti-Aliasing</mark> in-game.
* Use the <mark style="color:blue;">Anti-Aliasing Off</mark> tool in BF2142 Hub.

Notes:

* If you’re not having issues, you can set <mark style="color:blue;">Anti-Aliasing</mark> to <mark style="color:blue;">4x</mark>.
* If you must turn it off but still want smoothing, force Anti-Aliasing via your NVIDIA or AMD control panel instead.

</details>

<details>

<summary>A03: Delete Profile and Cache</summary>

This resets your profiles — including any faulty video or audio settings — and clears the shader cache.

There are three ways to do this:

* Delete the `Battlefield 2142` folder in `C:\Users\...\Documents`.

- Use the <mark style="color:blue;">Clear Cache</mark> and <mark style="color:blue;">Delete Profile</mark> tool in BF2142 Hub
- Use the <mark style="color:blue;">Clear Cache</mark> and <mark style="color:blue;">Reset Game-Settings</mark> tool in the Remaster Launcher.

</details>

<details>

<summary>A04: Install the missing registry files</summary>

{% hint style="danger" %}
If your game was installed via EA App or Origin, reinstall the game instead and do not use this method.
{% endhint %}

1. Download the registry file [here](https://www.regfiles.net/registry/battlefield-2142-registry).
2. Adjust the <mark style="color:blue;">PATH</mark> and <mark style="color:blue;">CDKEY</mark> before downloading.
3. Open the file in a text editor and set:
   * <mark style="color:blue;">Version</mark> to `1.51`
   * <mark style="color:blue;">BuildNr</mark> to `1.10.77.0`

4) Save, then double-click the file to install.

</details>

<details>

<summary>A05: Install OpenSpy patches manually</summary>

1. Download the patches.
   1. [MediaFire](https://www.mediafire.com/file/98a6muljivaoidl/BF2142_OpenSpy_Patches.zip/file)
   2. [Google Drive](https://drive.google.com/file/d/1SX1yyOhEGlUXKR3FBgbKRRCpvVsQ9iDJ/view)
   3. [Reclamation Discord](https://discord.com/invite/MEwBW9U)
2. Place `bf2142.exe`, `RendDX9_ori.dll`, and `RendDX9.dll` in your game directory: `C:\Program Files (x86)\Electronic Arts\Battlefield 2142`
3. Replace or overwrite the files when prompted.
4. Restart BF2142 Hub — you should now see four green ticks.

</details>

[^1]: e.g., `E6HH-DWUG-U8X1-R8F0-1911` for Standard Edition

[^2]: Whenever you install a new patch from BF2142 Hub, it updates your `BF2142.exe`, which means your compatibility settings will be reset.
