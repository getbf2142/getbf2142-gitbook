# Widescreen Hudfix

When BF2142 first launched, it only supported 4:3 displays. Even though the v1.51 patch from EA added native widescreen support (which mostly just stretches the image horizontally), the game’s HUD still looks off on 16:9 resolutions.&#x20;

Thanks to the Project Remaster Team for creating a widescreen HUD fix for BF2142 that properly resizes HUD elements for widescreen displays. This fix is included with the [Project Remaster](../project-remaster/download-and-install-remaster-mod.md) v14 installation, and in this guide, we’ll also show you how to install it if you don’t have the mod.

{% columns %}
{% column %}
<figure><img src="../.gitbook/assets/hudfix_before.png" alt=""><figcaption><p>BEFORE: Without Widescreen Hudfix</p></figcaption></figure>
{% endcolumn %}

{% column %}
<figure><img src="../.gitbook/assets/hudfix_after.png" alt=""><figcaption><p>AFTER: With Widescreen Hudfix</p></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

## Let's install it !

<details>

<summary>If you have Remaster mod installed ...<br><em>(Hudfix for Remaster mod)</em></summary>

To activate Widescreen Hudfix for your Remaster gameplay:

1. Open your <mark style="color:blue;">Remaster Launcher</mark>.
2. Go to the <mark style="color:blue;">Settings</mark> tab.
3. Check both the <mark style="color:blue;">Widescreen Fix</mark> and <mark style="color:blue;">HUD-fix</mark> options.
4. That’s all you need to do — you’re good to go!&#x20;

The <mark style="color:blue;">Widescreen Fix</mark> adds the widescreen flag to your launch parameters, while the <mark style="color:blue;">HUD-fix</mark> makes sure your HUD displays correctly in a 16:9 ratio.

If you ever want to uninstall, simply uncheck those two options. Then, head over to the <mark style="color:blue;">Help</mark> tab and click <mark style="color:blue;">Clear Cache</mark>. That’s it — super simple!

</details>

<details>

<summary>If you don't have Remaster mod installed ...<br><em>(Hudfix for Vanilla BF2142, or mods besides Remaster mod)</em></summary>

## Before we start ...

* Do you know where your game directory is? It’s the folder where `BF2142.exe` and `mods` are located. By default, this is usually: `C:\Program Files (x86)\Electronic Arts\Battlefield 2142`.
* You’ll be editing files in `mods\<MOD>`, so it’s a good idea to make a backup of the target files first — just add a suffix like `_bak` or `_o` to the filename of the clone. \[Why?[^1]]
* If you want this change to affect vanilla BF2142, make your edits in the `mods\bf2142` folder. Otherwise, edit the files in the `mods\<MOD>` folder for your chosen mod.

## Here we go ...

1. Download `BF2142_Widescreen_Hudfix.zip` from the link above.
2. Extract the two files inside: `Menu_server_hudfix.zip` and `Shaders_client_hudfix.zip`.
3. Drag and drop both files into your `mods\<MOD>` folder.
4. Open `ClientArchives.con` with a text editor.
5.  At the head of the file, add this line \[Why?[^2]]:

    ```
    fileManager.mountArchive Shaders_client_hudfix.zip Shaders
    ```
6. Save the file.
7. Open `ServerArchives.con` with a text editor.
8.  At the head of the file, add this line \[Why?[^3]]:

    ```
    fileManager.mountArchive Menu_server_hudfix.zip Menu
    ```
9. Save the file.
10. If you use a shortcut to launch the game, right-click it, go to <mark style="color:blue;">Properties</mark>, and check the <mark style="color:blue;">Target</mark> field for these flags \[How?[^4]]:

    ```json
    "C:\Program Files (x86)\Electronic Arts\Battlefield 2142\BF2142.exe" +menu 1 +fullscreen 0 +widescreen 1 +szx 1920 +szy 1200  
    ```
11. And that’s it — you’re all set!

## Something to note ...

* If you’re unable to save the changes, try moving the two .con files to your Desktop first. Edit and save them there, then move them back into the `mods/bf2142` folder.
* It’s unclear if you’ll run into issues with this fix enabled on Reclamation public servers. If you get kicked, just revert your changes before playing multiplayer.
* To uninstall the fix, just reverse the changes you made. Always remember to back up your files before editing, so you can easily restore them if needed.

</details>

## Special thanks to ...

* [Project Remaster Team](https://discord.com/invite/nVdDkgA) for creating this fix
* ompadu for sharing details on how to install the fix on vanilla BF2142 @ [Remaster Discord](https://discord.com/invite/nVdDkgA)



[^1]: That’s because it’s easy to restore the files. You wouldn’t want to go through the hassle of reinstalling the whole game just because something got messed up and you didn’t have a backup.

[^2]: This ensures this line comes before the original `fileManager.mountArchive Shaders_client.zip Shaders` line, so the HUD fix loads first and takes precedence.

[^3]: This ensures this line comes before the original `fileManager.mountArchive Menu_server.zip Menu`  line, so the HUD fix loads first and takes precedence.

[^4]: (0 means disable, 1 means enable)



    `+menu 1` helps prevent crashes at the menu startup.



    `+widescreen 1` enables widescreen support for wider aspect ratio resolutions.



    `+fullscreen 1` launches the game in fullscreen mode; set it to 0 for windowed mode.

    \
    `+szx 1920 +szy 1200` forces the game to use your chosen resolution.

    \
    Make sure the shortcut points to the correct directory where `BF2142.exe` is located.



    Check [here](https://www.moddb.com/tutorials/how-to-install-and-start-any-bf2142-mod-universal-tutorial-with-pictures) and [there](https://vandalfsen.me/tweakguides/BF2142_7.html) for more details on shortcut.
