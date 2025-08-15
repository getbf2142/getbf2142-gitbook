# Add More Bots

A lot of BF2142 players want more bots—16 just isn’t enough! Modern PCs can easily handle 64+ bots for a much more immersive experience. If you love bot grinding, you’re in good company. Here’s how to increase the number of bots in your game.

### Preparations

* Do you know where your game directory is? It’s the folder with `BF2142.exe` and your `mods` — by default, usually at `C:\Program Files (x86)\Electronic Arts\Battlefield 2142`.
* If you want the changes for vanilla BF2142, edit the file in `\mods\bf2142`. For a specific mod, edit the file in that mod’s folder instead.
* You’ll be editing the `\mods\...\AI\AIDefault.ai` file, so it’s smart to make a backup first — just copy the file and add something like `_o` to the filename. **\[**[**?**](#user-content-fn-1)[^1]**]**

### Procedures

<details>

<summary>If you have Remaster mod installed ...</summary>

In the launcher, head to the <mark style="color:blue;">Settings</mark> tab, adjust the <mark style="color:blue;">Bot-Settings</mark> as needed, and then click <mark style="color:blue;">Apply</mark>. _(You don't have to follow any steps below.)_

</details>

{% stepper %}
{% step %}
Inside the `AI` folder, open `AIDefault.ai` with a text editor.
{% endstep %}

{% step %}
Look for the line `aiSettings.setMaxNBots 16` near the top of the file.
{% endstep %}

{% step %}
Change the number to however many bots you want — for example, `aiSettings.setMaxNBots 32` for 32 bots.

Keep in mind that **\[**[**...**](#user-content-fn-2)[^2]**]**
{% endstep %}

{% step %}
Make sure to set `aiSettings.maxBotsIncludeHumans` to 0. **\[**[**?**](#user-content-fn-3)[^3]**]**
{% endstep %}

{% step %}
Put `aiSettings.overrideMenuSettings 1` before the line with `aiSettings.maxBotsIncludeHumans 0`. **\[**[**?**](#user-content-fn-4)[^4]**]**
{% endstep %}

{% step %}
Your file should look something like this around lines 9–12:

```batch
aiSettings.overrideMenuSettings 1
aiSettings.maxBotsIncludeHumans 0
aiSettings.setMaxNBots 32
aiSettings.setBotSkill 1.0
```
{% endstep %}

{% step %}
You can also adjust the bot skill — set `aiSettings.setBotSkill` to any value between 0 and 1 (higher means tougher bots).
{% endstep %}

{% step %}
If you want to allow more AI-controlled weapons like UAVs, sentry guns, and drones on the map, set `aiSettings.setMaxNAutoControllers` to a higher value.&#x20;

The default is 64, which is usually enough, but you can safely increase it to over 100 if needed.
{% endstep %}

{% step %}
Once you’re done, just save your changes!

If you’re unable to save your changes, try dragging the `.ai` file to your Desktop, make your edits there, and then drag it back when you’re done.
{% endstep %}
{% endstepper %}

### Remarks

* When you launch the game and select a map, it might still show 16 bots — but if you’ve edited the file correctly, you’ll get the numbers right.
* Everything is case sensitive — spelling mistakes or wrong capitalization can crash the game!
* If you host a server with this tweak, your server will have more bots, and players who join won’t need to change anything.
* If it doesn’t work after editing, try copying the default content below into your `AIDefault.ai` file, then start all over again from step 1.

<details>

<summary>Default Content of <code>AIDefault.ai</code></summary>

```batch
echo *****************************************************************************************
echo AIDefault.ai ****************************************************************************
echo *****************************************************************************************

aiSettings.setNSides 2
aiSettings.setAutoSpawnBots 1
aiSettings.setMaxNAutoControllers 256


aiSettings.maxBotsIncludeHumans 1
aiSettings.setMaxNBots 16
aiSettings.setBotSkill 0.4

rem To spawn more than 15 bots in SP, use the following lines instead of the three lines above.
rem Note that this is totaly unsupported, it will affect your system's performance 
rem and may even crash your game. That being said, you will most likely be able to run a lot
rem more bots than 15 on your system. 

rem Example for 32 bot game with expert bots

beginrem
aiSettings.overrideMenuSettings 1
aiSettings.maxBotsIncludeHumans 0
aiSettings.setMaxNBots 32
aiSettings.setBotSkill 1.0
endrem

run BotNames.ai

aiSettings.setInformationGridDimension 32

aiSettings.setDiscoverCloakedEnemiesDistance 3.0


run AIPathFinding.ai
run AutoControllers.ai

rem EOF

```

</details>

### Acknowledgements

Special thanks to:

* [asdasdadsdasdasdasda](https://www.moddb.com/members/na2740631) for sharing details on how to change bot counts @ [How To Change The Singleplayer Bot Count](https://www.moddb.com/mods/battlefield-2-world-at-war/tutorials/how-to-change-singleplayer-bot-count)

[^1]: `_o` denotes the original.



    If something goes wrong, you can easily restore the files without having to reinstall the whole game. Having a backup saves you a lot of hassle!

[^2]: Adding too many bots can cause performance drops or crashes on low-end PCs. Don’t go overboard — a good starting point is around 48 bots.

[^3]: This ensures the bot count doesn’t include human players, so you get the full number of bots you set.

[^4]: Doing this allows the game to override the normal 16 bot count.
