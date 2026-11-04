Gauntlet: Dark Legacy - PC port
================================


you will need the iso file to run the game :Gauntlet - Dark Legacy (Revision 1)
Start "Gauntlet Launcher.exe", choose your settings and press PLAY.

Files
  Gauntlet Launcher.exe   settings + start the game
  game.exe                the game (can also be started directly)
  SDL2.dll                audio
  vcruntime140.dll        Visual C++ runtime
  *.iso                   your Gauntlet: Dark Legacy (USA) disc image

Game disc
  The launcher uses the .iso in this folder. To use one elsewhere, press
  "Browse..." next to "Game disc" and pick it.

Controls (keyboard; gamepads also work, controllers 2-4 = players 2-4)
  WASD / arrows   move            Space   A (attack)
  Enter           Start           X       B (back / close scrolls)
  C / V           X / Y           Q / E   L / R          Z   Z
  Esc             pause and ask "Quit the game?" (Yes quits, No resumes)

Saves go to saves\card_a (Dolphin-compatible .gci files).
Settings are kept in launcher.ini; the last run's log is game.log.

Command line (game.exe): --res 1920x1080 --fps60 --widescreen --fullscreen
                         --msaa 4 --iso "D:\path\game.iso"
"Gauntlet Launcher.exe --play" starts the game with the saved settings.

Online play (2-4 players over the internet or a home network)
-------------------------------------------------------------
Everyone needs this same folder: the same game.exe and the same disc image.
Each PC controls one player (keyboard or first gamepad); in the game, press
Start to join as usual. The host is player 1, joiners get players 2-4.

Host
  1. Launcher -> Online: "Host a game". Set Players (2-4); Port 7777 is fine.
  2. Press PLAY. The window title says "waiting for players" until everyone
     has joined; then the game starts on all PCs at once.
  3. The first time, Windows Firewall asks about game.exe: tick both Private
     and Public networks and press Allow.
  4. Tell the other players which address to type:
     - Same house / same Wi-Fi: the address the launcher shows ("Friends join:").
     - Over the internet, either
       a) forward TCP port 7777 on your router to this PC (router settings ->
          Port forwarding) and give them your public IP (search the web for
          "what is my IP"), or
       b) easier: everyone installs the same free VPN app (Tailscale, ZeroTier
          or Radmin VPN), joins one network, and they use your VPN IP.

Join
  Launcher -> Online: "Join a game", type the host's address (IP, or IP:port
  if the host changed the port) and press PLAY.

Good to know
  - The host's 60 FPS and 16:9 settings are used by everyone; resolution,
    anti-aliasing and fullscreen are each player's own.
  - The game uses the host's memory card; only the host's saves are kept.
  - Input delay (default 4 frames) hides network lag. If the title often says
    "waiting for other players", raise it; on a fast connection lower it for
    snappier controls. The host's value is used.
  - Esc pauses the game for everyone until you answer.
  - If the title ever shows "DESYNC", the games stopped matching: everyone
    should quit and start the session again.
  - If a player leaves, the others keep playing.
