# Unlimited Sprint Tweak

If you’re getting used to the new Battlefield’s play style, you might find BF2142’s limited sprint a bit frustrating. Unlimited sprint is really just about convenience — some players see no reason not to have it. So, let’s mod BF2142 to give ourselves unlimited sprint too!

### Preparations

* Do you know where your game directory is? It’s the folder where `BF2142.exe` and `mods` are located. By default, this is usually: `C:\Program Files (x86)\Electronic Arts\Battlefield 2142`.
* You’ll be editing files in `mods\<MOD>\Objects\Soldiers_server.zip`, so it’s a good idea to make a backup of the file first — just add a suffix like `_bak` or `_o` to the filename of the clone. \[Why?[^1]]
* If you want this change to affect vanilla BF2142, make your edits in the `mods\bf2142` folder. Otherwise, edit the files in the `mods\<MOD>` folder for your chosen mod.

## Here we go ...

1. Inside `Soldiers_server.zip`, open the `EU` or `PAC` folder and edit the `.tweak` files. For example, to modify the EU heavy armor soldier, open `us/US_HEAVY_SOLDIER.tweak` with a text editor and make your changes like this:

```json
ObjectTemplate.SprintRecoverTime 1
ObjectTemplate.SprintDissipationTime 100
ObjectTemplate.SprintLimit 0.1
ObjectTemplate.SprintLossAtJump 0.10
```

2. Increase `SprintDissipationTime` to give yourself a bigger buffer before sprint runs out, and lower `SprintRecoverTime` so sprint refills quicker.
3. You can also adjust `SprintLimit` and `SprintLossAtJump` if you want, but the first two settings are usually enough. `SprintLimit` sets the minimum sprint bar needed before you can sprint again, while `SprintLossAtJump` controls how much sprint bar you lose when you jump.
4. Save your changes.
5. If you’re unable to save your changes, try dragging the `.zip` file to your Desktop, make your edits there, and then drag it back when you’re done.

## Something to note ...

* If you want to play with friends over LAN, everyone needs to have the same modification.
* If you plan to join a server without this mod, just switch back to your original `Soldiers_server.zip` file.

## Special thanks to ...

* [FFOLKES](https://forums.bf2s.com/profile.php?id=5041) for sharing details on how to modify sprint @ [BF2S Forum](https://forums.bf2s.com/viewtopic.php?id=23762)

[^1]: That’s because it’s easy to restore the files. You wouldn’t want to go through the hassle of reinstalling the whole game just because something got messed up and you didn’t have a backup.
