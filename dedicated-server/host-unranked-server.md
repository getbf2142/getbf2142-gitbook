---
description: This tutorial will guide you through the steps to host a server.
---

# ③ Host Unranked Server

{% hint style="warning" %}
* Port forwarding is only required for WAN servers. It's optional for LAN servers.
* Players do not need to do port forwarding. Only servers need to do that.
* BF2142ServerLauncher does not support mod. That's why you have to run it via a shortcut.
* Modded and unmodded servers read server settings files from different locations.
* For more server configurations, please refer to [https://pingperfect.com/index.php/knowledgebase/585/Battlefield-2142--Server-Configuration.html](https://pingperfect.com/index.php/knowledgebase/585/Battlefield-2142--Server-Configuration.html).
{% endhint %}

## Hosting a Modded Server on OpenSpy

In this example, we demonstrate how to host a server for the Remaster mod.

1. Use file explorer to navigate to the path "**C:\Program Files (x86)\Electronic Arts\Battlefield 2142 Server**"_._
2. Copy the folder <mark style="color:blue;">Project\_Remaster\_v14</mark> in <mark style="color:blue;">C:\Program Files (x86)\Electronic Arts\Battlefield 2142\mods</mark> and paste it to <mark style="color:blue;">C:\Program Files (x86)\Electronic Arts\Battlefield 2142 Server\mods</mark>_._
3. Right-click on "**BF2142\_w32ded.exe**" and click "**send it to desktop as a shortcut**".
4. Right-click the shortcut on your desktop and click "**Properties**".
5. In the target field, add **+modPath mods/Project\_Remaster\_v14** after "**C:\Program Files (x86)\Electronic Arts\Battlefield 2142 Server\BF2142\_w32ded.exe**". It should look like this:\
   ​"C:\Program Files (x86)\Electronic Arts\Battlefield 2142 Server\BF2142\_w32ded.exe" +modPath mods/Project\_Remaster\_v14
6. Click "**Apply**" and "**Confirm**".
7. Forward the following ports (i.e. port forwarding) to your local IP address in your wireless router control panel:\
   29900 - 29900 UDP or Both\
   29900 - 29900 UDP or Both\
   17567 - 17567 Both
8. Open "**C:\Program Files (x86)\Electronic Arts\Battlefield 2142 Server\mods\Project\_Remaster\_v14\Settings\ServerSettings.con**".\
   Make sure "**sv.internet**" is 1 and "**sv.allowNATNegotiation**"​ is 0.\
   &#xNAN;_&#x44;rag and drop the file to the desktop so that you can edit and save it._ \
   &#xNAN;_&#x4B;eep sv.intenet to 0 if you don't want your server to appear on the server browser._
9. Open ​​"**C:\Program Files (x86)\Electronic Arts\Battlefield 2142 Server\mods\Project\_Remaster\_v14\Settings\mapList.con**".\
   Add the line "**mapList.append Suez\_Canal gpm\_coop 16**" to add a map to the server.\
   &#xNAN;_&#x44;rag and drop the file to the desktop so that you can edit and save it._&#x20;
10. Double-click the shortcut on your desktop to run the server.

Note: "**C:\Program Files (x86)\Electronic Arts\Battlefield 2142 Server\mods\Project\_Remaster\_v14\Settings\ServerSettings.con**" is where you configure the server.

## Hosting an Unmodded Server on OpenSpy

1. Use file explorer to navigate to the path "**C:\Program Files (x86)\Electronic Arts\Battlefield 2142 Server**"_._&#x200B;
2. Look for "**BF2142ServerLauncher.exe**" in the folder. Double-click it to run the program.
3. Click the add icon to create a new config setting. Then you will be able to edit Server Settings and Map List. Make sure the "**Internet**" option is turned on and the "**AllowNATNegotiation**" is turned off.\
   &#xNAN;_&#x4B;eep the Internet option off if you don't want your server to appear on the server browser._&#x200B;
4. Forward the following ports (i.e. port forwarding) to your local IP address in your wireless router control panel:\
   29900 - 29900 UDP or Both\
   ​17567 - 17567 Both
5. Click "**Start**" to run the server.

Note: <mark style="color:blue;">C:\Users\xxxxx\Documents\Battlefield 2142\ServerConfigs</mark> is where you configure the server apart from using the server launcher.
