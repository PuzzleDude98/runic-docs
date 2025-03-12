---
title: Action On RuneUse (Rune Types)
date: 2025-03-08
---

# Action On Rune Use

[Rune Type](../rune_types.md)

Executes a [Block Action Type](../block_action_types.md) and/or [Item Action Types](../item_action_types.md) when the player that has the power "uses" (right-clicks) a block.

Type ID: `action_on_block_use`


### Key Terms
Key terms used when describing fields

| Term    | Type   | Definition                |
| ------- | ------ | ------------------------- |
| `actor` | Entity | The entity using the rune |


### Fields

| Field                | Type                                                                  | Default                                            | Description                                                                                                                                                              |
| -------------------- | --------------------------------------------------------------------- | -------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `entity_action`      | [Entity Action Type](../entity_action_types.md)                       | _optional_                                         | If specified, this entity action type will be executed on the `actor` if all conditions are met.                                                                         |
| `entity_condition`     | [Entity Condition Type](../entity_condition_types.md)              | *optional*                                         | If specified, only execute the specified actions if this condition is fulfilled by the `actor`.                                                                          |
| `block_action`       | [Block Action Type](../block_action_types.md)                         | _optional_                                         | If specified, the used rune will run this action if all conditions are met.                                                                                              |
| `item_condition`     | [Item Condition Type](../item_condition_types.md)                     | _optional_                                         | If specified, only execute the specified actions if this condition is fulfilled by the item in the `actor`'s specified hand(s) determined by the `"hands"` string field. |
| `directions`         | [Array](../data_types/array.md) of [Strings](../data_types/string.md) | `["north", "east", "south", "west", "up", "down"]` | If specified, only execute the specified actions if the `actor` used the specified face of the rune.                                                                     |
| `hands`              | [Array](../data_types/array.md) of [Strings](../data_types/string.md) | `["off_hand", "main_hand"]`                        | Determines if the rune should be activated if the `actor` used the specified hand(s). Accepts `"off_hand"`, `"main_hand"` or both.                                       |
| `result_stack`       | [Item Stack](../data_types/item_stack.md)                             | _optional_                                         | If specified, gives the item to the `actor`.                                                                                                                             |
| `held_item_action`   | [Item Action Type](../item_action_types.md)                           | _optional_                                         | If specified, this action will be executed on the item used by the `actor` to interact with the rune, in the specified hand(s) determined by the `hands` string field.   |
| `result_item_action` | [Item Action Type](../item_action_types.md)                           | _optional_                                         | If specified, this action will be executed on the item that is given to the `actor`.                                                                                     |
| `action_result`      | [Action Result](../data_types/action_result.md)                       | `"success"`                                        | Determines the result of the 'use' action.                                                                                                                               |


### Examples

```json
{
    "type": "action_on_rune_use",
    "block_action": {
        "type": "explode",
        "power": 5,
        "destruction_type": "none",
        "create_fire": false
    },
    "entity_condition": {
        "type": "on_fire"
    }
}
```

This example will cause the rune to explode when interacted with by a player that is on fire.
