---
title: Action On Callback (Rune Type)
date: 2024-11-25
---

# Action On Callback

[Rune Type](../rune_types.md)

Execute [Entity Action Types](../entity_action_types.md) depending on the context.

Type ID: `runics:action_on_callback`

!!! note

    Callbacks may refer to when the player joins the world, when the player leaves the world, or when the player respawns within a radius of the rune.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_action_joined` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the player when joining a world.
`entity_action_left` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the player when leaving the world.
`entity_action_respawned` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the player right after they respawns.
`block_action_joined` | [Block Action Type](../block_action_types.md) | _optional_ | If specified, this action will be executed on the rune when a player is joining a world.
`block_action_left` | [Block Action Type](../block_action_types.md) | _optional_ | If specified, this action will be executed on the rune when a player leaves the world.
`block_action_respawned` | [Block Action Type](../block_action_types.md) | _optional_ | If specified, this action will be executed on the rune right after a player respawns.
`radius` | [Integer](../data_types/integer.md) | `16` | Determines the radius of the area.
`shape` | [Shape](../data_types/shape.md) | `"cube"` | Determines the shape of the area.


### Examples

```json
{
    "type": "origins:action_on_callback",
    "entity_action_chosen": {
        "type": "origins:apply_effect",
        "effect": {
            "effect": "minecraft:luck",
            "duration": 24000
        }
    },
    "execute_chosen_when_orb": false
}
```

This example will give the player the Luck I (30:00) status effect the moment the player has chosen the origin that has the power, unless the player used the Orb of Origin item to choose that origin.
<br>


```json
{
  	"type": "origins:action_on_callback",
  	"entity_action_gained": {
    	"type": "origins:execute_command",
    	"command": "team join TheNetherBoys @s"
  	},
  	"entity_action_lost": {
    	"type": "origins:execute_command",
    	"command": "team leave @s"
  	},
  	"execute_chosen_when_orb": true
}
```

This example will make players automatically join the team called "TheNetherBoys" upon gaining the power, and will make the players also leave automatically if they ever change their origin with another one that doesn't have the power.
(The "TheNetherBoys" team has to exist beforehand for this power to work!)
