# ⍟ Play Singleplayer

In this tutorial, we’ll walk you through three different ways to enjoy singleplayer mode.

## Setting up a quick game in "SINGLEPLAY"&#x20;

This option offers a limited experience — you won’t be able to adjust settings like ticket ratio, team ratio, round time, friendly fire, or spawn time.

Once your game is [OpenSpy-ready](apply-openspy-patches.md), the customization screen will work properly, and all unlocks will be available in-game.

1. Click <mark style="color:blue;">SINGLEPLAY</mark>.
2. Configure your game settings and click <mark style="color:blue;">START PLAYLIST</mark>.

Check out the [Server Settings Tweak](../addons-tweaks/server-settings-tweak.md) guide for details on customizing your game with extra settings.

## **Setting up a LAN server in "MULTIPLAY"**

{% hint style="warning" %}
Whenever you see a Windows Firewall prompt, be sure to allow the game to communicate through both private and public networks to prevent any connection issues.
{% endhint %}

This option lets you adjust game settings such as ticket ratio, team ratio, round time, friendly fire, spawn time, and more.

Once your game is [OpenSpy-ready](apply-openspy-patches.md), the customization screen will work properly, and all unlocks will be available in-game.

1. ​Click <mark style="color:blue;">MULTIPLAY</mark>.
2. Click <mark style="color:blue;">LOCAL</mark>.
3. Click <mark style="color:blue;">CREATE</mark>.
4. Configure your game settings and click <mark style="color:blue;">START SERVER</mark>.

Check out the [Server Settings Tweak](../addons-tweaks/server-settings-tweak.md) guide for details on customizing your game with extra settings.

<details>

<summary>Solution to “1 more player to start game” issue when playing solo</summary>

You need this setting:

```
set sv.numPlayersNeededToStart 1
```

Check out the [Server Settings Tweak](../addons-tweaks/server-settings-tweak.md) Guide for instructions on how to do this.

</details>
