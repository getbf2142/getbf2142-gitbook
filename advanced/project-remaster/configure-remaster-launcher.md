---
description: How to configure the launcher? How to start the game with the launcher?
icon: '2'
---

# Configure the Remaster Launcher

This tutorial will walk you through how to configure the launcher and use it to launch the game. If you hit any snags or have questions, hop into our [Discord](https://discord.gg/7SBMKRy6q9) — we’re always happy to help!

{% embed url="https://discord.com/invite/nVdDkgA" %}

<details>

<summary>Important Notes</summary>

* If you want to play unmodded or join an unmodded server, uncheck all options under <mark style="color:blue;">Play</mark> → <mark style="color:blue;">Launch-Settings</mark> and <mark style="color:blue;">Settings</mark> → <mark style="color:blue;">General</mark> before launching.

- If you hit crashes, startup issues, or graphics glitches, use the troubleshooting and diagnosis tools on the <mark style="color:blue;">Help</mark> page. The offline manual in the launcher also has helpful fixes.

</details>

## Procedures

{% hint style="warning" %}
Before configuring the launcher, make sure you’ve started the game at least once. **\[**[**?**](#user-content-fn-1)[^1]**]**\
Make sure you’ve [installed OpenSpy patches](../../getting-started/apply-openspy-patches.md) via BF2142 Hub.
{% endhint %}

{% stepper %}
{% step %}
Right-click the <mark style="color:blue;">Remaster Launcher</mark> shortcut on your desktop and select <mark style="color:blue;">Properties</mark>.&#x20;
{% endstep %}

{% step %}
Go to the <mark style="color:blue;">Compatibility</mark> tab, check <mark style="color:blue;">Run this program as an administrator</mark>, then click <mark style="color:blue;">Apply</mark> and <mark style="color:blue;">OK</mark>.
{% endstep %}

{% step %}
Double-click the <mark style="color:blue;">Remaster Launcher</mark> shortcut to start the launcher.
{% endstep %}

{% step %}
When prompted by <mark style="color:blue;">User Account Control</mark>, click <mark style="color:blue;">Yes</mark> to allow the app to make changes on your device.
{% endstep %}

{% step %}
Go to the <mark style="color:blue;">Play</mark> page.
{% endstep %}

{% step %}
Under the <mark style="color:blue;">Launch-Settings</mark> section, disable the [<mark style="color:blue;">4GB Ram Patch</mark>](#user-content-fn-2)[^2] option. **\[**[**?**](#user-content-fn-3)[^3]**]**
{% endstep %}

{% step %}
Navigate to the <mark style="color:blue;">Settings</mark> page.
{% endstep %}

{% step %}
Enable options like <mark style="color:blue;">Unlock FPS (120HZ)</mark>, <mark style="color:blue;">Widescreen Fix</mark>, [HUD-Fix](../addons-tweaks/hudfix.md), <mark style="color:blue;">Blood Patch</mark> and [ReShade](../addons-tweaks/reshade.md) under the <mark style="color:blue;">General</mark> section.
{% endstep %}

{% step %}
Adjust <mark style="color:blue;">Resolution</mark> from the drop-down menu to match the one you have in-game.
{% endstep %}

{% step %}
Return to the <mark style="color:blue;">Play</mark> page.&#x20;
{% endstep %}

{% step %}
Click <mark style="color:blue;">Start Game!</mark> to launch the game.
{% endstep %}

{% step %}
_**Congratulations! You have completed all the steps to get Remaster up and running! See you on the battlefield!**_
{% endstep %}
{% endstepper %}

## Follow-ups

New to the mod or modding? We’ve got some manuals packed with helpful info, so it’s definitely worth setting aside a little time to check them out!

* [Remaster Manual](further-readings.md)
* [Tweak Guide](further-readings.md)
* [Modding Wiki](https://classic-battlefield-modding.fandom.com/wiki/Classic_Battlefield_Modding_Wikia)

Also, take a look at the addons and tweaks section in the sidebar navigation — you might find something that interests you!

[^1]: It’s not strictly mandatory, but it does make things easier. Starting the game once will create a profile for you, which allows you to set the launch resolution in Remaster Launcher.

[^2]: Battlefield 2142 is a 32-bit game, so it can use a maximum of 4GB of RAM. The 4GB RAM Patch helps prevent crashes caused by memory overflow, making the game more stable even though it can’t use more than 4GB.

[^3]: We need to disable this option because the OpenSpy patches from BF2142 Hub already include this fix by default.
