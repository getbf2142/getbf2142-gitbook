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
Create the `Demos` folder at `Battlefield 2142\mods\<MOD>`.
{% endstep %}

{% step %}
Download and install BattleDirector from [Downloads](battlerecorder-and-battledirector.md#downloads).
{% endstep %}

{% step %}
Read <mark style="color:blue;">Quick Help</mark> in BattleDirector.
{% endstep %}

{% step %}
In <mark style="color:blue;">Settings</mark>, set <mark style="color:blue;">Game</mark> to <mark style="color:blue;">Battlefield 2142</mark> and set <mark style="color:blue;">Game EXE Location</mark> to your BF2142 executable .
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
After the round ends, go to <mark style="color:blue;">Community</mark> > <mark style="color:blue;">Battle Recorder</mark> and download the demo under <mark style="color:blue;">Bookmarks</mark>.
{% endstep %}

{% step %}
Demos are saved to `Documents\Battlefield 2142\Profiles\Default\demos`.
{% endstep %}

{% step %}
Copy them to `Battlefield 2142\mods\<MOD>\Demos` to view in BattleDirector.
{% endstep %}
{% endstepper %}

### Viewing a demo with BattleDirector

{% stepper %}
{% step %}
Start BattleDirector.
{% endstep %}

{% step %}
In <mark style="color:blue;">Settings</mark>, configure <mark style="color:blue;">FPS</mark>, <mark style="color:blue;">FOV</mark>, Hide <mark style="color:blue;">Nametags</mark>, and <mark style="color:blue;">Hide HUD</mark>.
{% endstep %}

{% step %}
Set <mark style="color:blue;">Resolution</mark> and check <mark style="color:blue;">Windowed</mark> if needed.

For full widescreen, add `+widescreen 1` to the second input box (append other flags as needed).
{% endstep %}

{% step %}
In the <mark style="color:blue;">Launcher</mark> tab, select the <mark style="color:blue;">Mod</mark> used to record the demo.
{% endstep %}

{% step %}
Choose the demo and click <mark style="color:blue;">Record New Track</mark>.
{% endstep %}
{% endstepper %}

* Press `Q` to open play controls (Start/Pause, speed control). Note: no rewind. Do not press Restart — it will mess up the recording.
* Press `T` to open the Camera Rose to switch players and toggle between free cam and player cam.
* Commands:
  * Hide HUD: `renderer.drawHud 0`
  * Show HUD: `renderer.drawHud 1`
  * Exit current demo: `demo.ShutdownDemo`
  *   Adjust demo FOV: `demo.adjustDemoFov 90`

      Tip: For cinematic shots, try FOV 40–50.
* Here are some handy shortcut keys for quick control:
  *   Speed

      * 1: Pause
      * 2: Play at normal speed
      * 3: Play at 5% speed
      * 4: Play at 25% speed
      * 5: Play at 50% speed
      * 6: Play at normal speed
      * 7: Play at 150% speed
      * 8: Play at 300% speed


  * Camera & Navigation
    * Spacebar: Cycle forward between players
    * Shift + Spacebar: Cycle backward between players
    * Right Mouse Button: Toggle between free camera and player camera
    * Mouse Wheel: Zoom when locked onto a player
    * W/A/S/D/Ctrl/Shift: Move free camera (forward/left/back/right/down/up)

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
