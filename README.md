# Arc Cannon

Arc Cannon is a local two-player turn-based artillery duel built with Godot 4.
Players take turns moving a tank, adjusting the cannon angle, charging shot
power, and firing across destructible terrain while wind changes the projectile
arc.

Play it here:

https://nandoyang.github.io/Arc-Cannon/

## Controls

| Action | Keys |
| --- | --- |
| Move left / right | Left Arrow / Right Arrow, or A / D |
| Adjust cannon angle | Up Arrow / Down Arrow, or W / S |
| Charge and fire | Hold Space, then release |
| Restart after game over | R |

## Gameplay

- Player 1 and Player 2 alternate turns.
- Each turn restores the active tank's movement fuel.
- Wind changes every turn and affects projectile flight.
- Holding Space charges shot power.
- Releasing Space fires the active tank's weapon.
- Explosions damage tanks by distance from the impact point.
- Explosions also carve holes into the terrain.
- The match ends when one tank is destroyed. If both tanks are destroyed during
  the same resolution, the match is a draw.

## Tanks

- **Tank A** fires a single heavy shell.
- **Tank B** fires a three-shot burst.

## Build

This repository contains the exported Web build. From the Godot source project,
the Web build can be regenerated with:

```bash
godot4 --headless --path path/to/source-project --export-release Web path/to/pages-repo/index.html
```

The Web export is configured without thread support so it can run on GitHub
Pages without special server headers.

## Status

This is an MVP prototype. The core loop is playable, including movement, aiming,
wind, projectile physics, terrain destruction, damage, turn resolution, and
restart flow.
