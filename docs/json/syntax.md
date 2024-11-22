---
title: JSON Syntax
date: 11-22-2024
---

# JSON Syntax

While JSON represents the runes behind the scenes, runes are drawn in a visually manner in game.
This page basically describes how to translate JSON to runes.


### Syntax

Element  | JSON Syntax | Rune Syntax | Usagee
-------|-----------|-----------|-------------
`Object` | `{}` | Hexagon | Everything inside the brackets is instead places inside the hexagon
`Key` | `"key":` | Line with a circle in the middle | Attaches value to the inner edge of its object. The key type is contained within the circle.
`Value` | `:???` | Varies | A container attached to the end of a key. Can be an object, array, string, or other data type.
`Array` | `tbd` | tbd | 
`String` | `tbd` | tbd | 
`Number` | `tbd` | tbd | 
`Boolean` | `tbd` | tbd | 


### Examples


(not ready yet)
```json
{
    "type": "origins:active_self",
    "entity_action": {
        "type": "origins:execute_command",
        "command": "tellraw @a {\"text\": \"Hello world!\", \"color\": \"green\"}"
    },
    "name": "Hello World!",
    "description": "A power that announces a 'Hello world!' message to everyone in the server.",
    "badges": [
        {
            "sprite": "minecraft:textures/item/diamond.png",
            "text": "Ooh, shiny!"
        }
    ]
}
```

This example will print a green-colored 'Hello world!' message to all currently online players once activated.
