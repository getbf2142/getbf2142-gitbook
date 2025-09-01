---
description: 'Get online with OpenSpy: Patching your game for action !'
icon: '4'
---

# Apply OpenSpy patches

In this tutorial, we’ll show you how to get your game ready for OpenSpy, including installing the necessary patch and understanding why it's crucial for your online experience. If you hit any snags or have questions, hop into our [Discord](https://discord.gg/7SBMKRy6q9) — we’re always happy to help!

{% embed url="https://discord.com/invite/MEwBW9U" %}

<details>

<summary>What is OpenSpy ?</summary>

[OpenSpy](https://openspy.net/) is an open-source alternative to [GameSpy](https://en.wikipedia.org/wiki/GameSpy#Shutdown), built to work perfectly with all GameSpy-supported games. For Battlefield 2142, the main community using the OpenSpy master server is the Reclamation group.

</details>

<details>

<summary>What is a Master Server ?</summary>

Master Server handles your login details and soldier data, shows you available game servers in your browser, and gets updates from those servers about player progress. OpenSpy is a perfect example of a Master Server that brings online services to games like Battlefield 2142!

</details>

<details>

<summary>Why do we need OpenSpy patches ?</summary>

When GameSpy shut down in 2014, BF2142's original online services went with it. But don't worry! OpenSpy patches redirect your game to use the OpenSpy master server instead, which means you can log in and play online again!

</details>

<details>

<summary>Are there other master servers besides OpenSpy ?</summary>

Yep, there are a few others out there, like [NovGames](https://novgames.ru/), and [PlayBF2142](http://play2142.ru/). But honestly, OpenSpy, especially with the Reclamation community, is the most reliable and active one you'll find. Plus, BF2142 Hub makes it super easy to switch between OpenSpy and NovGames if you want to try them out!

</details>

<details>

<summary>What is Project Reclamation, and how does it tie into OpenSpy ?</summary>

Project Reclamation is a community-driven effort focused on bringing Battlefield 2142's online features back to life!&#x20;

It uses the OpenSpy platform to recreate that master server experience GameSpy originally offered. Basically, Reclamation servers connect directly to the OpenSpy master server, making it super easy for you to find and jump into games, just like in the good old days!

If you want the latest updates or need some help, be sure to join their [Discord](https://discord.com/invite/MEwBW9U) server!

</details>

<details>

<summary>How's the Reclamation community doing ? Still active ?</summary>

<figure><img src="../.gitbook/assets/reclamation_orig.png" alt="" width="563"><figcaption></figcaption></figure>

The Reclamation community is still going strong! There are both EU and US servers, and the English-speaking community is super active on [Discord](https://discord.com/invite/MEwBW9U).

Reclamation EU usually gets busy starting around 6 PM GMT, and Reclamation US picks up around 12 AM GMT. Weekends are even more active than weekdays during these times! You can jump into various game modes like Conquest, Conquest Coop, and Titan **\[**[**?**](#user-content-fn-1)[^1]**]**.

To join in on the fun:

* First, make sure you've installed OpenSpy patches using BF2142 Hub.
* Then, install the Reclamation Map Pack (or any maps currently running on the server) through BF2142 Hub.

Once you've done that, just jump in and you'll find a welcoming and active community ready to play!

</details>

<details>

<summary>Do we get all the unlocks with OpenSpy ?</summary>

Absolutely! Connecting to OpenSpy is a real privilege — you get all the unlocks as soon as you create a new soldier. As long as you're online, you'll have access to everything in both singleplayer and multiplayer modes. That makes it perfect for grinding against bots in a Conquest Coop game!

</details>

## Procedures

{% hint style="danger" %}
BF2142 Hub is a 64-bit application and won’t run on 32-bit Windows XP. If you’re using Windows XP, check out [this guide](https://battlefield2142.co/faq#notwin32) for alternative steps you can take.
{% endhint %}

{% stepper %}
{% step %}
Right-click <mark style="color:blue;">BF2142 Hub</mark> shortcut on your desktop and select <mark style="color:blue;">Properties</mark>.&#x20;
{% endstep %}

{% step %}
Go to the <mark style="color:blue;">Compatibility</mark> tab, check <mark style="color:blue;">Run this program as an administrator</mark>, then click <mark style="color:blue;">Apply</mark> and <mark style="color:blue;">OK</mark>. **\[**[**?**](#user-content-fn-2)[^2]**]**
{% endstep %}

{% step %}
Double-click the shortcut to launch BF2142 Hub.
{% endstep %}

{% step %}
When prompted by <mark style="color:blue;">User Account Control</mark>, click <mark style="color:blue;">Yes</mark> to allow the app to make changes on your device.
{% endstep %}

{% step %}
Go to the <mark style="color:blue;">Help</mark> tab (the question mark icon) and check if the <mark style="color:blue;">GamePath</mark> is set to the correct folder. If it isn't, click the gear icon to locate your game folder.
{% endstep %}

{% step %}
From the <mark style="color:blue;">Redirects\*</mark> drop-down menu, select <mark style="color:blue;">OpenSpy</mark> and click <mark style="color:blue;">Install</mark>.
{% endstep %}

{% step %}
When asked <mark style="color:blue;">Are you sure you want to patch the game?</mark>, click <mark style="color:blue;">Yes</mark> .
{% endstep %}

{% step %}
Once you see <mark style="color:blue;">Patch completed, Enjoy!</mark>, click <mark style="color:blue;">Confirm</mark>.
{% endstep %}

{% step %}
After patching, make sure the checkmarks for `Patch 1.51`, `BF2142.exe`, `RendDX9.d`, `RendDX9ori.dll` are all <mark style="color:green;">green</mark>. If any aren't, repeat from step 6.

If this doesn’t work, consider [installing the patches manually](../help-centre/troubleshoot.md#a05-install-openspy-patches-manually).
{% endstep %}

{% step %}
If you run into issues like crashes, the game not starting, or graphics glitches, the troubleshooting and diagnosis tools on the <mark style="color:blue;">Help</mark> tab are very useful.
{% endstep %}

{% step %}
If you’re using Windows display scaling, you might see scaling issues when launching the game in windowed mode. You can fix this by [enabling High DPI Aware](../help-centre/troubleshoot.md#a01-enable-high-dpi-aware).
{% endstep %}

{% step %}
Next, make sure to [install the map pack](install-map-pack.md) if you plan to play on Reclamation servers. If not, you can skip this step and proceed to [create an account](create-account.md).
{% endstep %}
{% endstepper %}

[^1]: Reclamation servers use some cool auto-managing scripts that tweak maps and game modes depending on how many players are online. Just a heads-up, Titan matches won't kick off until there are at least 20 players in the server!

[^2]: Running as administrator helps prevent permission issues during patching.
