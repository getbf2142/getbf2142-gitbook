---
description: This tutorial will guide you through the steps to join a server.
---

# ⑨ Play Multiplayer

{% hint style="warning" %}
* If you are joining an unmodded server, you must unselect all the [modded options](#user-content-fn-1)[^1] in the launcher before launching the game.
* You should join the server with a compatible[^2] mod. You cannot join an unmodded server with a mod or vice versa.
* You need to install [custom maps](apply-openspy-patches.md#installing-the-reclamation-map-pack) to play on Reclamation servers.
{% endhint %}

## Joining a LAN Server

A local server is a game server that appears on the local server browser and is accessible within a LAN network.

1. Log in to the game.
2. Click <mark style="color:blue;">MULTIPLAY</mark>.
3. Click <mark style="color:blue;">LOCAL</mark>.
4. In the <mark style="color:blue;">JOIN</mark> tab, click <mark style="color:blue;">UPDATE LIST</mark> until the LAN server appears on the list.
5. ​Double-click on the server to join the server.

<details>

<summary>Solution: Server Not Found in Local Server Browser</summary>

Ensure the following:

* You have connected to the same LAN network that the server is hosted on.&#x20;
* You cannot find the server in the local server browser even when the server is up.

If the above still does not rule out the cause for you, then follow these steps:

Click <mark style="color:blue;">ONLINE</mark>. In the <mark style="color:blue;">ADVANCED</mark> tab, click <mark style="color:blue;">CONNECT TO IP</mark>. Type in the server's local IP address. Click <mark style="color:blue;">OK</mark>.

A local IP address is usually in the pattern of 192.168.x.x. The server hoster will know his or her local IP address on the loading screen once the server is launched.

But have you ever wondered why? Like why your LAN server just doesn't show up in the local server browser, or why you just can't see your friend's server!

Most probably, it's because your PC is having multiple network adapters, especially when you have applications like Hamachi, VirtualBox or VMWare installed.

The simplest solution is to disable all other network adapters except the one for your current network.

1. Navigate to <mark style="color:blue;">Network and Sharing Center</mark> in your control panel.
2. Click <mark style="color:blue;">Change adapter settings</mark>.&#x20;
3. Right-click on the adapter that you want to disable and click <mark style="color:blue;">Disable</mark>.
4. Check this on your server computer first, followed by the computers connecting to the server.

Reference: [https://superuser.com/questions/610733/networking-games-cant-see-join-anyone-elses-lan-servers-unless-i-host](https://superuser.com/questions/610733/networking-games-cant-see-join-anyone-elses-lan-servers-unless-i-host)

</details>

## Joining a Public WAN Server

​A public server is a game server that appears on the online server browser and is accessible through the Internet.

1. Log in to the game.
2. Click <mark style="color:blue;">MULTIPLAY</mark>.
3. Click <mark style="color:blue;">ONLINE</mark>.
4. In the <mark style="color:blue;">ADVANCED</mark> tab, uncheck all the options in the filter and click <mark style="color:blue;">UPDATE LIST</mark>.
5. Now, you should see a list of public servers in the server browser. Double-click a server to play.

{% hint style="info" %}
​The green icon beside the 2142 icon tells you whether the server is modded or not. Green indicates unmodded while red indicates modded. Always launch the game without the mod to join any servers with the green icon.
{% endhint %}

![Configure the Server Browser](../.gitbook/assets/pic7\_orig.png)

## Joining a Private WAN Server

A private WAN server is a game server that does not appear on the online server browser but is still accessible over the internet if you know its public IP address.

1. Log in to the game.
2. Click <mark style="color:blue;">MULTIPLAY</mark>.
3. Click <mark style="color:blue;">ONLINE</mark>.
4. In the <mark style="color:blue;">ADVANCED</mark> tab, click <mark style="color:blue;">CONNECT TO IP</mark>.
5. Type in the server's public IP address and change the [port number](#user-content-fn-3)[^3] whenever necessary.
6. Click <mark style="color:blue;">OK</mark>.

[^1]: e.g., Remaster Mod, Blood Patch and HUD-Fix

[^2]: Compatible means you have the same mod content and mod version with the server.

[^3]: 17567 is the default port.
