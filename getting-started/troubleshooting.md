---
description: Got Issues? Find Answers Here!
---

# ⍟ Troubleshooting

This is your go-to spot for solutions to some of the most common problems you might run into. If you're facing something that isn't covered here, definitely head over to the [Reclamation FAQ page](https://battlefield2142.co/faq/) — you'll find even more helpful info there!

<details>

<summary>When I click Host or Singleplayer in BF2142Unlocker, the game crashes.</summary>

Related Article(s): [BF2142Unlocker](../addons-tweaks/bf2142unlocker.md)

{% hint style="warning" %}
Currently, you can’t play online with BF2142Unlocker, but master server emulation still works.&#x20;
{% endhint %}

`127.0.0.1` is usually the culprit behind most issues after clicking <mark style="color:blue;">Host</mark> or <mark style="color:blue;">Singleplayer</mark>. For details on how to troubleshoot, check [here](../addons-tweaks/bf2142unlocker.md#troubleshooting).

</details>

<details>

<summary>When I run the game in windowed mode, the scaling is off and everything looks distorted.</summary>

Related Article(s): [Install OpenSpy Patches](apply-openspy-patches.md)

If you’re using Windows display scaling, you might run into scaling issues when launching the game in windowed mode **\[**[**?**](#user-content-fn-1)[^1]**]**. You can fix this by running the game in compatibility mode:

1. Go to the folder where your `BF2142.exe` is located — by default, that’s usually `C:\Program Files (x86)\Electronic Arts\Battlefield 2142`.
2. Right-click `BF2142.exe` and select <mark style="color:blue;">Properties</mark>.
3. In the <mark style="color:blue;">Compatibility</mark> tab, click <mark style="color:blue;">Change high DPI settings</mark>.
4. Under <mark style="color:blue;">High DPI scaling override</mark>, check <mark style="color:blue;">Override high DPI scaling behavior</mark> and set <mark style="color:blue;">Scaling performed by:</mark> to <mark style="color:blue;">Application</mark>.
5. Click <mark style="color:blue;">Apply</mark> and <mark style="color:blue;">OK</mark>.

Just a heads up: you’ll need to repeat these steps every time you click the install button in BF2142 Hub. **\[**[**?**](#user-content-fn-2)[^2]**]**

</details>

<details>

<summary>When I run BF2142 Hub, the scaling is messed up and everything looks distorted.</summary>

If you’re running BF2142 Hub and everything looks distorted, it’s likely due to Windows display scaling. You can fix this by running the app in compatibility mode:

1. Right-click BF2142 Hub's shortcut and select <mark style="color:blue;">Properties</mark>.
2. In the <mark style="color:blue;">Compatibility</mark> tab, click <mark style="color:blue;">Change high DPI settings</mark>.
3. Under <mark style="color:blue;">High DPI scaling override</mark>, check <mark style="color:blue;">Override high DPI scaling behavior</mark> and set <mark style="color:blue;">Scaling performed by:</mark> to <mark style="color:blue;">Application</mark>.
4. Click <mark style="color:blue;">Apply</mark> and <mark style="color:blue;">OK</mark>.

</details>

<details>

<summary>When I try to to adjust audio settings, the game crashes.</summary>

Game crashes like this can be caused by virtual audio drivers. If you have VirtualCable or Voicemeeter installed, you’ll likely run into issues.

**Symptoms:**

* The game crashes when you try to adjust audio settings in-game, **AND**
* The game crashes when joining a match, sometimes with audio beeping just before the crash.

**Solutions:**

* Open Device Manager and disable any virtual drivers.

- In the game’s audio settings, set audio rendering to software and turn off EAX.

</details>

<details>

<summary>When I start the game, "Runtime Error" or "dice_py.dll / MSVCR**.dll is missing".</summary>

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

<summary>When joining a game or loading a map, "memory.dll sanity check ... error" pops up.</summary>

Related Article(s): [https://forum.realitymod.com/viewtopic.php?t=80268](https://forum.realitymod.com/viewtopic.php?t=80268)

Symtoms:

* "memory.dll: sanity check: block size xxxxxxx (xxxxxx mb) doesn't seem sane"
* "memory.dll: all alloc attempts failed for size xxxxxxxxx"

Solutions:

* Set pagefile to be managed by the OS.
* In Task Manager, set the game’s affinity to a single core.
* Try lowering your in-game graphics settings (medium or low for everything).
* Turn off Anti-Aliasing in-game.
* Check for BIOS updates for your motherboard.

</details>

<details>

<summary>When I try to login or create an account, "no internet connection" or "EA Master Server is down" pops up.</summary>

Related Article(s): [Install OpenSpy Patches](apply-openspy-patches.md)

Symptoms:

* we
* we

**Soutions:**

* Reinstall the OpenSpy patches and make sure there are four green ticks.
* Restart BF2142 Hub (close it completely, then start it again).
* Reinstall BF2142 Hub if the issue persists.
* Always run BF2142 Hub as an administrator.

- Make sure BF2142 is allowed through both private and public networks in Windows Firewall.

</details>

<details>

<summary>When I start the game, it crashes to Desktop after a black screen.</summary>

Battlefield 2142 can have issues on modern PCs, with the most common cause being incompatible video modes or incorrect video settings.

**Solutions:**

* Try deleting the `Battlefield 2142` folder in `My Documents`. This will clean up your profiles — including any faulty video or audio settings — and clear your shader cache.
  * You can also use the <mark style="color:blue;">Clear Cache</mark> and <mark style="color:blue;">Delete Profile</mark> function in <mark style="color:blue;">BF2142 Hub</mark> or <mark style="color:blue;">Remaster Launcher</mark>, which has a similar effect.
* Try launching the game in windowed mode, and be sure to use a resolution and refresh rate that your monitor supports.&#x20;
  * For example, if your monitor doesn’t support 120Hz and you select it, the game may crash. You can easily adjust these settings using <mark style="color:blue;">BF2142 Hub</mark> or <mark style="color:blue;">Remaster Launcher</mark>.
  * If you’re launching the game with the vanilla BF2142 shortcut, check the [Shortcut Guide](https://www.moddb.com/tutorials/how-to-install-and-start-any-bf2142-mod-universal-tutorial-with-pictures) for instructions on setting launch parameters for windowed mode and a fixed resolution.
* Try running the [vidcon fix](https://battlefield2142.co/bf2142_vidcon_fix.exe) and see if it helps. \[[Ref](https://battlefield2142.co/faq/#blackscreen)]

</details>

<details>

<summary>I can see strange graphical glitches or see through buildings.</summary>

It’s usually because the old DirectX9 engine is trying to use anti-aliasing with a modern graphics card.

To fix this, turn the anti-aliasing slider OFF in the in-game OPTIONS → VIDEO menu. Then, if you want anti-aliasing, use your NVIDIA or AMD control panel to set it up for your graphics card instead.

</details>

<details>

<summary>I see no servers in the server browser even though I have OpenSpy patches.</summary>

Related Article(s): [Play Multiplayer](play-multiplayer.md)

To see servers in the list, make sure to uncheck all the server filter options. For step-by-step instructions, see [here](play-multiplayer.md#joining-a-public-wan-server).

</details>

<details>

<summary>When I look around, I notice mouse skipping / stuttering / jumping aimpoint.</summary>

Related Article(s): [Stuttering, mouse skipping & FPS cap](https://www.lost-soldiers.org/v2.php?site=forum_topic\&topic=81\&type=ASC\&page=2#bigNO)

This issue may be related to the game’s animation system or engine itself.

**Symptoms:**

* Stand still (don’t move forward or backward; moving sideways is fine—the issue will still appear).
* Move your mouse only horizontally; the problem doesn’t occur vertically.
* The stutter happens when you move the mouse fast or over a long distance. Small aim adjustments are usually fine, but consistent sideways movement, even at slow speeds, can cause skipped frames.

**Solutions:**\
Unfortunately, there’s currently no known fix for this issue.

</details>

<details>

<summary>I keep getting kicks when playing on a Reclamation / NovGames server.</summary>

First, make sure you’re joining the server using vanilla 2142 (that is, `\mods\bf2142`) and that there aren’t any major modifications in your `\mods\bf2142` folder.

If you’re still having trouble, try using the CD Key fix feature in BF2142 Hub or Remaster Launcher — CD key issues can sometimes cause connection problems.

To play on NovGames servers, make sure you run the <mark style="color:blue;">ACTIVATOR</mark> and click the <mark style="color:blue;">Activate</mark> button at least once to apply the NovGames CD key fix. This step is usually completed during installation.

</details>

<details>

<summary>When joining a Reclamation server, "this map contains customised content" pops up.</summary>

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

<summary>When joining a server, "this server only allows players with unmodified content to join" pops up.</summary>

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

[^1]: Sometimes, Windows scaling settings can clash with a game’s display settings, which may cause incorrect scaling or visual glitches.

[^2]: Whenever you install a new patch from BF2142 Hub, it updates your `BF2142.exe`, which means your compatibility settings will be reset.
