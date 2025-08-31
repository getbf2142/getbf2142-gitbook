---
icon: clapperboard-play
---

# BattleRecorder & BattleDirector

Imagine reliving your most epic Battlefield 2142 moments, but from a whole new perspective! BattleRecorder, a fantastic built-in feature, lets you do just that — you can rewatch your past games from a thrilling third-person view. And to dive into those awesome recordings, all you need is BattleDirector. Get ready to see your battles like never before!

{% hint style="warning" %}
With OpenSpy patches, demo files won’t appear under Community > Battle Recorder in-game.
{% endhint %}

### Preparations

{% stepper %}
{% step %}
Manually create the Demos folder at `Battlefield 2142\mods\<MOD>`.
{% endstep %}

{% step %}
Download and install BattleDirector from [Downloads](battlerecorder-and-battledirector.md#downloads).
{% endstep %}

{% step %}
Read <mark style="color:blue;">Quick Help</mark> in BattleDirector.
{% endstep %}

{% step %}
Set <mark style="color:blue;">Game</mark> to <mark style="color:blue;">Battlefield 2142</mark> and set <mark style="color:blue;">Game EXE Location</mark> to your BF2142 executable in the <mark style="color:blue;">Settings</mark> tab.
{% endstep %}

{% step %}
Recorded demos will appear in the <mark style="color:blue;">Launcher</mark> tab after you select the correct <mark style="color:blue;">Mod</mark>.
{% endstep %}
{% endstepper %}

### Recording a demo with BattleRecorder

For singleplayer or LAN:

{% stepper %}
{% step %}
While in-game, press the `~` key to open the console (press it again to close).
{% endstep %}

{% step %}
To start recording, type `demo.recordDemo NAME` in console and press `Enter`.

You should see `recordingDemo` if it worked.
{% endstep %}

{% step %}
To stop recording, type `demo.stopRecording` in console and press `Enter`.

You should see `stoppingRecording` (it also stops automatically at the end of a match).
{% endstep %}

{% step %}
Find your demos in `Battlefield 2142\mods\<MOD>\Demos`.
{% endstep %}
{% endstepper %}

For multiplayer:

{% hint style="info" %}
Reclamation has disabled in-game demo downloads. Ask the admins on Discord for the file and include the gameplay timestamp.
{% endhint %}

{% stepper %}
{% step %}
Join a server with BattleRecorder enabled and properly configured.
{% endstep %}

{% step %}
After the round ends, go to Community > Battle Recorder and download the demo under Bookmarks.
{% endstep %}

{% step %}
Once downloaded, select the file in your Library and press Play.
{% endstep %}

{% step %}
Demos are saved to: `Documents\Battlefield 2142\Profiles\Default\demos`.
{% endstep %}

{% step %}
Copy them to `Battlefield 2142\mods\<MOD>\Demos` to view in BattleDirector.
{% endstep %}
{% endstepper %}

### Viewing a demo with BattleDirector

1. Start BattleDirector.
2. In the Settings tab, configure, FPS, FOV, Hide Nametags, Hide Huds.
3. Configure <mark style="color:blue;">Resolution</mark>. For full widescreen, add `+widescreen 1` to the second input box (append other flags as needed).
4. In the Launcher tab, select the Mod you used to record the demo.
5. Select the demo you want to view, then click Record New Track.
6. To change the speed at which your demo plays back press the Q key.&#x20;
7. Press “Q” to bring up the play controls.  From here you can also Start or Pause the demo. Unfortunately there is no option to Rewind. DO NOT press the restart button as it will mess up the recording.
8. press the T key to bring up the Camera Rose. You can cycle between players here and also change from free cam or to player cam.
9. Commands:\
   To remove the HUD from your screen while watching a demo (the mini map, and any text on the screen): **renderer.drawHud 0**\
   To put the HUD back on: **renderer.drawHud 1**\
   demo.ShutdownDemo - Stops and closes down current demo run\
   demo.adjustDemoFov - Adjust the DOV while watching a demo. Good FOV for cinematic shots (per HawkeAssult): 40-50
10. Here are some shortcut keys for some quick actions\
    1: pause    \
    2: play @ regular speed    \
    3: play @ 5% speed    \
    4: play @ 25% speed    \
    5: play @ 50% speed    \
    6: play @ regular speed    \
    7: play @ 150% speed    \
    8: play @ 300% speed    \
    Spacebar: cycle forward between players.    \
    Shift + Spacebar: cycle backwards between players.    \
    Right Mouse Button: cycle between free camera and player camera.    \
    Mouse wheel: zoom camera in and out when locked onto a player.    \
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
