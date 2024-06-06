---
description: This tutorial will guide you through the steps to host a server.
---

# ⑩ Host a Server

{% hint style="warning" %}
* Port forwarding is only required for WAN servers.
* Only servers are required to do port forwarding.​
* A server becomes a modded server if the server hoster launched the game with a mod.
{% endhint %}

In this tutorial, you will learn how to host a simple server in-game. However, there are always some bad things behind something that is quick and easy to set up:

* There are fewer[^1] game settings available for you to configure.
* The server hoster has to be [playing on the server](#user-content-fn-2)[^2] as well.

​That's why for a production server, you will need to host it with a [dedicated server client](../dedicated-server/download-and-install-the-server-client.md). But this quick setup method should already be sufficient for most of the use cases.

<details>

<summary>Port forwarding is not working for me!?</summary>

If port forwarding is done after the server is running, you need to restart the server.

If you have properly configured port forwarding but still no one can connect to it, then double-check whether your ISP uses CGNAT.

If that is the case, port forwarding will not take effect. Contact your ISP for an opt-out whenever possible.

An alternative is to host a LAN server over a VLAN[^3] o that your friends can join!

</details>

## Hosting a LAN Server

A local server is a game server that appears on the local server browser and is accessible within a LAN network.

This option is most suitable for hosting a game party for your family within your home network, or with your friends across the internet through the use of VLAN[^4].

1. Log in to the game.
2. Click <mark style="color:blue;">MULTIPLAY</mark>.
3. Click <mark style="color:blue;">LOCAL</mark>.
4. In the <mark style="color:blue;">CREATE</mark> tab, configure the server settings and click <mark style="color:blue;">START SERVER</mark>.
5. You will be able to see your server's local IP address on the loading screen while the server is launching (i.e., on loading / briefing screen).

## Hosting a Private WAN Server

A private WAN server is a game server that does not appear on the online server browser but is still accessible over the internet if you know its public IP address.&#x20;

This option is most suitable for hosting a game party with your friends without the need of using any virtual LAN solutions.

1. Forward[^5] the following ports to your server's local IP address in your home router's control panel:\
   `29900 - 29900 UDP or Both`\
   `17567 - 17567 Both​`
2. Go to [https://www.whatismyip.com/](https://www.whatismyip.com/) to view your public IP address. Tell the IP address to your friends.
3. Log in to the game.
4. Click <mark style="color:blue;">MULTIPLAY</mark>.
5. Click <mark style="color:blue;">LOCAL</mark>.
6. In the <mark style="color:blue;">CREATE</mark> tab, configure the server settings and click <mark style="color:blue;">START SERVER</mark>.

​LAN players can still join your server using your local IP address (such as your family members) while WAN players (such as your friends in another area) can join your server using your public IP address. This only applies when you have properly set up port forwarding.​​

## Hosting a Public WAN Server

​A public server is a game server that appears on the online server browser and is accessible through the Internet.&#x20;

Since the server is visible on the browser, you will be [allowing random people](#user-content-fn-6)[^6] on the Internet to join your game.

1. Forward[^7] the following ports to your server's local IP address in your wireless router control panel:\
   `29900 - 29900 UDP or Both`\
   `17567 - 17567 Both​`
2. Use file explorer to navigate to <mark style="color:blue;">C:\Users\xxxxx\Documents\Battlefield 2142\Profiles</mark>.
3. Open <mark style="color:blue;">Global.con</mark> using a text editor.&#x20;
4. Look for the line that begins with <mark style="color:blue;">GlobalSettings.setDefaultUser</mark>. \
   If its value is <mark style="color:blue;">0001</mark>, open the folder <mark style="color:blue;">0001</mark>.
5. In the folder, open <mark style="color:blue;">ServerSettings.con</mark> using a text editor.
6. Look for the line <mark style="color:blue;">GameServerSettings.setInternet 0</mark>. [Change <mark style="color:blue;">0</mark> to <mark style="color:blue;">1</mark>](#user-content-fn-8)[^8]. Save the file.
7. Go to [https://www.whatismyip.com/](https://www.whatismyip.com/) to view your public IP address. Tell the IP address to your friends.
8. Log in to the game.
9. Click <mark style="color:blue;">MULTIPLAY</mark>.
10. Click <mark style="color:blue;">LOCAL</mark>.
11. In the <mark style="color:blue;">CREATE</mark> tab, configure the server settings and click <mark style="color:blue;">START SERVER</mark>.
12. Now your server should show up in the online server browser.

To check whether your setup is correct, you may press the <mark style="color:blue;">Esc</mark> button in-game and go to the server browser. Your server should show up there.&#x20;

If port forwarding is not configured properly on the server side, you will still see the server on the list, but no one else will be able to join it.

​LAN players can still join your server using your local IP address while WAN players can join your server using your public IP address.

[^1]: Relative to a dedicated server.

[^2]: The server hoster plays while hosting. If he or she closes the game, the server will be closed as well.

[^3]: i.e., virtual LAN, e.g., [Hamachi](https://vpn.net/), [PartyLAN](https://github.com/gyf304/partylan)

[^4]: i.e., virtual LAN, e.g., [Hamachi](https://vpn.net/), [PartyLAN](https://github.com/gyf304/partylan)

[^5]: i.e., Port Forwarding / NAT Virtual Server)

[^6]: If you don't want to be disturbed, set a password for your server.

[^7]: i.e., Port Forwarding / NAT Virtual Server)

[^8]: This tells OpenSpy to show your server on the server browser. `1` for Internet, `0` for LAN.
