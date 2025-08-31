---
icon: clapperboard-play
---

# BattleRecorder & BattleDirector

BattleRecorder is a built-in feature for BF2142. To watch a recording, you will need to use BattleDirector.

{% hint style="warning" %}
With OpenSpy patches, you won't see the demo files in Community > Battle Recorder in-game.
{% endhint %}

### Preparations

1. Manually create the `Demos` folder in `Battlefield 2142\mods\<MODS>`.
2. Download BattleDirector from Downloads and install it.
3. Read Quick Help in BattleDirector.
4. Set Game to Battlefield 2142 and Game EXE locatation to align with your setup.
5. Configure Resolution. Add “ +widescreen 1” to the second input box for full widescreen support. You can append more flags if needed.
6. Any recorded demo files will be shown in the Launcher tab after selecting the correct Mod.

### Recording a demo with BattleRecorder

For singleplayer or LAN:

1. While in-game, open your console by pressing the \~ key. To close it, press the key again.
2. To record a demo, use this command: demo.recordDemo NAME. You should see recordingDemo in the console if the command is registered correctly.
3. To stop recording, use this command: demo.stopRecording. You should see stoppingRecording in the console if the command is registered correctly. Note that the recording will be stopped automatically when a match ends.
4. Your demos will be found here:   &#x20;Battlefield 2142\mods\\\<MOD>\Demos.

For multiplayer:

{% hint style="info" %}
Currently Reclamation has disabled the option to download recorded demos. Ask the admins in the discord server with the time stamp of the gameplay to obtain the file manually.
{% endhint %}

1. Join a server which has Battlerecorder enabled and properly set up.
2. Once the round has finished go to Community > Battle Recorder and download the demo files under the Bookmark section.
3. After downloaded, select the file in your library and press play.
4. Your demos will be found here:   &#x20;`Documents\Battlefield 2142\Profiles\Default\demos`.
5. Copy the files to `Battlefield 2142\mods\<MOD>\Demos` so that you can view them in BattleDirector.

### Viewing a demo with BattleDirector

1. Start BattleDirector.
2. In the Settings tab, configure, FPS, FOV, Hide Nametags, Hide Huds.
3. In the Launcher tab, select the Mod you used to record the demo.
4. Select the demo you want to view, then click Record New Track.
5. To change the speed at which your demo plays back press the Q key.&#x20;
6. Press “Q” to bring up the play controls.  From here you can also Start or Pause the demo. Unfortunately there is no option to Rewind. DO NOT press the restart button as it will mess up the recording.
7. press the T key to bring up the Camera Rose. You can cycle between players here and also change from free cam or to player cam.
8. Commands:\
   To remove the HUD from your screen while watching a demo (the mini map, and any text on the screen): **renderer.drawHud 0**\
   To put the HUD back on: **renderer.drawHud 1**\
   demo.ShutdownDemo - Stops and closes down current demo run\
   demo.adjustDemoFov - Adjust the DOV while watching a demo. Good FOV for cinematic shots (per HawkeAssult): 40-50
9. Here are some shortcut keys for some quick actions\
   1: pause   \
   2: play @ regular speed   \
   3: play @ 5% speed   \
   4: play @ 25% speed   \
   5: play @ 50% speed   \
   6: play @ regular speed   \
   7: play @ 150% speed   \
   8: play @ 300% speed   \
   Spacebar: cycle forward between players.   \
   Shift + Spacebar: cycle backwards between players.   \
   Right Mouse Button: cycle between free camera and player camera.   \
   Mouse wheel: zoom camera in and out when locked onto a player.   \
   W, A, S, D, Ctrl and Shift: move free camera around map, forward, left, backwards, right, down and up.

### Downloads

{% tabs %}
{% tab title="Downloads" %}
**BF2142 Battle Director 1.6 (5.74 MB)**

{% embed url="https://www.moddb.com/downloads/the-sir-community-bf2-bf2142-battle-director-1" %}

**BF2142 Battle Director 1.7 (20.05 MB)**

{% embed url="https://www.moddb.com/downloads/the-sir-community-battledirector-v1-7" %}
{% endtab %}

{% tab title="Changelogs" %}
N/A
{% endtab %}
{% endtabs %}

### Acknowledgements

Special thanks to

* higuy and HawkeAssault for sharing details on getting demo files working @ [BF2142 Remastered](https://discord.com/invite/nVdDkgA)
* [https://forum.realitymod.com/viewtopic.php?t=94558](https://forum.realitymod.com/viewtopic.php?t=94558)
* [https://forums.bf2s.com/viewtopic.php?id=6845](https://forums.bf2s.com/viewtopic.php?id=6845)
