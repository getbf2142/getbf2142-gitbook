---
icon: person-running-fast
---

# Unlimited Sprint

If you’re getting used to the new Battlefield’s play style, you might find BF2142’s limited sprint a bit frustrating. Unlimited sprint is really just about convenience — some players see no reason not to have it. So, let’s mod BF2142 to give ourselves unlimited sprint too!

### Preparations

* Do you know where your game directory is? It’s the folder with `BF2142.exe` and your `mods` — by default, usually at `C:\Program Files (x86)\Electronic Arts\Battlefield 2142`.
* If you want the changes for vanilla BF2142, edit the file in `\mods\bf2142`. For a specific mod, edit the file in that mod’s folder instead.
* You’ll be editing the `\mods\...\Objects\Soldiers_server.zip` file, so it’s smart to make a backup first — just copy the file and add something like `_o` to the filename. **\[**[**?**](#user-content-fn-1)[^1]**]**

### Procedures

{% stepper %}
{% step %}
Inside `Soldiers_server.zip`, open the `EU` or `PAC` folder and edit the `.tweak` files.&#x20;

For example, to modify the EU heavy armor soldier, open `\us\US_HEAVY_SOLDIER.tweak` with a text editor and make your changes like this:

```batch
ObjectTemplate.SprintRecoverTime 1
ObjectTemplate.SprintDissipationTime 100
ObjectTemplate.SprintLimit 0.1
ObjectTemplate.SprintLossAtJump 0.10
```
{% endstep %}

{% step %}
Increase `SprintDissipationTime` to give yourself a bigger buffer before sprint runs out, and lower `SprintRecoverTime` so sprint refills quicker.
{% endstep %}

{% step %}
You can also adjust `SprintLimit` and `SprintLossAtJump` if you want, but the first two settings are usually enough.

`SprintLimit` sets the minimum sprint bar needed before you can sprint again, while `SprintLossAtJump` controls how much sprint bar you lose when you jump.
{% endstep %}

{% step %}
Save your changes.

If you’re unable to save your changes, try dragging the `.zip` file to your Desktop, make your edits there, and then drag it back when you’re done.
{% endstep %}

{% step %}
Don’t forget to make the same changes to `Soldiers_bp1_server.zip` if you plan to play on Northern Strike maps.
{% endstep %}
{% endstepper %}

### Remarks

* Revert your changes before joining Reclamation or any multiplayer servers, unless the server explicitly allows or uses this mod.
* If you host a server with this tweak, players who join will also need to make this change.
* To uninstall the fix, simply undo the changes you made.

### Acknowledgements

Special thanks to:

* [FFOLKES](https://forums.bf2s.com/profile.php?id=5041) for sharing details on how to modify sprint @ [BF2S Forum](https://forums.bf2s.com/viewtopic.php?id=23762)

[^1]: `_o` denotes the original.



    If something goes wrong, you can easily restore the files without having to reinstall the whole game. Having a backup saves you a lot of hassle!
