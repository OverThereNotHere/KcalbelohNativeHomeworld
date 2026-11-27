# Kcalbeloh Native Homeworld

Made with irritaion at the funkiness in the KSC Scene related to entirely broken day/night and having Kerbin inside the accretion disk (among other nuisances).

## What's this about?

Kcalbeloh’s `DistanceFactor = 0` mode puts the stock solar system in orbit around the Kcalbeloh black hole instead of having the entire Kcalbeloh system be entirely seperate. The original setup moves Kerbin into its intended orbit after it spawns, this fixes is to just spawn it there in the first place.

## What does it do?

This ModuleManager patch lets Kopernicus load Kerbin directly in its orbit around Kerbol using the better homeworld reparenting added in Kopernicus 255 instead of the older workaround way. It moves the parent and any semimajor-axis override from `PostSpawnOrbit` into Kerbin’s regular `Orbit` node, then removes `PostSpawnOrbit`. The patch activates only in zero-distance mode with Home Switch off and doesn't effect anything when `DistanceFactor` is anything other than `0`.

## Install

Requires Kcalbeloh System, ModuleManager, and Kopernicus release 255 or later. Tested in-game with release 256.

1. Place `KcalbelohNativeHomeworld` in `GameData`. That's it!
2. For the patch to serve its purpose, in `GameData/KcalbelohSystem/Kcalbeloh System Settings.cfg`, set `DistanceFactor = 0` and make sure `HomeSwitch = False`.

Remove the `KcalbelohNativeHomeworld` folder to restore Kcalbeloh’s original reparenting behavior. Set `DistanceFactor` back to `1` to restore the default system layout.

The migration follows [Alternis Kerbol Rekerjiggered 2.7.1](https://github.com/WhirligigGirl/Alternis-Kerbol-Rekerjiggered/releases/tag/2.7.1).

Licensed under the [GNU GPL v3](LICENSE).
