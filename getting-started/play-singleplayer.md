---
description: How to play singleplayer? How to start a singleplayer game?
---

# ⍟ Play Singleplayer

In this tutorial, we’ll walk you through two different ways to enjoy singleplayer mode. If you have any questions or run into any issues, don’t hesitate to join our [Discord server](https://discord.com/invite/VnxTDPBebZ) — we’re always happy to help!

### Setting up a quick game in "SINGLEPLAY"&#x20;

This option offers a limited experience — you won’t be able to adjust settings like ticket ratio, team ratio, round time, friendly fire, or spawn time.

Once your game is [OpenSpy-ready](apply-openspy-patches.md), the customization screen will work properly, and all unlocks will be available in-game.

{% stepper %}
{% step %}
Select <mark style="color:blue;">SINGLEPLAY</mark>.
{% endstep %}

{% step %}
Configure your game settings and click <mark style="color:blue;">START PLAYLIST</mark>.

Check out the [Server Settings Tweak](../addons-tweaks/server-settings-tweak.md) guide for details on extra cutomization settings.
{% endstep %}
{% endstepper %}

### **Setting up a LAN server in "MULTIPLAY"**

This option lets you adjust game settings such as ticket ratio, team ratio, round time, friendly fire, spawn time, and more.

Once your game is [OpenSpy-ready](apply-openspy-patches.md), the customization screen will work properly, and all unlocks will be available in-game.

{% stepper %}
{% step %}
Select <mark style="color:blue;">MULTIPLAY</mark> → <mark style="color:blue;">LOCAL</mark> → <mark style="color:blue;">CREATE</mark>.
{% endstep %}

{% step %}
Configure your game settings and click <mark style="color:blue;">START SERVER</mark>.

Check out the [Server Settings Tweak](../addons-tweaks/server-settings-tweak.md) guide for details on extra cutomization settings.
{% endstep %}
{% endstepper %}

<details>

<summary>Solution to “1 more player to start game” issue when playing solo</summary>

You need this setting:

```
sv.numPlayersNeededToStart 1
```

Check out the [Server Settings Tweak](../addons-tweaks/server-settings-tweak.md) guide for instructions on how to do this.

</details>
