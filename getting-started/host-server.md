---
description: How to host a server? How to configure server settings?
---

# ⍟ Host Server

In this tutorial, you’ll learn how to host a simple server directly from the game. While this method is quick and easy, there are a few limitations:

* You’ll have fewer game settings to customize. **\[**[**?**](#user-content-fn-1)[^1]**]**
* The person hosting the server must also be playing on it.

For a full-featured, production server, you’d want to use a [dedicated server client](../dedicated-server/download-and-install-server-client.md). However, this quick setup is usually enough for most situations.

<details>

<summary>A few things to keep in mind ...</summary>

* Port forwarding is only needed if you want your server to be accessible over the internet (WAN), and only the host needs to set it up.

- If you launch the game with a mod, your server will be considered modded.

* Whenever you see a Windows Firewall prompt, be sure to allow the game to communicate through both private and public networks to avoid any connection issues.

</details>

<details>

<summary>Port forwarding is not working for me !?</summary>

If you set up port forwarding after your server is already running, you’ll need to restart the server for the changes to take effect.

If you’ve configured port forwarding correctly but others still can’t connect, check if your ISP uses CGNAT (Carrier-Grade NAT). If so, port forwarding won’t work. In that case, contact your ISP to see if you can opt out.

Alternatively, you can host a LAN server over a VLAN[^2] so your friends can still join and play together!

</details>

## Hosting a LAN Server

A local server is a game server that shows up in your local server browser and can be accessed by anyone on your LAN network. This option is perfect for hosting a game night with family at home, or for playing with friends over the internet using a VLAN[^2].

{% stepper %}
{% step %}
Select <mark style="color:blue;">MULTIPLAY</mark> → <mark style="color:blue;">LOCAL</mark>.
{% endstep %}

{% step %}
In the <mark style="color:blue;">CREATE</mark> tab, configure your server settings and click <mark style="color:blue;">START SERVER</mark>.

Check out the [Server Settings Tweak](../addons-tweaks/server-settings-tweak.md) guide for details on extra cutomization settings.
{% endstep %}

{% step %}
While the server is launching (on the loading or briefing screen), you’ll see your server’s local IP address displayed.
{% endstep %}
{% endstepper %}

## Hosting a Private WAN Server

A private WAN server is a game server that doesn’t show up in the online server browser, but friends can still join if they know your public IP address. This is a great option for hosting a game night with friends, without needing any virtual LAN tools.

{% stepper %}
{% step %}
Close the game if it’s running.
{% endstep %}

{% step %}
In your home router’s control panel, forward these ports to your server’s local IP address:

* `29900` (UDP or Both)
* `17567` (Both)
{% endstep %}

{% step %}
Visit [whatismyip.com](https://www.whatismyip.com/) to find your public IP address, and share it with your friends.
{% endstep %}

{% step %}
Log in to the game.
{% endstep %}

{% step %}
Select <mark style="color:blue;">MULTIPLAY</mark> → <mark style="color:blue;">LOCAL</mark>.
{% endstep %}

{% step %}
In the <mark style="color:blue;">CREATE</mark> tab, configure your server settings and click <mark style="color:blue;">START SERVER</mark>.

Check out the [Server Settings Tweak](../addons-tweaks/server-settings-tweak.md) guide for details on extra cutomization settings.
{% endstep %}

{% step %}
LAN players (like family at home) can join using your local IP address, while friends from other locations (WAN players) can join using your public IP address — as long as port forwarding is set up correctly.
{% endstep %}
{% endstepper %}

## Hosting a Public WAN Server

A public server is a game server that appears in the online server browser and can be accessed by anyone on the Internet. Since your server will be visible to everyone, random players can join your game.

{% stepper %}
{% step %}
Close the game if it’s running.
{% endstep %}

{% step %}
In your home router’s control panel, forward these ports to your server’s local IP address:

* `29900` (UDP or Both)
* `17567` (Both)
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
Go to [whatismyip.com](https://www.whatismyip.com/) to find your public IP address and share it with your friends.
{% endstep %}

{% step %}
Log in to the game.
{% endstep %}

{% step %}
Select <mark style="color:blue;">MULTIPLAY</mark> → <mark style="color:blue;">LOCAL</mark>.
{% endstep %}

{% step %}
In the <mark style="color:blue;">CREATE</mark> tab, configure your server settings and click <mark style="color:blue;">START SERVER</mark>.

Check out the [Server Settings Tweak](../addons-tweaks/server-settings-tweak.md) guide for details on extra cutomization settings.
{% endstep %}

{% step %}
Your server should now appear in the online server browser. To check if everything is set up correctly, press <mark style="color:blue;">Esc</mark> in-game and go to the server browser — your server should be listed there.

If port forwarding isn’t set up properly, your server will still show up in the list, but others won’t be able to join.
{% endstep %}
{% endstepper %}



[^1]: What I mean is that while you’re limited in how many settings you can tweak through the in-game GUI, you still have access to most server settings — you’ll just need to adjust them by editing the game’s files directly.

[^2]: i.e., virtual LAN, e.g., [Hamachi](https://vpn.net/), [PartyLAN](https://github.com/gyf304/partylan)
