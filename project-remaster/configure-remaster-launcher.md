---
description: How to configure the launcher? How to start the game with the launcher?
---

# ② Configure Remaster Launcher

This tutorial will walk you through how to configure the launcher and use it to launch the game. If you have any questions or run into any issues, don’t hesitate to join our [Discord server](https://discord.com/invite/VnxTDPBebZ) — we’re always happy to help!y

## Procedures

{% hint style="warning" %}
Before configuring the launcher, make sure you’ve started the game at least once. **\[**[**?**](#user-content-fn-1)[^1]**]**
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
When prompted by [<mark style="color:blue;">User Account Contro</mark>](#user-content-fn-2)[^2]<mark style="color:blue;">l</mark>, click <mark style="color:blue;">Yes</mark> to allow the app to make changes on your device.
{% endstep %}

{% step %}
Go to the <mark style="color:blue;">Play</mark> page.
{% endstep %}

{% step %}
Under the <mark style="color:blue;">Launch-Settings</mark> section, disable the [<mark style="color:blue;">4GB Ram Patch</mark>](#user-content-fn-3)[^3] option. **\[**[**?**](#user-content-fn-4)[^4]**]**
{% endstep %}

{% step %}
Navigate to the <mark style="color:blue;">Settings</mark> page.
{% endstep %}

{% step %}
Enable options like <mark style="color:blue;">Unlock FPS (120HZ)</mark>, <mark style="color:blue;">Widescreen Fix</mark>, [<mark style="color:blue;">HUD-Fix</mark>](#user-content-fn-5)[^5], <mark style="color:blue;">Blood Patch</mark> and <mark style="color:blue;">Reshade</mark> under the <mark style="color:blue;">General</mark> section.
{% endstep %}

{% step %}
Adjust <mark style="color:blue;">Resolution</mark> from the drop-down menu to match the one you have in-game.
{% endstep %}

{% step %}
Go to the <mark style="color:blue;">Help</mark> page.
{% endstep %}

{% step %}
Check if the debug message includes these lines:\
<mark style="color:green;">Game version: v1.51 OK!</mark>\
<mark style="color:red;">bf2142.exe: Not v1.51 or cracked.</mark>     <sub>(You will see this line if OpenSpy patches are installed properly.)</sub>\ <mark style="color:red;">bf2142\_4gb.exe: Missing! Patch first.</mark>   <sub>(You don't need 4gb ram patch because OpenSpy patches include it)</sub>\
<mark style="color:red;">RendDX9.dll: Wrong file version!</mark>    <sub>(You will see this line if OpenSpy patches are installed properly.)</sub>\
<mark style="color:green;">RendDX9\_ori.dll: OK!</mark>\
<mark style="color:yellow;">Profile: Found, delete if stuck with a black screen.</mark>  <sub>(You will see this line if you logged in before.)</sub>
{% endstep %}

{% step %}
Return to the <mark style="color:blue;">Play</mark> page.&#x20;
{% endstep %}

{% step %}
Click <mark style="color:blue;">Start Game!</mark> to launch the game.
{% endstep %}

{% step %}
The game may take a few seconds to start, so expect a brief black screen before the intro appears. **\[**[**?**](#user-content-fn-6)[^6]**]**
{% endstep %}

{% step %}
Be sure to read all the [Remarks](configure-remaster-launcher.md#remarks) — they’re important!
{% endstep %}

{% step %}
_**Congratulations! You have completed all the steps to get Remaster up and running! See you on the battlefield!**_
{% endstep %}
{% endstepper %}

## Remarks

<details>

<summary>Just a few things to note ...</summary>

* If you want to play an unmodded game or join an unmodded server, simply uncheck all options under <mark style="color:blue;">Play</mark> → <mark style="color:blue;">Launch-Settings</mark> and <mark style="color:blue;">Settings</mark> → <mark style="color:blue;">General</mark> before launching the game. **\[**[**?**](#user-content-fn-7)[^7]**]**

- Vanilla weapons is a mini-mod included with Project Remaster. Enable this option if you want to play with weapons and gadgets that have their original (vanilla) stats.

* The <mark style="color:blue;">Play Offline</mark> page lets you launch the Offline Singleplayer mini-mod. This version bypasses the master server and disables customization features.

- You can adjust the Reshade overlay in-game by pressing <mark style="color:blue;">Shift+F2</mark>. If you notice any graphical glitches, try turning off the LUT on certain maps.

* If you run into issues like crashes, the game not starting, or graphics glitches, the troubleshooting and diagnosis tools on the <mark style="color:blue;">Help</mark> page are very useful. The offline manual included with the launcher can also provide helpful tips for fixing problems.

</details>

## Follow-ups

New to the mod or modding? We’ve got some manuals packed with helpful info, so it’s definitely worth setting aside a little time to check them out!

* [Remaster Manual](further-readings.md)
* [Tweak Guide](further-readings.md)
* [Modding Wiki](https://classic-battlefield-modding.fandom.com/wiki/Classic_Battlefield_Modding_Wikia)

Also, take a look at the addons and tweaks section in the sidebar navigation — you might find something that interests you!

[^1]: It’s not strictly mandatory, but it does make things easier. Starting the game once will create a profile for you, which allows you to set the launch resolution in Remaster Launcher.

[^2]: i.e., Do you want to allow this app from an unknown publisher to make changes to your device?

[^3]: Battlefield 2142 is a 32-bit game, so it can use a maximum of 4GB of RAM. The 4GB RAM Patch helps prevent crashes caused by memory overflow, making the game more stable even though it can’t use more than 4GB.

[^4]: We need to disable this option because the OpenSpy patches from BF2142 Hub already include this fix by default.

[^5]: You should clear your shader-cache when enabling / disabling this setting, else the game will crash.



    To clear the shader cache:

    * Go to the <mark style="color:blue;">Settings</mark> page.
    * Click the <mark style="color:blue;">Clear Chache</mark> button.

[^6]: If you are using the full-screen mode, you may see the game blinking or resizing for a few times.

[^7]: This ensures you’re running a pure, unmodded version, which is required for vanilla servers, or you may get kicked by anti-cheat for modified content.
