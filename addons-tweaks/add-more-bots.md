# More Bots Tweak

Many BF2142 players want to play with more bots — 16 just isn’t enough for most! With today’s PCs, you can easily run over 64 bots without lag, making for a much more immersive battlefield experience. If you enjoy grinding bots for fun, you’re not alone!  Here’s a guide on how to increase the number of bots in your game.

### Preparations

* Do you know where your game directory is? It’s the folder where `BF2142.exe` and `mods` are located. By default, this is usually: `C:\Program Files (x86)\Electronic Arts\Battlefield 2142`.
* You’ll be editing files in `mods\<MOD>\AI\AIDefault.ai`, so it’s a good idea to make a backup of the file first — just add a suffix like `_bak` or `_o` to the filename of the clone. **\[**[**?**](#user-content-fn-1)[^1]**]**
* If you want this change to affect vanilla BF2142, make your edits in the `mods\bf2142` folder. Otherwise, edit the files in the `mods\<MOD>` folder for your chosen mod.

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

```json
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
Once you’re done, just save your changes!

If you’re unable to save your changes, try dragging the `.ai` file to your Desktop, make your edits there, and then drag it back when you’re done.
{% endstep %}
{% endstepper %}

### Remarks

* When you launch the game and select a map, it might still display 16 bots, but if you’ve edited the file correctly, you’ll actually have the number of bots you set.
* Remember, everything is case sensitive — spelling mistakes or incorrect capitalization can cause the game to crash!
* If you host a server with this tweak, your server will have more bots, and players who join won’t need to make any changes on their end.

### Acknowledgements

Special thanks to:

* [asdasdadsdasdasdasda](https://www.moddb.com/members/na2740631) for sharing details on how to change bot counts @ [How To Change The Singleplayer Bot Count](https://www.moddb.com/mods/battlefield-2-world-at-war/tutorials/how-to-change-singleplayer-bot-count)

[^1]: That’s because it’s easy to restore the files. You wouldn’t want to go through the hassle of reinstalling the whole game just because something got messed up and you didn’t have a backup.

[^2]: Adding too many bots can cause performance drops or crashes on low-end PCs. Don’t go overboard — a good starting point is around 48 bots.

[^3]: This ensures the bot count doesn’t include human players, so you get the full number of bots you set.

[^4]: Doing this allows the game to override the normal 16 bot count.
