# BLIKSEM for Omarchy

A DI.fm player on an amber CRT, with a lightning bolt on your bar. Curved glass, phosphor glow, VGA font, foul language.

You need a DI.fm premium listen key.

## Install

```sh
omarchy plugin add https://github.com/projectmushroom/omarchy-bliksem.git --enable
```

Then click the bolt, paste your key into `key>` with `Ctrl+V`, press `Enter`, and pick a channel.

## On the bar

| | |
|---|---|
| Click | open or hide the player |
| Middle click | play or stop |
| Scroll | hop channels |
| Right click | like the track |

The music keeps playing when the window is closed. Media keys and Omarchy's media widget work too.

## In the player

| | |
|---|---|
| `Space` | play or stop |
| `↑` `↓` | hop channels |
| `F` | fullscreen, `Esc` to leave |
| `Ctrl` `+` `-` `0` | zoom |
| `Ctrl` `L` | like the track |
| `Ctrl` `F` | find a channel |
| `Ctrl` `1`-`9` | favourites, then most played |
| `Ctrl` `Q` | quit |

DI allows one stream per key and the newest connection wins, so another device on your key will kick this one. BLIKSEM reconnects once, then tells you, rather than fighting it.

Your key and history are in `~/.config/bliksem/state.json`, readable only by you. Removing the plugin leaves them there.

## Update and remove

```sh
omarchy plugin update projectmushroom.bliksem
omarchy plugin disable projectmushroom.bliksem
omarchy plugin remove projectmushroom.bliksem
```

## What's in here

`bin/bliksem` is a prebuilt x86_64 Linux program, built from a separate private source repo. Plugins run unsandboxed and so does this, so only install it if you trust it. It needs Omarchy 4 with Quickshell plugin support, and `alsa-lib` with `pipewire-alsa`.

The plugin's QML and manifest are MIT, see `LICENSE`. The screen font is the Px437 IBM VGA 9x16 by VileR, under CC BY-SA 4.0, see `FONT-LICENSE.txt`. Compiled-in open source packages are listed in `THIRD-PARTY.txt`. BLIKSEM is an unofficial player and has nothing to do with DI.fm.
