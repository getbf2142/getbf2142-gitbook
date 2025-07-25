# Widescreen Hudfix

When BF2142 first launched, it only supported 4:3 displays. Even though the v1.51 patch from EA added native widescreen support (which mostly just stretches the image horizontally), the game’s HUD still looks off on 16:9 resolutions.&#x20;

Thanks to the Project Remaster Team for creating a widescreen HUD fix for BF2142 that properly resizes HUD elements for widescreen displays. This fix is included with the [Project Remaster](../getting-started/download-and-install-remaster-mod.md) v14 installation, and in this guide, we’ll also show you how to install it if you don’t have the mod.

## If you have Remaster Mod ...

1. Open your <mark style="color:blue;">Remaster Launcher</mark>.
2. Go to the <mark style="color:blue;">Settings</mark> tab.
3. Check both the <mark style="color:blue;">Widescreen Fix</mark> and <mark style="color:blue;">HUD-fix</mark> options.
4. That’s all you need to do — you’re good to go!&#x20;

The <mark style="color:blue;">Widescreen Fix</mark> adds the widescreen flag to your launch parameters, while the <mark style="color:blue;">HUD-fix</mark> makes sure your HUD displays correctly in a 16:9 ratio.

If you ever want to uninstall, simply uncheck those two options. Then, head over to the <mark style="color:blue;">Help</mark> tab and click <mark style="color:blue;">Clear Cache</mark>. That’s it — super simple!

## If you don't have Remaster Mod ...

If you want this change to affect vanilla BF2142, make your edits in the `mods/bf2142` folder. Otherwise, edit the files in the `mods/<MOD>` folder for your chosen mod.

{% embed url="https://drive.google.com/file/d/1dQUtpF37JYJhgEwCeqZ2Nqxd48dGNn8j" %}

#### Here we go ...

1. Download **BF2142\_Widescreen\_Hudfix.zip** from the link above.
2. Extract the two files inside: **Menu\_server\_hudfix.zip** and **Shaders\_client\_hudfix.zip**.
3. Drag and drop both files into your `mods\<MOD>` folder.
4. Open **ClientArchives.con** with a text editor.
5.  At the very top of the file, add this line \[Why?[^1]]:

    ```
    fileManager.mountArchive Shaders_client_hudfix.zip Shaders
    ```
6. Save the file.
7. Open **ServerArchives.con** with a text editor.
8.  At the very top of the file, add this line \[Why?[^2]]:

    ```
    fileManager.mountArchive Menu_server_hudfix.zip Menu
    ```
9. Save the file.
10. And that’s it — you’re all set!

#### Something more to note ...

* If you’re unable to save the changes, try moving the two .con files to your Desktop first. Edit and save them there, then move them back into the `mods/bf2142` folder.
* Since this is a client-side mod that changes \_client.zip, you should be able to join vanilla servers if you apply this changes to `mod/bf2142`.
* To uninstall the fix, simply undo what you have done.

## Special thanks to ...

* Project Remaster Team for creating this fix
* ompadu on Remaster Discord for providing details on how to install this fix on vanilla bf2142



[^1]: This ensures this line comes before the original `fileManager.mountArchive Shaders_client.zip Shaders` line, so the HUD fix loads first and takes precedence.

[^2]: This ensures this line comes before the original `fileManager.mountArchive Menu_server.zip Menu`  line, so the HUD fix loads first and takes precedence.
