# Unlimited Sprint Tweak

If you’re getting used to the new Battlefield’s play style, you might find BF2142’s limited sprint a bit frustrating. Unlimited sprint is really just about convenience — some players see no reason not to have it. So, let’s mod BF2142 to give ourselves unlimited sprint too!

## Before we start ...

* You’ll be editing files in `mods/<MOD>/Objects/Soldiers_server.zip`, so it’s a good idea to make a backup of the .zip file first — just add a suffix like `_bak` or `_o` to the filename of the clone.
* If you want this change to affect vanilla BF2142, make your edits in the `mods/bf2142` folder. Otherwise, edit the files in the `mods/<MOD>` folder for your chosen mod.

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

## Keep in mind ...

If you want to play with friends over LAN, everyone needs to have the same modification. If you plan to join a server without this mod, just switch back to your original `Soldiers_server.zip` file.

## Special thanks to ...

* [FFOLKES](https://forums.bf2s.com/profile.php?id=5041) sharing details on how to modify sprint

This guide is based on info from [https://forums.bf2s.com/viewtopic.php?id=23762](https://forums.bf2s.com/viewtopic.php?id=23762).
