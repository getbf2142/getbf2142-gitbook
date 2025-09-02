---
description: 'Jump in: Your guide to joining a server.'
icon: people-pants-simple
---

# Play Multiplayer

In this tutorial, we'll walk you through the steps to join a server. If you hit any snags or have questions, hop into our [Discord](https://discord.gg/7SBMKRy6q9) — we’re always happy to help!

{% embed url="https://discord.gg/7SBMKRy6q9" %}

<details>

<summary>Important Notes</summary>

* For Reclamation or any vanilla servers, use a clean vanilla BF2142 setup — no addons or file tweaks in `\mods\bf2142`.&#x20;
* To join Reclamation servers, you’ll also need to [install their map pack](install-map-pack.md).

- For modded servers, install the exact same mod and files the server is running.

</details>

### Joining a LAN Server

A local server is a game server that shows up in your local server browser and can be accessed by anyone on your LAN network.

<details>

<summary>Server is not showing up in the local server browser</summary>

First, make sure you’re connected to the same LAN network as the server host. If you still can’t find the server in the local server browser, even when it’s running, try this:

1. Click <mark style="color:blue;">ONLINE</mark> in the game.
2. Go to the <mark style="color:blue;">ADVANCED</mark> tab and click <mark style="color:blue;">CONNECT TO IP</mark>.
3. Enter the server’s local IP address (usually something like `192.168.x.x`) and click <mark style="color:blue;">OK</mark>. The server host can find their local IP on the loading screen after launching the server **\[**[**?**](#user-content-fn-1)[^1]**]**.

#### **Why this is happening ?**

If your PC has multiple network adapters (e.g., from Hamachi, VirtualBox, VMware, ExpressVPN), the game may pick the wrong one for multiplayer.

#### How to fix this ?

Disable adapters you’re not using and keep only the one(s) needed. **\[**[**?**](#user-content-fn-2)[^2]**]**

1. Go to <mark style="color:blue;">Control Panel</mark> → <mark style="color:blue;">Network and Sharing Center</mark> → <mark style="color:blue;">Change adapter settings</mark>.

2) Right-click the adapter you want to disable → <mark style="color:blue;">Disable</mark>.

If you can’t disable it via UI, use <mark style="color:blue;">PowerShell</mark> (Run as Administrator):

* Disable: `Disable-NetAdapter -Name "Adapter Name"`
* Enable: `Enable-NetAdapter -Name "Adapter Name"`

Do this first on the server computer, then on any computers trying to connect. This should help your LAN server show up in the local server browser!

Reference: [https://superuser.com/questions/610733/networking-games-cant-see-join-anyone-elses-lan-servers-unless-i-host](https://superuser.com/questions/610733/networking-games-cant-see-join-anyone-elses-lan-servers-unless-i-host)

</details>

{% stepper %}
{% step %}
Select <mark style="color:blue;">MULTIPLAY</mark> → <mark style="color:blue;">LOCAL</mark>.
{% endstep %}

{% step %}
In the <mark style="color:blue;">JOIN</mark> tab, click <mark style="color:blue;">UPDATE LIST</mark> until the LAN server appears.
{% endstep %}

{% step %}
​Once it shows up, double-click the server to join.
{% endstep %}
{% endstepper %}

### Joining a Public WAN Server

A public server is a game server that shows up in the online server browser and can be accessed over the Internet.

{% stepper %}
{% step %}
Click <mark style="color:blue;">MULTIPLAY</mark> → <mark style="color:blue;">ONLINE</mark>.
{% endstep %}

{% step %}
In the <mark style="color:blue;">ADVANCED</mark> tab, uncheck all the filter options and click <mark style="color:blue;">UPDATE LIST</mark> **\[**[**?**](#user-content-fn-3)[^3]**]**.

<div align="left"><figure><img src="../.gitbook/assets/pic7_orig.png" alt="" width="375"><figcaption></figcaption></figure></div>
{% endstep %}

{% step %}
You should now see a list of public servers. Double-click one to join and play.
{% endstep %}
{% endstepper %}

### Joining a Private WAN Server

A private WAN server is a game server that doesn’t show up in the online server browser, but you can still access it over the internet if you have its public IP address.

{% stepper %}
{% step %}
Click <mark style="color:blue;">MULTIPLAY</mark> → <mark style="color:blue;">ONLINE</mark>.
{% endstep %}

{% step %}
In the <mark style="color:blue;">ADVANCED</mark> tab, click <mark style="color:blue;">CONNECT TO IP</mark>.
{% endstep %}

{% step %}
Enter the server's public IP address and adjust the [port number](#user-content-fn-4)[^4] if needed.
{% endstep %}

{% step %}
Click <mark style="color:blue;">OK</mark> to connect.
{% endstep %}
{% endstepper %}

[^1]: If you’re using a VLAN or VPN, make sure to enter your VLAN or VPN IP address — not your regular local IP (from router) that connects you to the internet.

[^2]: If you’re connecting over a VLAN or VPN, keep both your main internet connection (Wi‑Fi or Ethernet) and your VLAN/VPN adapters enabled.

[^3]: If you don't, you'll see no multiplayer servers showing up in the list.

[^4]: 17567 is the default port.
