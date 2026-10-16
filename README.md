# RecRunner

Records your games, nothing else. It waits quietly by the clock. While one of your games is running, tap F7 to start and stop a recording, or hold F7 to save the last few minutes as a clip. Recording also starts by itself when one of your games opens (you can switch that off overall or per game). To trim a recording, hover it in the list and click Edit: step through it frame by frame, pick the start and end, choose which sound tracks to keep and save it as a clip (the window can be resized or maximized, and the preview plays with sound). It records just the game's own window - notifications, popups and other windows are not recorded, and your other monitors never are. Only the sounds you pick are recorded: the game's own sound, plus the microphone and apps (like Discord or Spotify) you add in Settings. Settings also has 15 looks to choose from and a switch for the pop-up notices.

It uses your graphics card's own video chip (NVIDIA, AMD or Intel) so games don't slow down, and falls back to the processor if it has to.

> This application is built by AI. I made this for myself and I'm uploading it to GitHub for backup and to share in case anyone can get any use out of it. It's pretty specific to my setup and my needs, but if you can get any use out of it, then enjoy.
>
> Use at your own risk. I offer no warranty or guarantees for this software.

## Download

**Latest version: v1.3** (Oct 16, 2026)

- [RecRunner_v1.3_no-install.zip](https://github.com/codenomics/RecRunner/releases/download/v1.3/RecRunner_v1.3_no-install.zip) - 170 KB
- [RecRunner_v1.3_Setup.exe](https://github.com/codenomics/RecRunner/releases/download/v1.3/RecRunner_v1.3_Setup.exe) - 586 KB
- [RecRunner_v1.3_source.zip](https://github.com/codenomics/RecRunner/releases/download/v1.3/RecRunner_v1.3_source.zip) - 171 KB

What's new in v1.3:

- New Fixed bitrate choice under Quality, so you can set the exact Mbit/s (2 to 150)
- Better picture on computers without a usable graphics card encoder: the processor encoder is now used before Windows' basic built-in one

Older versions are on the [Releases page](https://github.com/codenomics/RecRunner/releases).

## Getting started

### Installer (recommended)

1. Download the file ending in `_Setup.exe` above.
2. Double-click it and click Install. It installs just for you - no admin password needed - and adds Start menu and Desktop shortcuts.
3. To remove it later: Windows Settings > Apps, find RecRunner and click Uninstall.

### No install (portable zip)

1. Download the file ending in `_no-install.zip` above.
2. Right-click it > Extract All, and pick a folder. Don't run it from inside the zip.
3. Open the folder and double-click the app's .exe. Nothing is installed; delete the folder to remove it.

Windows says "Windows protected your PC"? Click More info > Run anyway. It shows that for apps without a paid signing certificate.

## Source code

Want to see how it works, or build it yourself? Download the file ending in `_source.zip` above, extract it and double-click `Build.bat`. It only uses the C# compiler that already comes with Windows, so there is nothing to install.

## More details

```
GETTING STARTED
---------------
Pick one. Both give you the same app.

OPTION 1 - INSTALLER (recommended)
  Download the file ending in _Setup.exe, double-click it and click Install.
  It installs just for you (no admin password) and adds Start menu and
  Desktop shortcuts. Needs Windows 10 (version 2004 or newer) or 11, 64-bit.
  To remove it later: Windows Settings > Apps > RecRunner > Uninstall.

OPTION 2 - NO INSTALL (zip)
  1. Download the file ending in _no-install.zip. Right-click it -> Extract
  All... and put the RecRunner folder somewhere it can stay (for example
  Documents). Don't run it from inside the zip.
  2. Double-click RecRunner.exe. Nothing is installed; to remove it, delete
  the folder (and turn off "Start RecRunner with Windows" first).

EITHER WAY
  1. RecRunner needs FFmpeg 8.1 or newer, a free program that does the
     video work. The first time, click "Get FFmpeg" and RecRunner downloads
     it for you (about 150 MB). Or put your own ffmpeg.exe next to
     RecRunner.exe.
  2. Open the Games tab and add your games: start the game and click
     "Add a running game", or click "Browse for a game" and pick its .exe.

"Windows protected your PC"? Click "More info" -> "Run anyway".
Windows shows that for apps downloaded from the internet that aren't
signed with a paid certificate.


USING IT
--------
- Start one of your games. RecRunner's icon by the clock says it's ready.
- Tap F7 to start recording. Tap F7 again to stop. The icon gets a red dot
  while it records. Closing the game also stops the recording.
- Hold F7 for about half a second to save the last 2 minutes as a clip
  (Videos\RecRunner\Clips). It works whether or not you're recording.
- When none of your games are running, RecRunner ignores F7, so it works as
  normal in every other app.
- Recordings go to Videos\RecRunner as .mp4 files. The Recordings tab lists
  them, clips included: click one to play it, "Show in folder" to find it,
  x to delete it (it goes to the Recycle Bin).

SETTINGS
- Folders: where recordings and clips are saved.
- Frame rate (30, 60, 120 or 144), Quality (Low, Medium, High) and Format:
    H.264  plays everywhere (default)
    HEVC   smaller files
    AV1    smallest files, newest graphics cards only
- Show the mouse pointer, Choose sounds to record (the game's own sound is always on; add a microphone or apps like Discord and Spotify; each gets its own track plus an "Everything mixed" track).
- Hotkey: click the box and press the key you want. Also how many minutes
  holding it saves (1 to 30), or turn that off.
- Drive space: warns when the drive gets low or the recordings take up too
  much room, and can delete the oldest full recordings for you (clips are
  never deleted).
- Start RecRunner with Windows, check for updates.


GOOD TO KNOW
------------
- Overlays that draw inside the game itself (the Steam overlay, sometimes
  Discord's) can still show in the video. Turn them off in Steam or Discord
  for that game if you don't want them.
- If a game runs as administrator, run RecRunner as administrator too, or
  it can't see the game's window or your key presses.
- So it can save the last few minutes, RecRunner records in short pieces
  while a game runs (in a hidden ".recrunner-temp" folder inside your
  recordings folder) and deletes the ones it no longer needs. Your graphics
  card does this work, so games don't slow down. Turn "Hold it to save the
  last ... minutes" off in Settings if you only want to record on demand.
- If the PC stops in the middle of a recording, the next start saves it.
- Updates: about 20 seconds after it starts, RecRunner checks GitHub for a
  newer version (it only reads the public release page; nothing is sent)
  and never interrupts a game. "Check for updates" is in the icon's menu
  and in Settings.
- Settings are kept in %APPDATA%\RecRunner\settings.txt.
- If something goes wrong, RecRunner-log.txt next to RecRunner.exe says what.
- FFmpeg is made by the FFmpeg project (ffmpeg.org). When RecRunner
  downloads it, it also saves FFmpeg's license next to it.
```

