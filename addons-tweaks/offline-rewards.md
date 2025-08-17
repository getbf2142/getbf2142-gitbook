---
icon: medal
---

# Offline Rewards

This patch emulates the ranked server rewards system — pins, ribbons, badges, and medals — in your singleplayer or LAN coop games. It’s a great quality-of-life improvement that makes bot grinding much more fun. Imagine earning a bunch of medals in one game — it’s pretty satisfying!

In vanilla, earning medals or badges was tough since many required things like 150 hours played or 300 EU team wins — goals you can’t reach in a single round. To fix this, we’ve reworked the rewards system and requirements to better suit a quick co-op games:

* Titan mode rewards have been removed.
* Requirements that were impossible to achieve are now gone.
* Most rewards can now be earned within about 15 minutes of play.

### Catalogue

{% tabs %}
{% tab title="How to ?" %}
Check the relevant tabs for more details on how to get the rewards.
{% endtab %}

{% tab title="v2" %}
{% embed url="https://drive.google.com/file/d/1Z5y7vFvdRZHqzQprv4zCwsvl_vzeiL5d" %}
{% endtab %}

{% tab title="v1" %}
{% embed url="https://drive.google.com/file/d/1NWUVSEbD-IXb-gXaO_t6aKgiQiSZhRmo" %}
{% endtab %}
{% endtabs %}

### Procedures

{% stepper %}
{% step %}
Download the patch from [Downloads](offline-rewards.md#downloads).
{% endstep %}

{% step %}
Go to the folder where your `BF2142.exe` is located — by default, that’s usually `C:\Program Files (x86)\Electronic Arts\Battlefield 2142`.
{% endstep %}

{% step %}
In your game directory, find the folder named `python` and rename it to something like `python_o` or `python_backup` to create a backup.
{% endstep %}

{% step %}
Drag and drop the `python` folder from the `.zip` file into the root directory of your game folder.
{% endstep %}
{% endstepper %}

### Downloads

{% tabs %}
{% tab title="Downloads" %}
**BF2142 Offline Rewards Patch v2 (37 KB)**

{% embed url="https://www.mediafire.com/file/35dhux0ys3sjxr2/BF2142_Offline_Rewards_v2.zip/file" %}

{% embed url="https://drive.google.com/file/d/1QelzAksf84NheB0HWL6fyvcCFxRIybjX" %}

**BF2142 Offline Rewards Patch v1 (42 KB)**

{% embed url="https://drive.google.com/file/d/16WwI7T8NAv3oJaNS4BysAfJ2Uev2ugrd" %}
{% endtab %}

{% tab title="Changelogs" %}
**v2**

* Added support for all Remaster mod weapons in `constants.py`
* Fixed several rewards that weren’t working by updating their requirements in `medal_data.py`
* Made it easier to enable or disable log functions in `__init__.py`
* Cleaned up code in `rank.py` and `unlocks.py`
{% endtab %}
{% endtabs %}

### Remarks

* This patch applies to all mods, including vanilla 2142.
* This patch only affects singleplayer and has no impact on multiplayer.
* This patch has been tested in multiplayer — you won’t get kicked for having it installed.
* This patch only emulates rewards for the current round and reset when the game ends.
* To enable logging, edit `python\bf2\__init__.py` and adjust the values for `g_debug`, `g_debug_log`, and `g_falog`.

### Acknowledgements

Special thanks to:

* [maiorBoltach](https://github.com/maiorBoltach) for writing the python files to support rewards emulation @ [bf2142stats\_emu](https://github.com/maiorBoltach/bf2142stats_emu)
* Dennie for optimising the rewards requirements and adding support for Remaster mod weapons @ [BF2142 Remastered](https://discord.com/invite/nVdDkgA)
