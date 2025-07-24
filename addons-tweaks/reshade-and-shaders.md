# ReShade & Shaders

Reshade adds a layer of shaders to the game, giving the visuals a big boost. It was first used in Project Reality for BF2 and has since been adapted for BF2142 as well.

A few things to note:

* Reshade can lower your FPS, so you might see a performance hit.
* It only works on Windows 7 or newer.
* Reshade will apply to all mods, including vanilla 2142.
* To uninstall, just delete the files you added.

The original post about Reshade for BF2142 by the Project Remaster Team is here:&#x20;

{% embed url="https://www.moddb.com/downloads/bf2142-reshade" %}

However, that version is outdated. The team now uses a newer Reshade client and has updated shader presets. The latest Reshade package for BF2142 is included with the [Remaster Mod](../getting-started/download-and-install-remaster-mod.md) v14 installation.

## If you have Remaster Mod ...

Activating Reshade is super simple. Just open your <mark style="color:blue;">Remaster Launcher</mark>, go to the <mark style="color:blue;">Settings</mark> tab, and enable the <mark style="color:blue;">Reshade</mark> option. That’s it — you’re all set!

## If you don't have Remaster Mod ...

{% tabs %}
{% tab title="Latest Release" %}
{% embed url="https://drive.google.com/file/d/1McXt77aT1TUCl72h9LOy3zSMRbR97fEv" %}
{% endtab %}

{% tab title="Older Release" %}
{% embed url="https://www.moddb.com/downloads/bf2142-reshade" %}
{% endtab %}
{% endtabs %}

1. Download either the latest or older release.
2. Extract all the files from the .rar to the folder where your `BF2142.exe` is located — by default, that’s usually `C:\Program Files (x86)\Electronic Arts\Battlefield 2142`. If not, then manually edit all the paths in `d3d9.ini` .

## Let’s try it out in-game !

1. Launch the game.
2. Press <mark style="color:blue;">Shift + F2</mark> to open ReShade in-game tool.
3. On the <mark style="color:blue;">Home</mark> tab, check if the preset has loaded — you should see shaders like Levels.fx and Vignette.fx listed. If the page is empty, the shaders are not loaded yet.&#x20;
   1. Go to the <mark style="color:blue;">Settings</mark> tab and enter the correct paths:
      1. Effect search path: `C:\Program Files (x86)\Electronic Arts\Battlefield 2142\reshade-shaders\Shaders` (or wherever your setup is)
      2. Texture search path: `C:\Program Files (x86)\Electronic Arts\Battlefield 2142\reshade-shaders\Textures` (or wherever your setup is)
   2. Then return to the <mark style="color:blue;">Home</mark> tab and click <mark style="color:blue;">Reload</mark>. The preset should load properly now.

By default, you can toggle the Reshade effect with the <mark style="color:blue;">Scroll Lock</mark> key, but you can change this key bind using the in-game tool. I would recommend setting it to <mark style="color:blue;">Shift + F1</mark>.

If you want to adjust the shaders, just go to the <mark style="color:blue;">Settings</mark> tab and enable <mark style="color:blue;">Configuration Mode</mark>. Then, return to the <mark style="color:blue;">Home</mark> tab to tweak the parameters however you like.

## Special thanks to ...

* Project Remaster Team for making this shaders for BF2142

This guide is based on info from [https://www.moddb.com/mods/heat-of-battle2/downloads/heat-of-battle-reshade-20](https://www.moddb.com/mods/heat-of-battle2/downloads/heat-of-battle-reshade-20) and [https://www.moddb.com/downloads/bf2142-reshade](https://www.moddb.com/downloads/bf2142-reshade).

