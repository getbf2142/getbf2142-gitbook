# ⍟ Play Multiplayer

In this tutorial, we'll walk you through the steps to join a server.

A few things to note:

* If you’re joining Reclamation servers or any pure vanilla servers, make sure you’re using a vanilla BF2142 setup — don’t use any addons like Blood Patch or HUD-Fix in `mods\bf2142`.
* You can only join servers that match the mod you’re running. You can’t join an unmodded server with a mod enabled, or vice versa. To join a modded server, you’ll need to have the exact same mod installed as the server.
* You need to install the required [custom maps](apply-openspy-patches.md#installing-the-reclamation-map-pack) to play on Reclamation servers.

## Joining a LAN Server

A local server is a game server that shows up in your local server browser and can be accessed by anyone on your LAN network.

1. Click <mark style="color:blue;">MULTIPLAY</mark>.
2. Click <mark style="color:blue;">LOCAL</mark>.
3. In the <mark style="color:blue;">JOIN</mark> tab, click <mark style="color:blue;">UPDATE LIST</mark> until the LAN server appears.
4. ​Once it shows up, double-click the server to join.

<details>

<summary>Solution to "Server Not Found" in Local Server Browser</summary>

First, make sure you’re connected to the same LAN network as the server host. If you still can’t find the server in the local server browser, even when it’s running, try this:

1. Click <mark style="color:blue;">ONLINE</mark> in the game.
2. Go to the <mark style="color:blue;">ADVANCED</mark> tab and click <mark style="color:blue;">CONNECT TO IP</mark>.
3. Enter the server’s local IP address (usually something like `192.168.x.x`) and click <mark style="color:blue;">OK</mark>. The server host can find their local IP on the loading screen after launching the server.

#### **Why does this happen?**

Often, it’s because your PC has multiple network adapters — especially if you use programs like Hamachi, VirtualBox, or VMWare.

#### **The simplest fix**

Disable all other network adapters except the one you’re using for your current network.

1. Go to <mark style="color:blue;">Network and Sharing Center</mark> in your <mark style="color:blue;">Control Panel</mark>.

2) Click <mark style="color:blue;">Change adapter settings</mark>.
3) Right-click any adapter you want to disable and select <mark style="color:blue;">Disable</mark>.

Do this first on the server computer, then on any computers trying to connect. This should help your LAN server show up in the local server browser!

Reference: [https://superuser.com/questions/610733/networking-games-cant-see-join-anyone-elses-lan-servers-unless-i-host](https://superuser.com/questions/610733/networking-games-cant-see-join-anyone-elses-lan-servers-unless-i-host)

</details>

## Joining a Public WAN Server

A public server is a game server that shows up in the online server browser and can be accessed over the Internet.

1. Click <mark style="color:blue;">MULTIPLAY</mark>.
2. Click <mark style="color:blue;">ONLINE</mark>.
3. In the <mark style="color:blue;">ADVANCED</mark> tab, uncheck all the filter options and click <mark style="color:blue;">UPDATE LIST</mark>.
4. You should now see a list of public servers. Double-click one to jon and play.

{% columns %}
{% column width="41.66666666666667%" %}
<figure><img src="../.gitbook/assets/pic7_orig.png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}

{% column %}
The green icon next to the 2142 icon shows if a server is modded or not — green means it’s unmodded, while red means it’s running a mod. To join servers with the green icon, always launch the game without any mods enabled.
{% endcolumn %}
{% endcolumns %}

## Joining a Private WAN Server

A private WAN server is a game server that doesn’t show up in the online server browser, but you can still access it over the internet if you have its public IP address.

1. Click <mark style="color:blue;">MULTIPLAY</mark>.
2. Click <mark style="color:blue;">ONLINE</mark>.
3. In the <mark style="color:blue;">ADVANCED</mark> tab, click <mark style="color:blue;">CONNECT TO IP</mark>.
4. Enter the server's public IP address and adjust the [port number](#user-content-fn-1)[^1] if needed.
5. Click <mark style="color:blue;">OK</mark> to connect.

[^1]: 17567 is the default port.
