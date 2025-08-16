# ③ Hosting a dedicated server

This tutorial will guide you through the steps to host a dedicated _unranked_ server.

<details>

<summary>Just a couple of things to note ...</summary>

* Port forwarding is only needed if you want your server to be accessible over the internet (WAN), and only the host needs to set it up.

- `BF2142ServerLauncher` does not support mod. That's why you have to run it via a shortcut.
- Modded and unmodded servers read server settings files from different locations.

</details>

### Hosting a Modded Server

In this example, we demonstrate how to host a dedicated server for the [Remaster](../project-remaster/download-and-install-remaster-mod.md) mod.&#x20;

{% stepper %}
{% step %}
Use File Explorer to go to `C:\Program Files (x86)\Electronic Arts\Battlefield 2142 Server`.
{% endstep %}

{% step %}
Copy the folder `Project_Remaster_v14` from `C:\Program Files (x86)\Electronic Arts\Battlefield 2142\mods` and paste it into `C:\Program Files (x86)\Electronic Arts\Battlefield 2142 Server\mods`.
{% endstep %}

{% step %}
Right-click `BF2142_w32ded.exe` and select <mark style="color:blue;">Send to > Desktop (create shortcut)</mark>.
{% endstep %}

{% step %}
On your desktop, right-click the shortcut and choose <mark style="color:blue;">Properties</mark>.
{% endstep %}

{% step %}
In the <mark style="color:blue;">Target</mark> field, add `+modPath mods/Project_Remaster_v14` after the path, so it looks like this:

```json
"C:\Program Files (x86)\Electronic Arts\Battlefield 2142 Server\BF2142_w32ded.exe" +modPath mods/Project_Remaster_v14
```
{% endstep %}

{% step %}
Click <mark style="color:blue;">Apply</mark> and then <mark style="color:blue;">OK</mark> to confirm.
{% endstep %}

{% step %}
In your router’s control panel, forward these ports to your local IP address:

* `29900` UDP or Both
* `17567` Both
{% endstep %}

{% step %}
Open `C:\Program Files (x86)\Electronic Arts\Battlefield 2142 Server\mods\Project_Remaster_v14\Settings\ServerSettings.con` with a text editor.

Note that this is where you tweak your server settings.\
Refer to the list of server settings [here](../addons-tweaks/server-settings.md#list-of-server-settings).
{% endstep %}

{% step %}
Make sure `sv.internet` is set to 1 and `sv.allowNATNegotiation` is set to 0.\
(Tip: Drag the file to your desktop to edit and save it, then move it back.)

If you don’t want your server to appear in the server browser, set `sv.internet` to 0.
{% endstep %}

{% step %}
Open `C:\Program Files (x86)\Electronic Arts\Battlefield 2142 Server\mods\Project_Remaster_v14\Settings\mapList.con` with a text editor.
{% endstep %}

{% step %}
Add this line to include a map: `mapList.append Suez_Canal gpm_coop 16`.\
(Again, drag the file to your desktop to edit and save it.)

Refer to [here](https://www.moddb.com/members/antniquiler/blogs/installing-a-battlefield-2142-dedicated-server-on-linux-part-2) to know how to configure the map rotation.
{% endstep %}

{% step %}
Double-click the shortcut on your desktop to start the server.
{% endstep %}
{% endstepper %}

### Hosting a Vanilla Server

{% stepper %}
{% step %}
Use File Explorer to go to `C:\Program Files (x86)\Electronic Arts\Battlefield 2142 Server`.
{% endstep %}

{% step %}
Find `BF2142ServerLauncher.exe` in the folder and double-click it to open.
{% endstep %}

{% step %}
Click the <mark style="color:blue;">Add</mark> icon to create a new config setting.
{% endstep %}

{% step %}
You can now edit the <mark style="color:blue;">Server Settings</mark> and <mark style="color:blue;">Map List</mark>.
{% endstep %}

{% step %}
Make sure the <mark style="color:blue;">Internet</mark> option is turned on and <mark style="color:blue;">AllowNATNegotiation</mark> is turned off.

If you don’t want your server to show up in the server browser, leave the <mark style="color:blue;">Internet</mark> option off.
{% endstep %}

{% step %}
Open `C:\Users\<YOU>\Documents\Battlefield 2142\ServerConfigs.con` with a text editor.

This is where you configure the server apart from using the server launcher.\
Refer to the list of server settings [here](../addons-tweaks/server-settings.md#list-of-server-settings).
{% endstep %}

{% step %}
In your router’s control panel, forward these ports to your local IP address:

* `29900` UDP or Both
* `17567` Both
{% endstep %}

{% step %}
Click <mark style="color:blue;">Start</mark> to launch the server.
{% endstep %}
{% endstepper %}
