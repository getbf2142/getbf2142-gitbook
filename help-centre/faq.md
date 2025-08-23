---
description: Frequently Asked Questions
icon: message-question
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

# FAQ

This is where you find answers to some of the commonly asked questions. If you have questions that aren’t answered here, be sure to check out the [Reclamation FAQ page](https://battlefield2142.co/faq/) for more information.

### (G) General

<details>

<summary>G01: How do I get all the unlocks ?</summary>

Related Article(s): [Apply OpenSpy patches](../getting-started/apply-openspy-patches.md), [BF2142Unlocker](../advanced/addons-tweaks/bf2142unlocker.md)

When you use OpenSpy as your login service, you get access to all unlocks as soon as you create a soldier. This means you’ll have all unlocks available in Singleplayer and LAN, provided you’re connected to the internet and OpenSpy is online.

If you want access to all unlocks without needing an internet connection or OpenSpy, use [BF2142Unlocker](../advanced/addons-tweaks/bf2142unlocker.md). This tool lets you host a master server locally on your own system.

</details>

<details>

<summary>G02: How to reset my password ?</summary>

Related Article(s): [Create an account](../getting-started/create-account.md)

OpenSpy now lets you reset your password and manage your account at [https://account.openspy.net/login](https://account.openspy.net/login) (use Partner Code 20 - EA).

</details>

<details>

<summary>G03: How to change the language ?</summary>

If you already have the [Remaster mod](../advanced/project-remaster/download-and-install-remaster-mod.md) installed, you can easily switch languages using the <mark style="color:blue;">Remaster Launcher</mark>.

If you don’t have the mod, follow these steps to change the language manually:

1. Press <mark style="color:blue;">WIN + R</mark>, type `regedit`, and press <mark style="color:blue;">Enter</mark>.
2. Navigate to `HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Electronic Arts\EA GAMES\Battlefield 2142`.
3. Change the value of <mark style="color:blue;">Locale</mark> to the code of the language you want (refer to the table below).

If the corresponding entries are missing in the registry, you may need to manually install the registry files:

1. Download the registry file from [https://www.regfiles.net/registry/battlefield-2142-registry](https://www.regfiles.net/registry/battlefield-2142-registry).
   * **Note:** If your game is installed through Origin/EA App, reinstall the game instead and avoid using this file.
2. Adjust the <mark style="color:blue;">PATH</mark> and <mark style="color:blue;">CDKEY</mark> before downloading.
3. Open the file with a text editor and update:
   * <mark style="color:blue;">Version</mark> to `1.51`.
   * <mark style="color:blue;">BuildNr</mark> to `1.10.77.0`.
4. Save the changes and double-click the file to install it.

| Code   | Language              |
| ------ | --------------------- |
| cs     | Czech                 |
| da     | Danish                |
| de     | German                |
| el     | Greek                 |
| en\_UK | English (UK)          |
| en\_US | English (US)          |
| es     | Spanish               |
| fi     | Finnish               |
| fr\_FR | French                |
| hu     | Hungarian             |
| it     | Italian               |
| ja     | Japanese              |
| ko     | Korean                |
| nl     | Dutch                 |
| no     | Norwegian             |
| pl     | Polish                |
| pt\_BR | Portuguese (Brazil)   |
| pt\_PT | Portuguese (Portugal) |
| ru     | Russian               |
| sv     | Swedish               |
| th     | Thai                  |
| zh\_CN | Chinese (Simplified)  |
| zh\_tw | Chinese (Traditional) |

</details>

<details>

<summary>G04: How to play with bots ?</summary>

Conquest Co-op (gpm\_coop) mode is the game mode that spawns bots, and any Conquest Co-op map will support them.

* **Singleplayer:** Conquest Co-op is the default mode, so there’s no need to worry about selecting it.
* **LAN:** Make sure to select Conquest Co-op as the game mode to play with bots.

</details>

### (AT) Addons / Tweaks

<details>

<summary>AT01: How to change field of view in-game ?</summary>

You can’t change the FOV (field of view) in-game, since BF2142 is an older title and doesn’t offer as many video settings as modern games.&#x20;

However, you can still achieve this by editing the game files. For step-by-step instructions, check out our [Field of View (FOV)](../advanced/addons-tweaks/fov.md) guide.

</details>

<details>

<summary>AT02: How to add more bots in Singleplayer or Multiplayer LAN ?</summary>

Refer to our [Add More Bots](../advanced/addons-tweaks/add-more-bots.md) guide for more details.

</details>

<details>

<summary>AT03: How to adjust ticket counts, team ratio, and respawn time in Singleplayer ?</summary>

Refer to our [Server Settings](../advanced/addons-tweaks/server-settings.md) guide for more details.

</details>

<details>

<summary>AT04: How to adjust more server settings other than those avilable in the game menu ?</summary>

Refer to our [Server Settings](../advanced/addons-tweaks/server-settings.md) guide for more details.

</details>

<details>

<summary>AT05: Where can I get more maps with bot support ?</summary>

Refer to our [Maps with Bots](../advanced/addons-tweaks/maps-with-bots.md) guide for more details.

</details>
