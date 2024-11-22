---
title: Home
date: 2024-11-19
---

# Welcome to the Runics documentation!

Runics is a theoretical magic system that has not been programmed yet. This documentation is a fork of Origins mod docs, which runics is currently based off of.

Much of these docs are unchanged and still hold information for Origins. This is all a work in progress, pages will be updated as I figure out more about this mod.

namespace = `runics`

Visit [CurseForge](https://www.curseforge.com/minecraft/mc-mods/origins) or [Modrinth](https://modrinth.com/mod/origins) to learn more about the Origins mod!

> While all information on these docs is currently theoretical, information stated in these blocks should be noted as even more so. they are tentative ideas that may not have any significance in the final version.

## General information

- Most powers are now configurable via data packs. You can also add new powers, as well as new origins, via data packs. This wiki should help you as a reference for everything important, and will maybe contain a few useful tutorials in the future.
- You are welcome to join the [Origins Discord server](https://discord.gg/4mTMHu3) if you want to talk about the mod, making data packs or add-ons for the mod, or to discover servers which use the mod which are sometimes advertised there.
    - If you've been banned from the Discord server, and believe it was unjust, you can appeal the ban by [filling out this form](https://forms.gle/JnoxrTFDXXNws6qx7).
- What is considered "meat" is defined via a tag (`origins/tags/items/meat.json`), so you can add modded foods in there if you want. Avians can eat all food items that are not in the meat tag. However, if the mod correctly defines the food component as meat in code, it should work out of the box.
- You can add food to the tag `origins/tags/items/ignore_diet.json` if you want it to be edible by both vegetarians and carnivores.
- Blocks which are not passable for Phantoms include bedrock, obsidian and crying obsidian. You can change this via a tag as well (`origins/tags/blocks/unphasable.json`).
- For the Feline and Shulk, blocks which are considered "natural stone" are also defined via a tag (`origins/tags/blocks/natural_stone.json`). By default, it includes Stone, Diorite, Andesite, Granite, Netherrack, Blackstone, Basalt and all kinds of natural Sandstone.
- There is an "Orb of Origin" item available in the creative menu. It's a consumable that allows players to change their origin. If you want this to be obtainable in survival, add a crafting recipe via a data pack.

## Helpful links

* [Example data packs](https://github.com/apace100/origins-example-packs)
* [Minecraft Wiki: Data Pack](https://minecraft.wiki/w/Data_Pack)
* [Minecraft Wiki: Creating a data pack](https://minecraft.wiki/w/Tutorials/Creating_a_data_pack)
* [Video Tutorial for creating custom origins with data packs by CandyCaneCazoo](https://www.youtube.com/watch?v=jId0Fw4w2PQ)
