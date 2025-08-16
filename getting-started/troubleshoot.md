---
description: Got Issues? Find Answers Here!
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

<summary>G02: BF2142 Hub scaling looks messed up or distorted</summary>

Sometimes, Windows scaling settings can interfere with an app's display, causing weird scaling or visual glitches. You can fix this by running the app in compatibility mode:

1. Right-click BF2142 Hub's shortcut and select <mark style="color:blue;">Properties</mark>.
2. In the <mark style="color:blue;">Compatibility</mark> tab, click <mark style="color:blue;">Change high DPI settings</mark>.
3. Under <mark style="color:blue;">High DPI scaling override</mark>, check <mark style="color:blue;">Override high DPI scaling behavior</mark>.
4. Set <mark style="color:blue;">Scaling performed by:</mark> to <mark style="color:blue;">Application</mark>.
5. Click <mark style="color:blue;">Apply</mark> and <mark style="color:blue;">OK</mark>.

</details>

<details>

<summary>G03: Experiencing weird graphics glitches like blackouts, ghost objects, etc.</summary>

It’s usually because the old DirectX9 engine is trying to use anti-aliasing with a modern graphics card.

**Symptoms:**

* See-through buildings
* Ghost objects (e.g., invisible terrain or soldier units)
* Blackouts of certain objects

**Solutions:**

* Turn off Anti-Aliasing in-game.
  * If you want anti-aliasing, use your NVIDIA or AMD control panel to set it up for your graphics card instead.
* Delete the `Battlefield 2142` folder in `C:\Users\...\Documents`. This will clean up your profiles — including any faulty video or audio settings — and clear your shader cache.
  * You can also use the <mark style="color:blue;">Clear Cache</mark> and <mark style="color:blue;">Delete Profile</mark> function in <mark style="color:blue;">BF2142 Hub</mark> or <mark style="color:blue;">Remaster Launcher</mark>, which has a similar effect.

</details>

<details>

<summary>G04: Experiencing mouse skipping, stuttering, or a jumping aimpoint</summary>

Related Article(s): [Stuttering, mouse skipping & FPS cap](https://www.lost-soldiers.org/v2.php?site=forum_topic\&topic=81\&type=ASC\&page=2#bigNO)

This issue may be related to the game’s animation system or engine itself, and has nothing to do with mouse polling rate.

**Symptoms:**

* Stand still (don’t move forward or backward; moving sideways is fine—the issue will still appear).
* Move your mouse only horizontally; the problem doesn’t occur vertically.
* The stutter happens when you move the mouse fast or over a long distance. Small aim adjustments are usually fine, but consistent sideways movement, even at slow speeds, can cause skipped frames.

**Solutions:**\
Unfortunately, there’s currently no known fix for this issue.

</details>

### (C) Crashes

<details>

<summary>C01: Game crashes to desktop after a flashing black screen</summary>

BF2142 can have issues on modern PCs, with the most common cause being incompatible video modes or incorrect video settings.

**Symptoms:**

* The game crashes after a flashing black screen.
* The game crashes way before the game intro or game menu shows.

**Solutions:**

* Delete the `Battlefield 2142` folder in `C:\Users\...\Documents`. This will clean up your profiles — including any faulty video or audio settings — and clear your shader cache.
  * You can also use the <mark style="color:blue;">Clear Cache</mark> and <mark style="color:blue;">Delete Profile</mark> function in <mark style="color:blue;">BF2142 Hub</mark> or <mark style="color:blue;">Remaster Launcher</mark>, which has a similar effect.
* Launch the game in windowed mode, and be sure to use a resolution and refresh rate that your monitor supports.&#x20;
  * For example, if your monitor doesn’t support 120Hz and you select it, the game may crash. You can easily adjust these settings using <mark style="color:blue;">BF2142 Hub</mark> or <mark style="color:blue;">Remaster Launcher</mark>.
  * Navigate to `C:\Users\...\Documents\Battlefield 2142\Profiles\Default\Video.con` and update the resolution and frequency to `800x600@60Hz` on the line that says: `VideoSettings.setResolution`. Once done, repeat this process in the `0001` profile folder as well.
  * If you’re launching the game with the vanilla BF2142 shortcut, check the [Shortcut Guide](https://www.moddb.com/tutorials/how-to-install-and-start-any-bf2142-mod-universal-tutorial-with-pictures) for instructions on setting launch parameters for windowed mode and a fixed resolution.
* Run the [vidcon fix](https://battlefield2142.co/bf2142_vidcon_fix.exe) and see if it helps. \[[Ref](https://battlefield2142.co/faq/#blackscreen)]

</details>

<details>

<summary>C02: Game crashes when adjusting audio settings</summary>

Game crashes like this can be caused by virtual audio drivers. If you have VirtualCable or Voicemeeter installed, you’ll likely run into issues.

**Symptoms:**

* The game crashes when you try to adjust audio settings in-game, **AND**
* The game crashes when joining a match, sometimes with audio beeping just before the crash.

**Solutions:**

* Open Device Manager and disable any virtual drivers.

- In the game’s audio settings, set audio rendering to software and turn off EAX.

</details>

<details>

<summary>C03: "Runtime Error" or "dice_py.dll / MSVCR**.dll is missing" error when starting the game</summary>

If you see a Runtime Error or messages about `dice_py.dll` or `MSVCR**.dll` missing when launching the game, it usually means you’re missing the Microsoft Visual C++ Runtime Library.

**Symptoms:**

* "The code execution cannot proceed because MSVCP71.dll was not found. Reinstalling the program may fix this problem."
* "The code execution cannot proceed because dice\_py.dll was not found. Reinstalling the program may fix this problem."
* "Runtime Error! This application has requested the Runtime to terminate it in an unusual way."

**Solutions:**

* Install the [Microsoft Visual C++ Runtime Library](https://aka.ms/vs/17/release/vc_redist.x86.exe).
* Make sure your Windows is up to date.

</details>

<details>

<summary>C04: "memory.dll sanity check" error when joining a game or loading a map </summary>

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

<summary>C05: Game crashes when clicking Host or Singleplayer in BF2142Unlocker</summary>

Related Article(s): [BF2142Unlocker](../addons-tweaks/bf2142unlocker.md)

`127.0.0.1` is usually the culprit behind most issues after clicking <mark style="color:blue;">Host</mark> or <mark style="color:blue;">Singleplayer</mark>. For details on how to troubleshoot, check [here](../addons-tweaks/bf2142unlocker.md).

</details>

### (S) Servers

<details>

<summary>S01: "No internet connection" or "EA Master Server is down" when logging in or creating an account</summary>

Related Article(s): [Install OpenSpy Patches](apply-openspy-patches.md)

Symptoms:

* "You are not connected to the Internet. Click OK to select a soldier to play offline, or try to reconnect."
* "Could not connect to EA Online. Retry, or click OK to go into Offline mode. If you proceed, try logging in again later."
* "Could not connect to EA Online."
* "EA Master Server is down."
* "EA Master Server is down. Please use BF2142Unlocker."

**Soutions:**

* Reinstall the OpenSpy patches and make sure there are four green ticks.
* Restart BF2142 Hub (close it completely, then start it again).
* Reinstall BF2142 Hub if the issue persists.
* Always run BF2142 Hub as an administrator.

- Make sure BF2142 is allowed through both private and public networks in Windows Firewall.

</details>

<details>

<summary>S02: No servers showing in the server browser, even with OpenSpy patches installed</summary>

Related Article(s): [Play Multiplayer](play-multiplayer.md)

To see servers in the list, make sure to uncheck all the server filter options. For step-by-step instructions, see [here](play-multiplayer.md#joining-a-public-wan-server).

</details>

<details>

<summary>S03: Getting kicked when playing on Reclamation or NovGames servers</summary>

First, make sure you’re joining the server using vanilla 2142 (that is, `\mods\bf2142`) and that there aren’t any major modifications in your `\mods\bf2142` folder.

If you’re still having trouble, try using the CD Key fix feature in BF2142 Hub or Remaster Launcher — CD key issues can sometimes cause connection problems.

To play on NovGames servers, make sure you run the <mark style="color:blue;">ACTIVATOR</mark> and click the <mark style="color:blue;">Activate</mark> button at least once to apply the NovGames CD key fix. This step is usually completed during installation.

</details>

<details>

<summary>S04: "This map contains customised content" error when joining a Reclamation server</summary>

Related Article(s): [Install OpenSpy Patches](apply-openspy-patches.md), [Reclamation Map Pack](apply-openspy-patches.md#reclamation-map-pack)

You might have an outdated map or be missing the required map.

**Symptoms:**

* "This map contains customized content. The map creator might have more information about the map on the community site."

**Solution:**

* Download the map pack or the specific map the server is running.
* If you already have the map or map pack, note which map is causing issues, uninstall it, and then reinstall it using BF2142 Hub’s individual map option.
* If you get kicked with this message when the server changes maps, that’s normal — just rejoin the server.

</details>

<details>

<summary>S05: "This server only allows players with unmodified content to join" error when joining a server</summary>

Related Article(s): [Play Multiplayer](play-multiplayer.md)

You may have modified files in your current mod or tried to join the server with the wrong mod selected.

**Symptoms:**

* "This server only allows players with unmodified content to join. Revert your version of Battlefield 2142 to the current version to join."

**Solution:**

* If you’re joining Reclamation servers or any vanilla servers, make sure you’re using a vanilla BF2142 setup — don’t use any addons or tweaks that change files in `\mods\bf2142`.

- You can only join servers that match the mod and files you have.
  * You can’t join a vanilla server with a mod enabled, or the other way around.
  * To join a modded server, you’ll need to have the exact same mod and files installed as the server.
- Revert your changes before joining Reclamation or any multiplayer servers, unless the server explicitly allows or uses this mod.

</details>

[^1]: Whenever you install a new patch from BF2142 Hub, it updates your `BF2142.exe`, which means your compatibility settings will be reset.
