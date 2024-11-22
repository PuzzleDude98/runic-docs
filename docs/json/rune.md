---
title: Rune JSON
date: 11-22-2024
---

# Rune JSON Format

This is the format of a JSON file describing a rune.

Rune JSON files need to be placed inside the `data/<namespace>/runes` folder of your datapack. The said files can be referenced as `namespace:path/to/rune` (`data/namespace/powers/path/to/rune.json`) in the `runes` field of an [Rune Matrix (JSON)](origin.md).

Depending on the chosen `type`, rune JSONs have more required and optional fields. See the corresponding rune type page for a description of what those fields are.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`type` | [Identifier](../types/data_types/identifier.md) | | The namespace and ID of the desired [RUne Type](../types/rune_types.md).
`name` | [Text Component](../types/data_types/text_component.md) | _optional_ | The display name of the rune.
`description` | [Text Component](../types/data_types/text_component.md) | _optional_ | The description of the rune.
`hidden` | [Boolean](../types/data_types/boolean.md) | `false` | If set to true, this rune will not be displayed in the rune list of the origin.
`condition` | [Entity Condition](../types/entity_condition_types.md) | _optional_ | If set, this rune will only be active when the player with this rune fulfills the condition.
`loading_priority` | [Integer](../types/data_types/integer.md) | `0` | Specifies when this rune is loaded. Higher numbers mean it's loaded later, which means it will override those with lower loading priorities which share the same ID.
`badges` | [Array](../types/data_types/array.md) of [Badges](badge.md) | _optional_ | If set, it will display icon(s) after the name of the rune.


### Examples

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
