---
description: This tutorial will guide you through the steps to quickly host a server.
---

# ⑩ Host Server

{% hint style="warning" %}
* Port forwarding is only required for WAN servers.
* Only servers are required to do port forwarding.​
* A server becomes a modded server if the server hoster launched the game with a mod.
{% endhint %}

In this tutorial, you will learn how to host a simple server in-game. However, there are always some bad things behind something that is quick and easy to set up:

* There are fewer game settings available for you to configure in-game[^1].
* The server hoster has to be [playing on the server](#user-content-fn-2)[^2] as well.

​That's why for a production server, you will need to host it with a [dedicated server client](../dedicated-server/download-and-install-server-client.md). But this quick setup method should already be sufficient for most of the use cases.

<details>

<summary>Port forwarding is not working for me!?</summary>

If port forwarding is done after the server is running, you need to restart the server.

If you have properly configured port forwarding but still no one can connect to it, then double-check whether your ISP uses CGNAT.

If that is the case, port forwarding will not take effect. Contact your ISP for an opt-out whenever possible.

An alternative is to host a LAN server over a VLAN[^3] o that your friends can join!

</details>

## Hosting a LAN Server

A local server is a game server that appears on the local server browser and is accessible within a LAN network.

This option is most suitable for hosting a game party for your family within your home network, or with your friends across the internet through the use of VLAN[^3].

1. Log in to the game.
2. Click <mark style="color:blue;">MULTIPLAY</mark>.
3. Click <mark style="color:blue;">LOCAL</mark>.
4. In the <mark style="color:blue;">CREATE</mark> tab, configure the server settings and click <mark style="color:blue;">START SERVER</mark>.
5. You will be able to see your server's local IP address on the loading screen while the server is launching (i.e., on loading / briefing screen).

## Hosting a Private WAN Server

A private WAN server is a game server that does not appear on the online server browser but is still accessible over the internet if you know its public IP address.&#x20;

This option is most suitable for hosting a game party with your friends without the need of using any virtual LAN solutions.

1. Close the game if you still have the game running.
2. Forward[^4] the following ports to your server's local IP address in your home router's control panel:\
   `29900 - 29900 UDP or Both`\
   `17567 - 17567 Both​`
3. Go to [https://www.whatismyip.com/](https://www.whatismyip.com/) to view your public IP address. Message your friends the IP address.
4. Log in to the game.
5. Click <mark style="color:blue;">MULTIPLAY</mark>.
6. Click <mark style="color:blue;">LOCAL</mark>.
7. In the <mark style="color:blue;">CREATE</mark> tab, configure the server settings and click <mark style="color:blue;">START SERVER</mark>.

​LAN players can still join your server using your local IP address (such as your family members) while WAN players (such as your friends in another area) can join your server using your public IP address. This only applies when you have properly set up port forwarding.​​

## Hosting a Public WAN Server

​A public server is a game server that appears on the online server browser and is accessible through the Internet.&#x20;

Since the server is visible on the browser, you will be [allowing random people](#user-content-fn-5)[^5] on the Internet to join your game.

1. Close the game if you still have the game running.
2. Forward[^4] the following ports to your server's local IP address in your wireless router control panel:\
   `29900 - 29900 UDP or Both`\
   `17567 - 17567 Both​`
3. Use file explorer to navigate to <mark style="color:blue;">C:\Users\\\<YOU>\Documents\Battlefield 2142\Profiles</mark>.
4. Open <mark style="color:blue;">Global.con</mark> using a text editor.&#x20;
5. Look for the line that begins with <mark style="color:blue;">GlobalSettings.setDefaultUser</mark>. \
   If its value is <mark style="color:blue;">0001</mark>, open the folder <mark style="color:blue;">0001</mark>.
6. In the folder, open <mark style="color:blue;">ServerSettings.con</mark> using a text editor.
7. Look for the line <mark style="color:blue;">GameServerSettings.setInternet 0</mark>. [Change <mark style="color:blue;">0</mark> to <mark style="color:blue;">1</mark>](#user-content-fn-6)[^6]. Save the file.
8. Go to [https://www.whatismyip.com/](https://www.whatismyip.com/) to view your public IP address. Message your friends the IP address.
9. Log in to the game.
10. Click <mark style="color:blue;">MULTIPLAY</mark>.
11. Click <mark style="color:blue;">LOCAL</mark>.
12. In the <mark style="color:blue;">CREATE</mark> tab, configure the server settings and click <mark style="color:blue;">START SERVER</mark>.
13. Now your server should show up in the online server browser.

To check whether your setup is correct, you may press the <mark style="color:blue;">Esc</mark> button in-game and go to the server browser. Your server should show up there.&#x20;

If port forwarding is not configured properly on the server side, you will still see the server on the list, but no one else will be able to join it.

​LAN players can still join your server using your local IP address while WAN players can join your server using your public IP address.

## Configuring more server settings

1. Close the game if you still have the game running.
2. Use file explorer to navigate to <mark style="color:blue;">C:\Users\\\<YOU>\Documents\Battlefield 2142\Profiles</mark>.
3. Open <mark style="color:blue;">Global.con</mark> using a text editor.&#x20;
4. Look for the line that begins with <mark style="color:blue;">GlobalSettings.setDefaultUser</mark>. \
   If its value is <mark style="color:blue;">0001</mark>, open the folder <mark style="color:blue;">0001</mark>.
5. In the folder, open <mark style="color:blue;">ServerSettings.con</mark> using a text editor.
6. Modify the values according to your needs. \[How?[^7]]
7. Safe the file to apply the changes.
8. Use file explorer to navigate to <mark style="color:blue;">\<GAME\_FOLDER>\mods\\<</mark>[<mark style="color:blue;">MOD</mark>](#user-content-fn-8)[^8]<mark style="color:blue;">></mark>.
9. Open <mark style="color:blue;">GameLogicInit.con</mark> using a text editor.
10. Append the params and flags that you need to the end of the file. \[How?[^9]]\
    Some of the frequently used configurations are listed below.
11. Save the file to apply the changes.

<details>

<summary>Useful flags to be appended to GameLogicInit.con</summary>

sv.allowNATNegotiation 0\
sv.welcomeMessage "Welcome!""\
sv.numPlayersNeededToStart 1\
sv.useGlobalRank 1\
sv.useGlobalUnlocks 1

sv.spawnTime 10\
sv.manDownTime 10\
sv.botSkill 0.2

Refer to [https://pingperfect.com/index.php/knowledgebase/585/Battlefield-2142--Server-Configuration.html](https://pingperfect.com/index.php/knowledgebase/585/Battlefield-2142--Server-Configuration.html) or <mark style="color:blue;">\mods\\\<MOD>\Settings\ServerSettings.csv</mark> for more details.

</details>

[^1]: However, you can configure more settings using a text editor.

[^2]: The server hoster plays while hosting. If he or she closes the game, the server will be closed as well.

[^3]: i.e., virtual LAN, e.g., [Hamachi](https://vpn.net/), [PartyLAN](https://github.com/gyf304/partylan)

[^4]: i.e., Port Forwarding / NAT Virtual Server)

[^5]: If you don't want to be disturbed, set a password for your server.

[^6]: This tells OpenSpy to show your server on the server browser. `1` for Internet, `0` for LAN.

[^7]: Refer to [https://pingperfect.com/index.php/knowledgebase/585/Battlefield-2142--Server-Configuration.html](https://pingperfect.com/index.php/knowledgebase/585/Battlefield-2142--Server-Configuration.html) or <mark style="color:blue;">\mods\bf2142\Settings\ServerSettings.csv</mark> as a reference.

[^8]: Choose the mod folder that you want to host the server with. "bf2142" is the vanilla base game.

[^9]: Refer to [https://pingperfect.com/index.php/knowledgebase/585/Battlefield-2142--Server-Configuration.html](https://pingperfect.com/index.php/knowledgebase/585/Battlefield-2142--Server-Configuration.html) or <mark style="color:blue;">\mods\\\<MOD>\Settings\ServerSettings.csv</mark> as a reference. Copy the line that you need to <mark style="color:blue;">GameLogicInit.con</mark>.
