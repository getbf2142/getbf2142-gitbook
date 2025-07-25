---
description: This tutorial will guide you through the steps to apply the patches.
---

# ⑤ Apply OpenSpy Patches

OpenSpy is an open-source GameSpy clone which aims to provide 100% compatibility with GameSpy games. Reclamation is the core BF2142 community that utilises the OpenSpy master server.

Apart from Openspy - Reclamation, there are other master servers and communities as well. To name a few, we have NovGames, PlayBF2142 and MAGMA. OpenSpy - Reclamation, however, offers the most long-lasting and stable service with a large and active community for support. In this tutorial, we will focus on getting our game to work with OpenSpy.

A master server is a server that holds the database of your login credentials and soldier data. It broadcasts[^1] game servers to the server browser, while in return a game server regularly reports the player's in-game progress to the master server.

Installing OpenSpy patches to the game forces the game to connect through OpenSpy instead of the dead GameSpy. This allows the game to work again, especially for the login and online part, after [GameSpy shutdown](https://en.wikipedia.org/wiki/GameSpy#Shutdown) in June 2014.

## About OpenSpy - Reclamation

{% tabs %}
{% tab title="OpenSpy - Reclamation" %}
![OpenSpy Server List](../.gitbook/assets/reclamation_orig.png)

* Gadgets: All gadget items are unlocked
* Playerbase: 10+ players on weekdays, 30+ at weekends
* Servers: Reclamation EU, Reclamation US
* Community: [Reclamation Discord](https://discord.com/invite/MEwBW9U), English-speaking
* Gamemodes: Conquest, Conquest Coop, Titan
* ​Requirements: Install OpenSpy patches via BF2142 Hub
* Requirements: Install Reclamation Map Pack or maps that the server is currently running upon via BF2142 Hub

You do not have to play on ranked servers to rank up because you are given all the unlocks right from the start. This provides a very ideal setting for grinding bots on a Project Remaster's Conquest Coop (Solo/LAN/Multi) game.
{% endtab %}
{% endtabs %}

## Procedures

{% hint style="warning" %}
​Before you patch your game, it’s highly recommended to make a backup copy of your `BF2142.exe` and `RendDX9.dll` files from your game folder.
{% endhint %}

1. Right-click the <mark style="color:blue;">BF2142 Hub</mark> shortcut on your desktop and select <mark style="color:blue;">Properties</mark>.&#x20;
2. Go to the <mark style="color:blue;">Compatibility</mark> tab, checl <mark style="color:blue;">Run this program as an administrator</mark>, then click <mark style="color:blue;">Apply</mark> and <mark style="color:blue;">OK</mark>. \[Why?[^2]]
3. Double-click the shortcut to launch the app.
4. &#x20;When prompted with <mark style="color:blue;">Do you want to allow this app from an unknown publisher to make changes to your device?</mark>, click <mark style="color:blue;">Yes</mark>
5. Go to the <mark style="color:blue;">Help</mark> tab (the question mark icon) and check if the <mark style="color:blue;">GamePath</mark> is set to the correct folder. If it isn't, click the gear icon to locate your game folder.
6. From the <mark style="color:blue;">Redirects\*</mark> drop-down menu, select <mark style="color:blue;">OpenSpy</mark> and click <mark style="color:blue;">Install</mark>.
7. When asked <mark style="color:blue;">Are you sure you want to patch the game?</mark>, click <mark style="color:blue;">Yes</mark> .
8. Once you see <mark style="color:blue;">Patch completed, Enjoy!</mark>, click <mark style="color:blue;">Confirm</mark>.
9. After patching, make sure the checkmarks for <mark style="color:blue;">Patch 1.51</mark>, <mark style="color:blue;">BF2142.exe</mark>, <mark style="color:blue;">RendDX9.d</mark>, <mark style="color:blue;">RendDX9ori.dll</mark> are all <mark style="color:green;">green</mark>. If any aren't, repeat from step 6.

## Reclamation Map Pack

The Reclamation Community runs two multiplayer servers, both featuring their own modified versions of maps. To join their public servers, you’ll need to install their map pack or the specific map currently in rotation. Click [here](https://www.battlefield2142.co/maps/v3.html) for more details about the maps in the pack.

{% hint style="info" %}
The steps below are optional and only needed if you want to play on Reclamation’s multiplayer servers.
{% endhint %}

#### **Installing the complete pack**

1. In the <mark style="color:blue;">Download</mark> tab, double-click on <mark style="color:blue;">BF2142 MapPack v1.0</mark>. This will open your browser to the download link of the pack. Download <mark style="color:blue;">2142\_MapPack\_v1.zip</mark> ([bf2142.ddns.net](http://bf2142.ddns.net/), 3.9GB).
2. Once the download finishes, click the <mark style="color:blue;">MapPack Installer \*</mark> button and select the .zip file you just downloaded.
3. A command-line window will appear and close automatically when the installation is doe.
4. If everything looks good, you can close the app.

#### **Installing individual maps**

You can also download maps individually. If you’d like to do this, just follow the instructions below.

1. In the <mark style="color:blue;">Download</mark> tab, click on <mark style="color:blue;">Individual Maps</mark>.&#x20;
2. Choose the maps you want to download from the <mark style="color:blue;">Available Maps</mark> box and click <mark style="color:blue;">>></mark> to download them.
3. To uninstall a map, select it from the <mark style="color:blue;">Installed Maps</mark> box and click <mark style="color:blue;"><<</mark>.

{% hint style="info" %}
The downloaded maps are installed to the `\mods\bf2142\Levels` folder. \[Why?[^3]]
{% endhint %}

[^1]: A master server makes a game server visible on the client's server browser.

[^2]: This is something UAC-related: You’ll need to run Bf2142 Hub as an Administrator to apply patches, since it has to modify files in your game folder.

[^3]: Reclamation servers are unmodded servers, but are run on a set of modified maps.&#x20;
