# Field of View (FOV) Tweak

Unlike modern Battlefield games, BF2142 doesn’t let you adjust your FOV in-game. Many players find the default field of view too low, so this guide will show you how to change it to whatever you prefer!

{% columns %}
{% column %}
<figure><img src="../.gitbook/assets/kursk_fov_1_1.png" alt="" width="375"><figcaption><p>1.1</p></figcaption></figure>
{% endcolumn %}

{% column %}
<figure><img src="../.gitbook/assets/kursk_fov_1_5.png" alt="" width="375"><figcaption><p>1.5</p></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

## Before we start ...

* You’ll be editing files in `mods/<MOD>/Objects/Soldiers_server.zip`, so it’s a good idea to make a backup of the .zip file first — just add a suffix like `_bak` or `_o` to the filename of the clone. \[Why?[^1]]
* If you want this change to affect vanilla BF2142, make your edits in the `mods/bf2142` folder. Otherwise, edit the files in the `mods/<MOD>` folder for your chosen mod.

## Here we go ...

1. Inside `Soldiers_server.zip`, open the `Common` folder and edit the `SoldierCamera.tweak` file using a text editor. Here are the lines we want to tweak, along with their default values:

```json
ObjectTemplate.worldFOV 1.1
ObjectTemplate.insideFOV 1.1
```

2. You can set the value as low as `0.65` to mimic BF P4F’s FOV, or as high as `1.85` for an ultra-wide view  — but keep in mind, the game doesn’t look great with extreme settings.&#x20;

* According to illicitSoul on ModDB, a value of `1.1` gives you about 60-65 FOV, while `1.6` is roughly 90-95 FOV. So, a good starting point is by changing `1.1` to `1.5`.

3. Save your changes.

## Special thanks to ...

* [illicitSoul](https://www.moddb.com/members/ainas) for sharing details on how to modify FOV

This guide is based on info from [https://www.moddb.com/tutorials/bf2bf2142-field-of-view-modding-tutorial](https://www.moddb.com/tutorials/bf2bf2142-field-of-view-modding-tutorial).

[^1]: That’s because it’s easy to restore the files. You wouldn’t want to go through the hassle of reinstalling the whole game just because something got messed up and you didn’t have a backup.
