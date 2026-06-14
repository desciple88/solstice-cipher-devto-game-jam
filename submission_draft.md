---
title: Solstice Cipher: a light-routing puzzle for the June Solstice Game Jam
published: false
tags: devchallenge, gamechallenge, gamedev, javascript
---

This is a submission for the [June Solstice Game Jam](https://dev.to/challenges/june-game-jam-2026-06-03).

## What I Built

**Solstice Cipher** is a small browser puzzle game about the longest day, code-breaking, and the turning point between signal and shadow.

The player rotates mirrors to route a solstice beam through every cipher node before landing on the final beacon. Each level is a tiny circuit of light: if the beam misses a cipher gate, the beacon does not unlock.

The game is inspired by a few June themes from the challenge prompt:

- the June solstice and the long arc of daylight
- light versus darkness
- turning points
- Alan Turing, code-breaking, and computational thinking

## Demo

Demo video: [demo.mp4](https://github.com/desciple88/solstice-cipher-devto-game-jam/blob/main/demo.mp4)

Playable game: https://desciple88.github.io/solstice-cipher-devto-game-jam/

Source code: https://github.com/desciple88/solstice-cipher-devto-game-jam

## How It Works

The game is a dependency-free HTML/CSS/JavaScript canvas app.

The board is a 6x6 grid. A sunbeam enters from one side of the board, moves in one of four directions, and reflects when it hits a mirror:

- `/` turns east to north, south to west, and so on
- `\` turns east to south, north to west, and so on

Cipher nodes record whether the beam visited them. A level is solved only when the beam has touched all required cipher nodes and then reaches the beacon.

## Controls

- Click or tap a mirror to rotate it.
- Use **Reset** or press `R` to restart the level.
- Use **Next** or arrow keys to switch levels.
- Use **Hint** or press `H` if the path gets stuck.

## Why the Turing Angle

I wanted the Alan Turing category to feel like part of the mechanics, not just a label. The player is effectively debugging a simple signal machine: change one reflector, trace the path, see which gates activated, and iterate until the message resolves.

It is not an Enigma simulator, but it borrows the feeling of signal routing, symbolic gates, and systematic code-breaking.

## What I Used

- HTML
- CSS
- JavaScript
- Canvas 2D
- ffmpeg for the demo capture

AI assistance was used while preparing the implementation and write-up. I am not entering this under the Best Google AI Usage category because I could not complete a real Google AI toolchain step during the build; the local Gemini CLI was unavailable in my environment.

## What I Learned

For a tiny jam game, the best scope was a mechanic that could be understood instantly: rotate mirrors, follow light, unlock the beacon.

The solstice theme gave the visual direction. The Turing theme gave the rules: the path is not just pretty, it has to carry a complete signal.
