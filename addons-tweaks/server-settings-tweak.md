# Server Settings Tweak

In-game settings are pretty limited — singleplayer only lets you adjust rounds per map and bot skill. LAN mode offers more, like ticket ratio, friendly fire, and team ratio. But what if you want those options in singleplayer too, or want to change things like man down time and the number of players needed to start?

In this tutorial, we’ll cover how to make all these settings configurable for both singleplayer and multiplayer (LAN). There are several ways to do this, each with its own trade-offs. Just choose the method that works best for you and follow the steps.

### Method 1

**Editing ServerSettings.con in Profiles/Default**

{% hint style="info" %}
Any changes you make with this method will apply to all mods.
{% endhint %}

Whatever you set in `ServerSettings.con` will override any in-game adjustments. For example, if you set the ticket ratio to 100 in the .con file but use the in-game slider to set it to 300, the game or server will still use the value from the .con file.

{% stepper %}
{% step %}
Go into your `Documents/Battlefield 2142/Profiles/Default` folder.
{% endstep %}

{% step %}
Open `ServerSettings.con` with a text editor.
{% endstep %}

{% step %}
Edit your game settings as needed.
{% endstep %}
{% endstepper %}

1.
2.
3.
4. Save the changes.
5. Now, here's the most important part...
   1. Right-click on the `ServerSettings.con` file and select <mark style="color:blue;">Properties</mark>.
   2. At the bottom, check the <mark style="color:blue;">Read-Only</mark> option, then click <mark style="color:blue;">Apply</mark> and <mark style="color:blue;">OK</mark>.

You might wonder why we need to set the .con file to read-only instead of just editing it and leaving it as is. The reason is that BF2142 can be pretty buggy when reading server settings — if you don’t make the file read-only, the game will often overwrite your changes every time you start, and your edits won’t stick. \[[Reference](https://classic-battlefield-modding.fandom.com/wiki/Changing_Ticket_Counts)]

### Method 2

**Editing GameLogicInit.con in mods/\<MOD>**

{% hint style="info" %}
Changes made with this method are specific to each mod.
{% endhint %}

This is my preferred method: just add the settings you want to override to `GameLogicInit.con` — usually the ones you can’t change in-game. For anything you can adjust in-game, just leave it out of this file. The only downside is you might forget what you’ve added, so if you no longer need certain flags, make sure to remove or comment them out.

1. Go into your `mods/<MOD>` folder.
2. Open `GameLogicInit.con` file with a text editor.
3. Append the server settings that you want to the end of the file.
4. Save the changes.

If you don’t need certain settings anymore, just add `rem` at the start of the line to comment it out. For multi-line comments, use `beginrem` and `endrem` to enclose the section you want to disable.

### List of Server Settings

<details>

<summary>TL;DR</summary>

Here are some very frequently used settings that require your attention.

<pre class="language-json"><code class="lang-json">sv.internet 1 // display your server on the server browser
sv.welcomeMessage "Welcome!" // welcome message on loading screen
<strong>sv.numPlayersNeededToStart 1 // fixed the “1 more player to start” issue in LAN games
</strong>sv.spawnTime 10 // the time you have to wait before respawning
sv.manDownTime 10 // the amount of time you can be revived by a medic
sv.ticketRatio 100
sv.teamRatioPercent 100
sv.autoBalanceTeam 0
sv.roundsPerMap 1
sv.useGlobalRank 1
sv.useGlobalUnlocks 1
sv.botSkill 0.2
sv.friendlyFireWithMines 0 // disable friendly fire on mines
</code></pre>

</details>

<table><thead><tr><th width="312">Settings</th><th>Description</th></tr></thead><tbody><tr><td><code>sv.serverName ""</code></td><td>This is the name your server will be listed by in the Internet or LAN server browser.</td></tr><tr><td><code>sv.password ""</code></td><td>If you set a password, players will need to enter it before connecting to your server.</td></tr><tr><td><code>sv.internet 0</code></td><td>Set this to report your server to the Internet server browser list. <strong>1 for Internet, 0 for LAN.</strong></td></tr><tr><td><code>sv.bandwidthChoke 0</code></td><td>This setting controls how much bandwidth (in Kbps) the server can use, so it doesn’t need to constantly poll for bandwidth. It also helps save bandwidth for non-gaming LAN users who want to check email or browse the web. If you set it to 0, there’s no bandwidth limit.</td></tr><tr><td><code>sv.maxPlayers 16</code></td><td>The maximum number of players allowed on your server at once.  This setting also determines whether the 16, 32 or 64 player configuration of maps is used.</td></tr><tr><td><code>sv.allowFreeCam 0</code></td><td>Allow players to use a free-roaming camera while waiting to spawn.  Players can activate this camera using the JUMP key. <strong>1 to enable, 0 to disable.</strong></td></tr><tr><td><code>sv.allowExternalViews 1</code></td><td>Use this to enable or disable the use of 3rd person cameras in vehicles. <strong>1 to enable, 0 to disable.</strong></td></tr><tr><td><code>sv.allowNoseCam 1</code></td><td>Use this to enable or disable the use of nose-cam in certain vehicles. <strong>1 to enable, 0 to disable.</strong></td></tr><tr><td><code>sv.startDelay 2</code></td><td>This is the amount of time in seconds players are kept waiting for the game to start, once the minimum number of players has been reached.</td></tr><tr><td><code>sv.endDelay 10</code></td><td>This is the amount of time in seconds between when a round ends and a new round begins.</td></tr><tr><td><code>sv.spawnTime 15</code></td><td>This is the amount of time in seconds that players will wait to spawn in the game again after being killed.</td></tr><tr><td><code>sv.manDownTime 15</code></td><td>This is the amount of time players will wait to spawn in the game again after being incapacitated and able to be revived by a medic.</td></tr><tr><td><code>sv.ticketRatio 100</code></td><td>You can set the percentage of the normal number of tickets you wish to use.</td></tr><tr><td><code>sv.roundsPerMap 1</code></td><td>Set the number of rounds to complete before the map automatically changes to the next on the list.</td></tr><tr><td><code>sv.timeLimit 0</code></td><td>After this amount of time is reached, the round will end.</td></tr><tr><td><code>sv.soldierFriendlyFire 100</code></td><td>This is the percentage of direct damage that soldiers will receive from other players on the same team.</td></tr><tr><td><code>sv.vehicleFriendlyFire 100</code></td><td>This is the percentage of direct damage that vehicles will receive from other players on the same team.</td></tr><tr><td><code>sv.soldierSplashFriendlyFire 100</code></td><td>This is the percentage of splash damage that soldiers will receive from other players on the same team.</td></tr><tr><td><code>sv.vehicleSplashFriendlyFire 100</code></td><td>This is the percentage of splash damage that vehicles will receive from other players on the same team.</td></tr><tr><td><code>sv.voteTime 60</code></td><td>This is the amount of time that a poll such as a kick vote or map vote stays open.</td></tr><tr><td><code>sv.minPlayersForVoting 2</code></td><td>This is the minimum number of votes needed for a poll to be sucessful.</td></tr><tr><td><code>sv.autoRecord 0</code></td><td>Enable or disable automatic demo recording.  Turning on this feature will seriously impact your server’s performance. <strong>1 to enable, 0 to disable.</strong></td></tr><tr><td><code>sv.demoDownloadURL ""</code></td><td>If demo recording is enabled, this should be set to the publicly accessible URL where the demo files can be downloaded.</td></tr><tr><td><code>sv.autoDemoHook ""</code></td><td>This is the application or script that is called on to manage demo recordings at the end of rounds.</td></tr><tr><td><code>sv.adminScript ""</code></td><td>Set the path to a custom admin script to run.</td></tr><tr><td><code>sv.hitIndicator 1</code></td><td>Toggles whether or not players receive crosshair feedback indicating they have hit a target. <strong>1 to enable, 0 to disable.</strong></td></tr><tr><td><code>sv.numPlayersNeededToStart 1</code></td><td>The minimum number of players needed for a round to begin.  Until this number of players have joined, the server stays in a pre-game state and neither team loses any tickets.</td></tr><tr><td><code>sv.tkPunishEnabled 1</code></td><td>Enable the system through which players can punish teamkillers in an attempt to kick them from the server. <strong>1 to enable, 0 to disable.</strong></td></tr><tr><td><code>sv.tkNumPunishToKick 3</code></td><td>When punishing is enabled, this sets the number of punished teamkills required to be kicked from the server.</td></tr><tr><td><code>sv.tkPunishByDefault 1</code></td><td>This sets whether or not a player is automatically punished for a teamkill. <strong>1 to enable, 0 to disable</strong></td></tr><tr><td><code>sv.voipEnabled 1</code></td><td>Enable the use of VOIP for squad communication.  **Please see the readme.txt file for more information about this feature. <strong>1 to enable, 0 to disable</strong></td></tr><tr><td><code>sv.voipServerRemote 0</code></td><td>Enable the use of an external BF2142 VOIP Server, thereby disabling the integrated VOIP server.</td></tr><tr><td><code>sv.voipServerRemoteIP "127.0.0.1"</code></td><td>When using an external VOIP server, this should be set with it's IP address.</td></tr><tr><td><code>sv.voipServerPort 55125</code></td><td>The VOIP server uses this port to receive BF2142 server data.  When using an external VOIP server, this should be set to the port associated with the shared password from the VOIP server's configuration.</td></tr><tr><td><code>sv.voipBFClientPort 55123</code></td><td>This is the port the BF2142 client uses for communication with the voip server.</td></tr><tr><td><code>sv.voipBFServerPort 55124</code></td><td>The BF2142 server uses this port to communicate with the VOIP server.</td></tr><tr><td><code>sv.voipSharedPassword ""</code></td><td>When using an external VOIP server, this should be set to the password associated with the VOIP Server port from the VOIP server's configuration.</td></tr><tr><td><code>sv.voipQuality 5</code></td><td>Use this to adjust the quality of VOIP audio.  Raising the quality level will increase the amount of bandwidth your server uses.  Recommended settings are 5 for LAN and 3 for Internet.</td></tr><tr><td><code>sv.gameSpyPort 29900</code></td><td>Your server sends information about settings and status through this port.  You only need to change this if it is in conflict with another port being used on your system.  For best results, this value should stay between 29900 and 29950.</td></tr><tr><td><code>sv.allowNATNegotiation 0</code></td><td>Allow Network Address Translation negotiation.  Try this if you use a router or gateway device and are having problems hosting a server. <strong>1 to enable, 0 to disable.</strong></td></tr><tr><td><code>sv.autoBalanceTeam 1</code></td><td>Enabling this will automatically move players to the team with less players when they die, and will prevent players from switching teams if it would cause them to be too unbalanced. <strong>1 to enable, 0 to disable.</strong></td></tr><tr><td><code>sv.teamRatioPercent 100</code></td><td>This ratio represents how autoBalanceTeam considers the desired ratio between team 1 and team 2.  The percent represents what percent of team 1's current players is considered 'even' for team 2. Team 1 is usually PAC, Team 2 is EU.</td></tr><tr><td><code>sv.sponsorLogoURL ""</code></td><td>Enter a URL to an image, and it will be displayed in the server browser when the server is highlighted.  The image must be in PNG or JPG format, and should have a 4:1 aspect ratio for best results.</td></tr><tr><td><code>sv.punkBuster 0</code></td><td>Enable PunkBuster automatic cheat protection. <strong>1 to Enable, 0 to disable.</strong></td></tr><tr><td><code>sv.useGlobalRank 1</code></td><td>This setting toggles whether or not players can use and show their official rank they have earned by playing on ranked servers. <strong>1 to enable, 0 to disable.</strong></td></tr><tr><td><code>sv.useGlobalUnlocks 1</code></td><td>This setting toggles whether or not players can use the unlocks they have earned by playing on ranked servers. <strong>1 to enable, 0 to disable.</strong></td></tr><tr><td><code>sv.welcomeMessage ""</code></td><td>This text is displayed on the map load screen when connecting to the server.</td></tr><tr><td><code>sv.serverIP ""</code></td><td>This setting allows you to set the network IP address for your server.  This setting needs to match the interface IP setting.</td></tr><tr><td><code>sv.serverPort 17567</code></td><td>This setting allows you to customize the port used for gameplay network traffic.</td></tr><tr><td><code>sv.votingEnabled 1</code></td><td>Enable or disable voting. <strong>1 to enable, 0 to disable.</strong></td></tr><tr><td><code>sv.communityLogoURL ""</code></td><td>Enter a URL to an image, and it will be displayed in the loading screen when connecting to the server.  The image must be in PNG or JPG format, and should have a 4:1 aspect ratio for best results.</td></tr><tr><td><code>sv.customMapURL ""</code></td><td>This setting only applies when running custom maps. The user is redirected to this URL when he/she tries to join a map that the user doesn't have. When this field is empty, they are redirected to bfeditor.org where the game tries to find the map name.</td></tr><tr><td><code>sv.demoQuality 1</code></td><td>Set the quality of demo recording, if enabled, on the server.</td></tr><tr><td><code>sv.endOfRoundDelay 15</code></td><td>This is the amount of time in seconds that the message stating which team won is displayed at the end of the round.</td></tr><tr><td><code>sv.notEnoughPlayersRestartDelay 5</code></td><td>When the number of players on the server drops below the number of players needed to start, the server will wait for this number of seconds for more players to join.  If no players join within this time, the round will end.</td></tr><tr><td><code>sv.interfaceIP ""</code></td><td>This setting allows you to set the network interface IP address for your server.  This setting needs to match the "serverIP" setting.</td></tr><tr><td><code>sv.numReservedSlots 0</code></td><td>Set the number of player slots that will be reserved for the player names defines in ReservedSlots.con.</td></tr><tr><td><code>sv.friendlyFireWithMines 0</code></td><td>Turn this setting off to prevent friendly mines and claymores from detonating when teammates go over them. This setting only works on unranked servers, it's always off on ranked servers. <strong>1 to enable, 0 to disable.</strong></td></tr><tr><td><code>sv.TeamVoteOnly</code></td><td>This option will restrict all voting queries and responses to members of the same team.</td></tr><tr><td><code>sv.botSkill 0.5</code></td><td>Sets the bot skill level for coop.</td></tr><tr><td><code>sv.maxRank 0</code></td><td>Enables/disables the rank restriction on a ranked server.</td></tr><tr><td><code>sv.minUnlockLevel 0</code></td><td>Grants every player unlocks up to this level.</td></tr><tr><td><code>sv.maxUnlockLevel -1</code></td><td>Restricts players so that they can't use unlocks above this level.</td></tr><tr><td><code>sv.allowSpectators 0</code></td><td>Allows/disallows spectators on unranked servers. <strong>1 to enable, 0 to disable.</strong></td></tr><tr><td><code>sv.allowTitanMovement 1</code></td><td>Allows/disallows the commander's ability to move the titan around the battlefield. <strong>1 to enable, 0 to disable.</strong></td></tr></tbody></table>

The list above isn’t complete — some settings aren’t shown because they’re deprecated, only available on ranked servers, or not useful for regular gameplay.
