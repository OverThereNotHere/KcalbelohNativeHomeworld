# Kcalbeloh Native Homeworld

## What's this about?

Kcalbeloh’s `DistanceFactor = 0` mode puts the stock solar system in orbit around the Kcalbeloh black hole. The original setup moves Kerbin into its intended orbit after it spawns. Made with irritaion.

## What does it do?

This ModuleManager patch lets Kopernicus load Kerbin directly in its orbit around Kerbol. It moves the parent and any semimajor-axis override from `PostSpawnOrbit` into Kerbin’s regular `Orbit` node, then removes `PostSpawnOrbit`. The patch activates only in zero-distance mode with Home Switch off.

## Install

Requires Kcalbeloh System, ModuleManager, and Kopernicus release 255 or later. Tested in-game with release 256.

1. Place `KerbinOrbit.cfg` in `GameData/KcalbelohNativeHomeworld/`.
2. In `GameData/KcalbelohSystem/Kcalbeloh System Settings.cfg`, set `DistanceFactor = 0` and `HomeSwitch = False`.

Remove the `KcalbelohNativeHomeworld` folder to restore Kcalbeloh’s original reparenting behavior. Set `DistanceFactor` back to `1` to restore the default system layout.

The migration follows [Alternis Kerbol Rekerjiggered 2.7.1](https://github.com/WhirligigGirl/Alternis-Kerbol-Rekerjiggered/releases/tag/2.7.1).

Licensed under the [GNU GPL v3](LICENSE).
