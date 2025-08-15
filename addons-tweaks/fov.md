# Field of View (FOV)

Unlike modern Battlefield games, BF2142 doesn’t let you adjust your FOV in-game. Many players find the default field of view too low, so this guide will show you how to change it to whatever you prefer!

{% columns %}
{% column %}
<figure><img src="../.gitbook/assets/kursk_fov_1_1.png" alt="" width="375"><figcaption><p>1.1</p></figcaption></figure>
{% endcolumn %}

{% column %}
<figure><img src="../.gitbook/assets/kursk_fov_1_5.png" alt="" width="375"><figcaption><p>1.5</p></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

### Preparations

* Do you know where your game directory is? It’s the folder with `BF2142.exe` and your `mods` — by default, usually at `C:\Program Files (x86)\Electronic Arts\Battlefield 2142`.
* If you want the changes for vanilla BF2142, edit the file in `\mods\bf2142`. For a specific mod, edit the file in that mod’s folder instead.
* You’ll be editing the `\mods\...\Objects\Soldiers_server.zip` file, so it’s smart to make a backup first — just copy the file and add something like `_o` to the filename. **\[**[**?**](#user-content-fn-1)[^1]**]**

### Procedures

{% stepper %}
{% step %}
Inside `Soldiers_server.zip`, open the `Common` folder and edit the `SoldierCamera.tweak` file using a text editor.&#x20;

Here are the lines we want to tweak, along with their default values:

```batch
ObjectTemplate.worldFOV 1.1
ObjectTemplate.insideFOV 1.1
```
{% endstep %}

{% step %}
You can set the value as low as `0.65` to mimic BF P4F’s FOV, or as high as `1.85` for an ultra-wide view  — but keep in mind, the game doesn’t look great with extreme settings.
{% endstep %}

{% step %}
According to illicitSoul on ModDB, a value of `1.1` gives you about 60-65 FOV, while `1.6` is roughly 90-95 FOV. So, a good starting point is by changing `1.1` to `1.5`.
{% endstep %}

{% step %}
Save your changes.

If you’re unable to save your changes, try dragging the `.zip` file to your Desktop, make your edits there, and then drag it back when you’re done.
{% endstep %}
{% endstepper %}

### Remarks

* Revert your changes before joining Reclamation or any multiplayer servers, unless the server explicitly allows or uses this mod.
* If you host a server with this tweak, players who join will also need to make this change.
* To uninstall the fix, simply undo the changes you made.

### Acknowledgements

Special thanks to:

* [illicitSoul](https://www.moddb.com/members/ainas) for sharing details on how to modify FOV @ [BF2/BF2142 FOV Modding Tutorial](https://www.moddb.com/tutorials/bf2bf2142-field-of-view-modding-tutorial)

[^1]: `_o` denotes the original.



    If something goes wrong, you can easily restore the files without having to reinstall the whole game. Having a backup saves you a lot of hassle!
