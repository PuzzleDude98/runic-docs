---
title: How to use
date: 2025-03-18
---
# Using Runics

Runics currently has no official releases, or any viable user interface. However, some developer builds can be downloaded if you want to try the limited existing features via developer tools. This guide will help you both download and utilize the mod in its current state.

## Downloading the .jar

Builds are stored in the official [Runics Github](https://github.com/PuzzleDude98/Runics) at [build/libs](https://github.com/PuzzleDude98/Runics/tree/main/build/libs)]. Here you can select the most recent .jar and download it. From there it should work like any other fabric mod, simply add to your mod folder with the right dependencies and enjoy! If you do not know how to install a fabric mod, refer to [this guide](https://docs.fabricmc.net/players/installing-mods) for advice. It should be noted that if you do not have existing experience modding, this mod is probably not for you.

### Requirements

Runics is build for minecraft version 1.21.4 and fabric loader 0.16.10. Attempt other versions at your own risk.
The only required dependency for runics is [fabric api](https://modrinth.com/mod/fabric-api) version 0.188.0.


## Usage

Runes are not available in the creative inventory. In order to try them, you must use commands to obtain a `runics:rune` item and place it down. If you right click it with an open hand, you should see the data stored in the rune: `{}`. Runes have no data by default, so writing some should be your next step.

In order to write data to a rune, you need to put it into a config file. Navigate to your `config` folder in your minecraft instance and make a new file called `data.json`. It should contain a single json object defining a single rune. See [Rune Types](../types/rune_types.md) for help. After your rune is defined, all you need to do is right click your rune block while holding a stick, You should receive a confirmation message. If you right click with an empty hand again, you should see the new value of your rune, matching the contents of your `data.json`. Your spell is now ready to be executed.

Eventually, different runes will have different methods of activation. However, this version of runics only has one type: [`action_on_rune_use`](../types/rune_types/action_on_rune_use.md). This means that all runes are triggered the same way: by right clicking it with a blaze rod. When you trigger it, it should evaluate all conditions you have added, and if they clear it will execute your specified action(s). Congratulations! You have experienced everything that this mod has to offer.