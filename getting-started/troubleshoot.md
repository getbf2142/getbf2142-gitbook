---
description: Got issues ? Find answers here !
---

# ⍟ Troubleshoot

This is your go-to spot for solutions to some of the most common problems you might run into. If you're facing something that isn't covered here, definitely head over to the [Reclamation FAQ page](https://battlefield2142.co/faq/) — you'll find even more helpful info there!

### (G) Graphics

<details>

<summary>G01: Running the game in windowed mode causes scaling issues or distortion</summary>

Related Article(s): [Install OpenSpy Patches](apply-openspy-patches.md)

Sometimes, Windows scaling settings can interfere with a game’s display, causing weird scaling or visual glitches. You can fix this by running the game in compatibility mode:

1. Go to the folder where your `BF2142.exe` is located — by default, that’s usually `C:\Program Files (x86)\Electronic Arts\Battlefield 2142`.
2. Right-click `BF2142.exe` and select <mark style="color:blue;">Properties</mark>.
3. In the <mark style="color:blue;">Compatibility</mark> tab, click <mark style="color:blue;">Change high DPI settings</mark>.
4. Under <mark style="color:blue;">High DPI scaling override</mark>, check <mark style="color:blue;">Override high DPI scaling behavior</mark>.
5. Set <mark style="color:blue;">Scaling performed by:</mark> to <mark style="color:blue;">Application</mark>.
6. Click <mark style="color:blue;">Apply</mark> and <mark style="color:blue;">OK</mark>.

Just a heads up: you’ll need to repeat these steps every time you click the install button in BF2142 Hub. **\[**[**?**](#user-content-fn-1)[^1]**]**

</details>

<details>

<summary>G02: Having weird graphics glitches like blackouts or ghost objects</summary>

This usually happens because the old DirectX9 engine is trying to use anti-aliasing with a modern graphics card.

**Symptom(s):**

* See-through buildings
* Ghost objects (e.g., invisible terrain or soldier units)
* Blackouts of certain objects

**Solution(s):**

* Turn off Anti-Aliasing in-game.
  * If you want anti-aliasing, use your NVIDIA or AMD control panel to set it up for your graphics card instead.
* Delete the `Battlefield 2142` folder in `C:\Users\...\Documents`. This will clean up your profiles — including any faulty video or audio settings — and clear your shader cache.
  * You can also use the <mark style="color:blue;">Clear Cache</mark> and <mark style="color:blue;">Delete Profile</mark> function in <mark style="color:blue;">BF2142 Hub</mark> or <mark style="color:blue;">Remaster Launcher</mark>, which has a similar effect.

</details>

<details>

<summary>G03: Experiencing mouse skipping, stuttering, or a jumping aimpoint</summary>

Related Article(s): [Stuttering, mouse skipping & FPS cap](https://www.lost-soldiers.org/v2.php?site=forum_topic\&topic=81\&type=ASC\&page=2#bigNO)

This issue may be related to the game’s animation system or engine itself, and has nothing to do with the mouse polling rate.

**Symptom(s):**

* Stand still (don’t move forward or backward; moving sideways is fine—the issue will still appear).
* Move your mouse only horizontally; the problem doesn’t occur vertically.
* The stutter happens when you move the mouse fast or over a long distance. Small aim adjustments are usually fine, but consistent sideways movement, even at slow speeds, can cause skipped frames.

**Solution(s):**\
Unfortunately, there’s currently no known fix for this issue.

</details>

### (C) Crashes

<details>

<summary>C01: Game crashes to desktop after a flashing black screen</summary>

BF2142 can have issues on modern PCs, with the most common cause being incompatible video modes or incorrect video settings.

**Symptom(s):**

* The game crashes after a flashing black screen.
* The game crashes way before the game intro or game menu shows.

**Solution(s):**

* Delete the `Battlefield 2142` folder in `C:\Users\...\Documents`. This will clean up your profiles — including any faulty video or audio settings — and clear your shader cache.
  * You can also use the <mark style="color:blue;">Clear Cache</mark> and <mark style="color:blue;">Delete Profile</mark> function in <mark style="color:blue;">BF2142 Hub</mark> or <mark style="color:blue;">Remaster Launcher</mark>, which has a similar effect.
* Launch the game in windowed mode, and be sure to use a resolution and refresh rate that your monitor supports.&#x20;
  * For example, if your monitor doesn’t support 120Hz and you select it, the game may crash. You can easily adjust these settings using <mark style="color:blue;">BF2142 Hub</mark> or <mark style="color:blue;">Remaster Launcher</mark>.
  * To start fresh, navigate to `C:\Users\...\Documents\Battlefield 2142\Profiles\Default\Video.con` and update the resolution and frequency to `800x600@60Hz` on the line that says: `VideoSettings.setResolution`. Once done, repeat this process in the `0001` profile folder as well.
* Run the [vidcon fix](https://battlefield2142.co/bf2142_vidcon_fix.exe) \[[Ref](https://battlefield2142.co/faq/#blackscreen)] and see if it helps.

</details>

<details>

<summary>C02: Game crashes when adjusting audio settings</summary>

Game crashes like this can be caused by virtual audio drivers. If you have VirtualCable or Voicemeeter installed, you’ll likely run into issues.

**Symptom(s):**

* The game crashes when you try to adjust audio settings in-game
* The game crashes when joining a match, sometimes with audio beeping just before the crash.

**Solution(s):**

* Open Device Manager and disable any virtual drivers.

- In the game’s audio settings, set audio rendering to software and turn off EAX.

</details>

<details>

<summary>C03: Runtime error or missing DLL error when starting the game</summary>

If you see a Runtime Error or messages about `dice_py.dll` or `MSVCR**.dll` missing when launching the game, it usually means you’re missing the Microsoft Visual C++ Runtime Library.

**Symptom(s):**

* "The code execution cannot proceed because MSVCP71.dll was not found. Reinstalling the program may fix this problem."
* "The code execution cannot proceed because dice\_py.dll was not found. Reinstalling the program may fix this problem."
* "Runtime Error! This application has requested the Runtime to terminate it in an unusual way."

**Solution(s):**

* Install the [Microsoft Visual C++ Runtime Library](https://aka.ms/vs/17/release/vc_redist.x86.exe).
* Make sure your Windows is up to date.

</details>

<details>

<summary>C04: "memory.dll sanity check" error when joining a game or loading a map</summary>

Related Article(s): [memory.dll sanity check.... error](https://forum.realitymod.com/viewtopic.php?t=80268)

**Symptoms:**

* "memory.dll: sanity check: block size xxxxxxx (xxxxxx mb) doesn't seem sane"
* "memory.dll: all alloc attempts failed for size xxxxxxxxx"

**Solutions:**

* Set pagefile to be managed by the OS.
* In Task Manager, set the game’s affinity to a single core.
* Try lowering your in-game graphics settings (medium or low for everything).
* Turn off Anti-Aliasing in-game.
* Check for BIOS updates for your motherboard.

</details>

<details>

<summary>C05: Game crashes when clicking "Host" or "Singleplayer" in BF2142Unlocker</summary>

Related Article(s): [BF2142Unlocker](../addons-tweaks/bf2142unlocker.md)

`127.0.0.1` is usually the culprit behind most issues after clicking <mark style="color:blue;">Host</mark> or <mark style="color:blue;">Singleplayer</mark>. For details on how to fix this, check [here](../addons-tweaks/bf2142unlocker.md).

</details>

### (S) Servers

<details>

<summary>S01: Account creation error when creating an account</summary>

Related Article(s): [Create an account](create-account.md)

**Symptom(s):**

* "A system error occured. Try again later. If problem persists, contact customer support."

**Solution(s):**

* Try using different entries for account name or email address, as they may already be associated with other accounts.
* Ensure you use a valid country code, postal code, correct birthdate format, and avoid entering non-standard characters in any fields.

</details>

<details>

<summary>S02: Could not connect to EA Online or EA Master Server when logging in or creating an account</summary>

Related Article(s): [Apply OpenSpy patches](apply-openspy-patches.md), [Install BF2142 Hub](download-and-install-bf2142-hub.md)

There are many potential causes for this issue, including your internet connection, BF2142 Hub, OpenSpy patches, firewall, antivirus, DNS, ISP, or even the master server itself.

{% hint style="info" %}
If OpenSpy is down, you can switch to NovGames via BF2142 Hub or play Singleplayer with all unlocks using [BF2142Unlocker](../addons-tweaks/bf2142unlocker.md).
{% endhint %}

**Symptom(s):**

* "You are not connected to the Internet. Click OK to select a soldier to play offline, or try to reconnect."
* "Could not connect to EA Online. Retry, or click OK to go into Offline mode. If you proceed, try logging in again later."
* "Could not connect to EA Online."
* "EA Master Server is down."
* "EA Master Server is down. Please use BF2142Unlocker."

**Soution(s):**

* Ensure you have a steady internet connection.
* Reinstall the OpenSpy patches and confirm there are four green ticks.
* Restart BF2142 Hub (close it completely, then reopen it).
* Reinstall BF2142 Hub if the issue persists.
* Always run BF2142 Hub as an administrator.

- Make sure BF2142 is allowed through both private and public networks in Windows Firewall.
- Check that no antivirus or firewall is blocking BF2142 from communicating externally.

* Ask in the Reclamation Discord to see if others are experiencing the same issue. If so, the OpenSpy master server (login service) might be down or undergoing maintenance.
* Use `ipconfig /flushdns` in Command Prompt to flush your DNS entries.
* Switch to DNS services like `1.1.1.1` or `1.0.0.1` (Cloudflare).
* Use a VPN service, such as ExpressVPN or ProtonVPN, to bypass ISP restrictions.

</details>

<details>

<summary>S03: No servers showing in the server browser, even with the patches installed</summary>

Related Article(s): [Play multiplayer](play-multiplayer.md)

To view servers in the global server browser, ensure all server filter options are unchecked. For step-by-step instructions, click [here](play-multiplayer.md#joining-a-public-wan-server).

If you’re referring to servers in the local server browser, check [here](play-multiplayer.md#joining-a-lan-server).

</details>

<details>

<summary>S04: "This map contains customised content" error when joining a Reclamation server</summary>

Related Article(s): [Apply OpenSpy patches](apply-openspy-patches.md), [Install the map pack](install-map-pack.md)

You might have an outdated map or be missing the required map.

**Symptom(s):**

* "This map contains customized content. The map creator might have more information about the map on the community site."

**Solution(s):**

* Download the map pack or the specific map the server is running.
* If you already have the map or map pack, note which map is causing issues, uninstall it, and then reinstall it using BF2142 Hub’s individual map option.
* If you get kicked with this message when the server changes maps, that’s normal — just rejoin the server.

</details>

<details>

<summary>S05: "This server only allows players with unmodified content to join" error when joining a server</summary>

Related Article(s): [Play multiplayer](play-multiplayer.md)

You may have modified files in your current mod or tried to join the server with the wrong mod selected.

**Symptom(s):**

* "This server only allows players with unmodified content to join. Revert your version of Battlefield 2142 to the current version to join."

**Solution(s):**

* If you’re joining Reclamation servers or any vanilla servers, make sure you’re using a vanilla BF2142 setup — don’t use any addons or tweaks that change files in `\mods\bf2142`.

- You can only join servers that match the mod and files you have.
  * You can’t join a vanilla server with a mod enabled, or the other way around.
  * To join a modded server, you’ll need to have the exact same mod and files installed as the server.
- Revert your changes before joining Reclamation or any multiplayer servers, unless the server explicitly allows or uses this mod.

</details>

<details>

<summary>S06: Invalid CD-Key error when joining a server</summary>

This issue occurs when the game’s CD key cannot be found in your computer’s registry, likely due to some omitted steps during installation.

**Symptom(s):**

* "Invalid CD-Key"

**Solution(s):**

* Use the CD Key fix feature in BF2142 Hub or Remaster Launcher.
* Navigate to `C:\Program Files (x86)\Electronic Arts\Battlefield 2142\Support`, launch `Battlefield 2142_code.exe`, and enter a [CD key](#user-content-fn-2)[^2].

- Inject the registry file from [https://www.regfiles.net/registry/battlefield-2142-registry](https://www.regfiles.net/registry/battlefield-2142-registry) into your PC.
  * Adjust the `PATH` and [`CDKEY`](#user-content-fn-2)[^2] before downloading.
  * Edit the file with a text editor and change `Version` to `1.51` and `BuildNr` to `1.10.77.0`.
  * Save the changes and double-click the file to install it.
- Reinstall the game.

To play on NovGames servers, make sure you run the <mark style="color:blue;">ACTIVATOR</mark> and click the <mark style="color:blue;">Activate</mark> button at least once to apply the NovGames CD key fix. This step is usually completed during installation.

</details>

### (H) BF2142 Hub

<details>

<summary>H01: App exception or mdIBF error when starting BF2142 Hub</summary>

This usually happens when your ISP blocks certain IP addresses, which prevent BF2142 Hub from communicating with external services, or if the game’s information hasn’t been added to your computer’s registry, likely due to omitted steps during installation.

**Symptom(s):**

* "mdIBF.ReadConfig: Unexpected character encountered while parsing value: <. Path ", line 0, position 0."
* "mdIBF.\*\*\*\*: Object reference not set to an instance of an object."
* "the type initialisation function for b2142\_hub MDIBFclient has causes an exeption."

**Solution(s):**

* Use a VPN service, such as ExpressVPN or ProtonVPN, to bypass ISP restrictions.

- Inject the registry file from [https://www.regfiles.net/registry/battlefield-2142-registry](https://www.regfiles.net/registry/battlefield-2142-registry) into your PC.
  * Adjust the `PATH` and [`CDKEY`](#user-content-fn-2)[^2] before downloading.
  * Edit the file with a text editor and change `Version` to `1.51` and `BuildNr` to `1.10.77.0`.
  * Save the changes and double-click the file to install it.
- Reinstall the game.

</details>

<details>

<summary>H02: BF2142 Hub scaling looks messed up or distorted</summary>

Sometimes, Windows scaling settings can interfere with an app's display, causing weird scaling or visual glitches. You can fix this by running the app in compatibility mode:

1. Right-click BF2142 Hub's shortcut and select <mark style="color:blue;">Properties</mark>.
2. In the <mark style="color:blue;">Compatibility</mark> tab, click <mark style="color:blue;">Change high DPI settings</mark>.
3. Under <mark style="color:blue;">High DPI scaling override</mark>, check <mark style="color:blue;">Override high DPI scaling behavior</mark>.
4. Set <mark style="color:blue;">Scaling performed by:</mark> to <mark style="color:blue;">Application</mark>.
5. Click <mark style="color:blue;">Apply</mark> and <mark style="color:blue;">OK</mark>.

</details>

[^1]: Whenever you install a new patch from BF2142 Hub, it updates your `BF2142.exe`, which means your compatibility settings will be reset.

[^2]: e.g., `E6HH-DWUG-U8X1-R8F0-1911`
