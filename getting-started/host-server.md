---
description: 'Be the host: How to set up your own game server ...'
icon: server
---

# Host a server

In this tutorial, you’ll learn how to host a simple server directly from the game. If you hit any snags or have questions, hop into our [Discord](https://discord.gg/7SBMKRy6q9) — we’re always happy to help!

While this method is quick and easy, there are a few limitations:

* You’ll have fewer game settings to customize. **\[**[**?**](#user-content-fn-1)[^1]**]**
* The person hosting the server must also be playing on it.

For a full-featured, production server, you’d want to use a [dedicated server](../advanced/dedicated-server/install-server.md). However, this quick setup is usually enough for most situations.

{% embed url="https://discord.gg/7SBMKRy6q9" %}

<details>

<summary>Important Notes</summary>

* You only need port forwarding if you want your server accessible over the internet (WAN), and only the host needs to set it up. **\[**[**?**](#user-content-fn-2)[^2]**]**
* Disable unused network adapters; keep only the one(s) you’ll host on (details below).

- When prompted by Windows Firewall, allow the game (or BF2142Unlocker) on both Private and Public networks to avoid connection issues.
- For WAN servers: LAN players at home join via your local IP; friends elsewhere join via your public IP — assuming port forwarding is configured correctly.
- If you launch the game with a mod, any server you host will also be modded.

</details>

<details>

<summary>LAN Over Internet</summary>

If port forwarding isn’t feasible but you still want to play online with friends, a VLAN is your best option.

Apps like [Hamachi](https://vpn.net/), [GameRanger](https://www.gameranger.com/), or [Radamin VPN](https://www.radmin-vpn.com/) create a secure virtual network that simulates a LAN. Typically, you and your friends just:

* Install the app and create accounts
* Create or join a room to connect to the same LAN
* Use the IP address assigned by the app to host or join a server

For setup details, refer to the app’s documentation or resources.

</details>

<details>

<summary>Disabling Network Adapters</summary>

If your PC has multiple network adapters (e.g., from Hamachi, VirtualBox, VMware, ExpressVPN), the game may pick the wrong one when hosting.

To fix this, disable adapters you’re not using and keep only the one(s) needed for hosting. **\[**[**?**](#user-content-fn-3)[^3]**]**

1. Go to <mark style="color:blue;">Control Panel</mark> → <mark style="color:blue;">Network and Sharing Center</mark> → <mark style="color:blue;">Change adapter settings</mark>.

2) Right-click the adapter you want to disable → <mark style="color:blue;">Disable</mark>.

If you can’t disable it via UI, use <mark style="color:blue;">PowerShell</mark> (Run as Administrator):

* Disable: `Disable-NetAdapter -Name "Adapter Name"`
* Enable: `Enable-NetAdapter -Name "Adapter Name"`

Reference: [https://superuser.com/questions/610733/networking-games-cant-see-join-anyone-elses-lan-servers-unless-i-host](https://superuser.com/questions/610733/networking-games-cant-see-join-anyone-elses-lan-servers-unless-i-host)

</details>

<details>

<summary>Port Forwarding Troubleshoots</summary>

* If you configure port forwarding after the server is running, restart the server for changes to take effect.
* If port forwarding is set up correctly but others still can’t connect, your ISP may be using CGNAT (Carrier-Grade NAT), which blocks port forwarding. Contact your ISP to opt out.
* Alternatively, host a LAN server over a VLAN so friends can still join and play together.

</details>

### Hosting a LAN Server

A local server is a game server that shows up in your local server browser and can be accessed by anyone on your LAN network. This option is perfect for hosting a game night with family at home, or for playing with friends over the internet using a virtual LAN tool.

{% stepper %}
{% step %}
Disable any unused network adapters (see the [expandable](host-server.md#disabling-network-adapters) above).
{% endstep %}

{% step %}
Select <mark style="color:blue;">MULTIPLAY</mark> → <mark style="color:blue;">LOCAL</mark>.
{% endstep %}

{% step %}
In the <mark style="color:blue;">CREATE</mark> tab, configure your server settings and click <mark style="color:blue;">START SERVER</mark>.

Check out the [Server Settings](../advanced/addons-tweaks/server-settings.md) guide for details on extra cutomization settings.
{% endstep %}

{% step %}
While the server is launching (on the loading or briefing screen), you’ll see your server’s local IP address displayed.
{% endstep %}
{% endstepper %}

### Hosting a Private WAN Server

A private WAN server is a game server that doesn’t show up in the online server browser, but friends can still join if they know your public IP address. This is a great option for hosting a game night with friends, without needing any virtual LAN tools.

{% stepper %}
{% step %}
Close the game if it’s running.
{% endstep %}

{% step %}
Disable any unused network adapters  (see the [expandable](host-server.md#disabling-network-adapters) above).
{% endstep %}

{% step %}
In your home router’s control panel, forward these ports to your device's local IPv4 address:

* `29900` (UDP or Both) - Login Service
* `17567` (Both) - Game Service

If you’re using BF2142Unlocker, make sure to also enable these two extra ports:

* `8085` (TCP or Both) – Unlock Service
* `18300` (TCP or Both) – Login Service

You may refer to [this guide](https://www.noip.com/support/knowledgebase/general-port-forwarding-guide) on how to perform port forwarding.
{% endstep %}

{% step %}
Visit [whatismyip.com](https://www.whatismyip.com/) to find your public IPv4 address, and share it with your friends.
{% endstep %}

{% step %}
Log in to the game.
{% endstep %}

{% step %}
Select <mark style="color:blue;">MULTIPLAY</mark> → <mark style="color:blue;">LOCAL</mark>.
{% endstep %}

{% step %}
In the <mark style="color:blue;">CREATE</mark> tab, configure your server settings and click <mark style="color:blue;">START SERVER</mark>.

Check out the [Server Settings](../advanced/addons-tweaks/server-settings.md) guide for details on extra cutomization settings.
{% endstep %}
{% endstepper %}

### Hosting a Public WAN Server

A public server is a game server that appears in the online server browser and can be accessed by anyone on the Internet. Since your server will be visible to everyone, random players can join your game.

{% stepper %}
{% step %}
Close the game if it’s running.
{% endstep %}

{% step %}
Disable any unused network adapters.

Refer to the expandable above for details on how to do so.
{% endstep %}

{% step %}
In your home router’s control panel, forward these ports to your device’s local IP address:

* `29900` (UDP or Both) - Login Service
* `17567` (Both) - Game Service

If you’re using BF2142Unlocker, make sure to also enable these two extra ports:

* `8085` (TCP or Both) – Unlock Service
* `18300` (TCP or Both) – Login Service

You may refer to [this guide](https://www.noip.com/support/knowledgebase/general-port-forwarding-guide) on how to perform port forwarding.
{% endstep %}

{% step %}
Open File Explorer and go to `C:\Users\<YOU>\Documents\Battlefield 2142\Profiles`.
{% endstep %}

{% step %}
Open `Global.con` with a text editor.
{% endstep %}

{% step %}
Find the line starting with `GlobalSettings.setDefaultUser`. If its value is `0001`, open the folder named `0001`.
{% endstep %}

{% step %}
Inside that folder, open `ServerSettings.con` with a text editor.
{% endstep %}

{% step %}
Find the line `GameServerSettings.setInternet 0` and change the `0` to `1`. Save the file.
{% endstep %}

{% step %}
Go to [whatismyip.com](https://www.whatismyip.com/) to find your public IPv4 address and share it with your friends.
{% endstep %}

{% step %}
Log in to the game.
{% endstep %}

{% step %}
Select <mark style="color:blue;">MULTIPLAY</mark> → <mark style="color:blue;">LOCAL</mark>.
{% endstep %}

{% step %}
In the <mark style="color:blue;">CREATE</mark> tab, configure your server settings and click <mark style="color:blue;">START SERVER</mark>.

Check out the [Server Settings](../advanced/addons-tweaks/server-settings.md) guide for details on extra cutomization settings.
{% endstep %}

{% step %}
Your server should now appear in the online server browser.

To check if everything is set up correctly, press `Esc` in-game and go to the server browser — your server should be listed there.

If port forwarding isn’t set up properly, your server will still show up in the list, but others won’t be able to join.
{% endstep %}
{% endstepper %}



[^1]: What I mean is that while you’re limited in how many settings you can tweak through the in-game GUI, you still have access to most server settings — you’ll just need to adjust them by editing the game’s files directly.

[^2]: If you’re hosting your server over a VLAN, there’s no need for port forwarding — it works just like a regular LAN setup.

[^3]: If you’re hosting over a VLAN or VPN, keep both your main internet connection (Wi‑Fi or Ethernet) and your VLAN/VPN adapters enabled.



    These virtual adapters usually have higher priority, so your server will often bind to them by default. Not sure which one is in use? Open <mark style="color:blue;">Command Prompt</mark> and run `ipconfig` — the adapters listed first typically have higher priority.
