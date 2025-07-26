# ④ Apply OpenSpy Patches

In this tutorial, we’ll focus on getting your game working with OpenSpy.

OpenSpy is an open-source replacement for GameSpy, designed to provide full compatibility with GameSpy-supported games. The Reclamation community is the main BF2142 group using the OpenSpy master server.

<details>

<summary>What's a master server?</summary>

A master server manages your login credentials and soldier data, broadcasts available game servers to your server browser, and receives regular updates from game servers about player progress.

</details>

<details>

<summary>Why do we need OpenSpy patches?</summary>

After [GameSpy shutdown](https://en.wikipedia.org/wiki/GameSpy#Shutdown) in 2014, the original online services for BF2142 stopped working. OpenSpy patches redirect the game to use the OpenSpy master server instead, letting you log in and play online again.

</details>

<details>

<summary>Are there any other master servers besides OpenSpy?</summary>

Yes, there are a few, like NovGames, PlayBF2142, and MAGMA. However, OpenSpy — especially with the Reclamation community — offers the most reliable and active service.

</details>

<details>

<summary>How's the Reclamation community? Is it active?</summary>

<figure><img src="../.gitbook/assets/reclamation_orig.png" alt="" width="563"><figcaption></figcaption></figure>

The Reclamation servers are quite active! You’ll usually find 10+ players on weekdays and 30+ on weekends. There are both EU and US servers available, and the community is English-speaking and connected through the [Reclamation Discord](https://discord.com/invite/MEwBW9U).

You can enjoy various game modes, including Conquest, Conquest Coop, and Titan.

**To join:**

* Make sure you’ve installed OpenSpy patches using BF2142 Hub.
* Also, install the Reclamation Map Pack (or any maps currently running on the server) through BF2142 Hub.

Jump in and you’ll find a welcoming and active community!

</details>

<details>

<summary>Do we have all the unlocks with OpenSpy?</summary>

Yes, connecting to OpenSpy is a real privilege — it gives you access to all unlocks in Single-Player and Multi-Player LAN modes. This makes it perfect for grinding against bots in a Conquest Coop game.

If you want to unlock everything in BFHQ, just join a Reclamation (ranked) server and play a round. That said, this step isn’t required — you’ll still have access to all unlocks in SP/LAN even if you never play on a ranked server.

</details>

## Procedures

{% hint style="warning" %}
Before patching your game, it’s a good idea to make backup copies of your `BF2142.exe` and `RendDX9.dll` files from your game folder. \[Why?[^1]]
{% endhint %}

1. Right-click <mark style="color:blue;">BF2142 Hub</mark> shortcut on your desktop and select <mark style="color:blue;">Properties</mark>.&#x20;
2. Go to the <mark style="color:blue;">Compatibility</mark> tab, check <mark style="color:blue;">Run this program as an administrator</mark>, then click <mark style="color:blue;">Apply</mark> and <mark style="color:blue;">OK</mark>. \[Why?[^2]]
3. Double-click the shortcut to launch BF2142 Hub.
4. When prompted by [<mark style="color:blue;">User Account Contro</mark>](#user-content-fn-3)[^3]<mark style="color:blue;">l</mark>, click <mark style="color:blue;">Yes</mark> to allow the installer to make changes on your device.
5. Go to the <mark style="color:blue;">Help</mark> tab (the question mark icon) and check if the <mark style="color:blue;">GamePath</mark> is set to the correct folder. If it isn't, click the gear icon to locate your game folder.
6. From the <mark style="color:blue;">Redirects\*</mark> drop-down menu, select <mark style="color:blue;">OpenSpy</mark> and click <mark style="color:blue;">Install</mark>.
7. When asked <mark style="color:blue;">Are you sure you want to patch the game?</mark>, click <mark style="color:blue;">Yes</mark> .
8. Once you see <mark style="color:blue;">Patch completed, Enjoy!</mark>, click <mark style="color:blue;">Confirm</mark>.
9. After patching, make sure the checkmarks for <mark style="color:blue;">Patch 1.51</mark>, <mark style="color:blue;">BF2142.exe</mark>, <mark style="color:blue;">RendDX9.d</mark>, <mark style="color:blue;">RendDX9ori.dll</mark> are all <mark style="color:green;">green</mark>. If any aren't, repeat from step 6.

If you run into issues like crashes, the game not starting, or graphics glitches, the troubleshooting and diagnosis tools on the <mark style="color:blue;">Help</mark> tab are very useful.

## Reclamation Map Pack

The Reclamation Community runs 2 multiplayer servers, both featuring their own modified versions of maps. To join their public servers, you’ll need to install their map pack or the specific map currently in rotation. Click [here](https://www.battlefield2142.co/maps/v3.html) for more details about the maps in the pack.

{% hint style="info" %}
The steps below are optional and only needed if you want to play on Reclamation’s multiplayer servers.
{% endhint %}

{% hint style="info" %}
The downloaded maps are installed to the `\mods\bf2142\Levels` folder.
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

[^1]: This way, you’ll have a safety net in case anything goes wrong during the patching process.

[^2]: Running as administrator helps prevent permission issues during patching.

[^3]: i.e., <mark style="color:blue;">Do you want to allow this app from an unknown publisher to make changes to your device?</mark>
