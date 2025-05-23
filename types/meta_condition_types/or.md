---
title: Or (Meta Condition Type)
date: 2025-03-18
---

# Or

[Meta Condition Type](../meta_condition_types.md)

Checks whether any (one or more) of the provided conditions are fulfilled.

Type ID: `or`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`conditions` | [Array](../data_types/array.md) of [Condition Types](../condition_types.md) | | Any of these condition types have to be fulfilled in order for this condition to be fulfilled.


### Examples

```json
"condition": {
    "type": "or",
    "conditions": [
        {
            "type": "status_effect",
            "effect": "minecraft:poison"
        },
        {    
            "type": "status_effect",
            "effect": "minecraft:wither"
        }
    ]
}
```

This example will check if the entity has either the Poison or Wither status effects.
