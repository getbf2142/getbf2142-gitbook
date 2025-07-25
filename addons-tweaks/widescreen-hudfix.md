# Widescreen Hudfix

When BF2142 first launched, it only supported 4:3 displays. Even though the v1.51 patch from EA added native widescreen support (which mostly just stretches the image horizontally), the game’s HUD still looks off on 16:9 resolutions.&#x20;

Thanks to the Project Remaster Team for creating a widescreen HUD fix for BF2142 that properly resizes HUD elements for widescreen displays. This fix is included with the [Project Remaster](../getting-started/download-and-install-remaster-mod.md) v14 installation, and in this guide, we’ll also show you how to install it if you don’t have the mod.

## If you have Remaster Mod ...

Activating Widescreen Hudfix is a breeze! Just open your <mark style="color:blue;">Remaster Launcher</mark>, go to the <mark style="color:blue;">Settings</mark> tab, and check both the <mark style="color:blue;">Widescreen Fix</mark> and <mark style="color:blue;">HUD-fix</mark> options. That’s all you need to do — you’re good to go! The <mark style="color:blue;">Widescreen Fix</mark> adds the widescreen flag to your launch parameters, while the <mark style="color:blue;">HUD-fix</mark> makes sure your HUD displays correctly in a 16:9 ratio.

If you ever want to uninstall, simply uncheck those two options. Then, head over to the <mark style="color:blue;">Help</mark> tab and click <mark style="color:blue;">Clear Cache</mark>. That’s it — super simple!

## If you don't have Remaster Mod ...



1. Download **BF2142\_Widescreen\_Hudfix.zip** from above.
2. Extract the two files inside: **Menu\_server\_hudfix.zip** and **Shaders\_client\_hudfix.zip**.
3. Drag and drop both files into your `mods\bf2142` folder.
4. Create backup copies of **ClientArchives.con** and **ServerArchives.con** from `mods\bf2142` folder.
5. Move the original **ClientArchives.con** and **ServerArchives.con** files to your Desktop for easy editing.
6. Open **ClientArchives.con** with a text editor.
7.  At the very top of the file, add this line:

    ```
    fileManager.mountArchive Shaders_client_hudfix.zip Shaders
    ```

    Make sure this line comes before the original `fileManager.mountArchive Shaders_client.zip Shaders` line, so the HUD fix loads first and takes precedence.
8. Open **ServerArchives.con** with a text editor.
9.  At the very top of the file, add this line:

    ```
    fileManager.mountArchive Menu_server_hudfix.zip Menu
    ```

    Make sure this line comes before the original `fileManager.mountArchive Menu_server.zip Menu`  line, so the HUD fix loads first and takes precedence.

And that’s it — you’re all set!



Since this is a client-side mod that changes \_client.zip, you should be able to join vanilla servers if you apply this changes to mod/bf2142. But do it at your own risk. No one knows if Punkbuster is getting strict on it. If you experience kicks after using it, disable it with online multiplayer

## Special thanks to ...

* Remaster Team for creating this fix
* ompadu on Remaster Discord for installing this fix for vanilla bf2142

