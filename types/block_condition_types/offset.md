---
title: Offset (Block Condition Type)
date: 2025-03-11
---

# Offset

[Block Condition Type](../block_condition_types.md)

Checks the provided [Block Condition Type](../block_condition_types.md) at a position offset from the current position.

Type ID: `offset`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`condition` | [Block Condition Type](../block_condition_types.md) | | The condition to check with the given offset.
`x` | [Integer](../data_types/integer.md) | `0` |  How much to offset the position on the x-axis.
`y` | [Integer](../data_types/integer.md) | `0` |  How much to offset the position on the y-axis.
`z` | [Integer](../data_types/integer.md) | `0` |  How much to offset the position on the z-axis.


### Examples

```json
"block_condition": {
    "type": "offset",
    "condition": {
        "type": "block",
        "block": "minecraft:grass_block"
    },
    "y": 1
}
```

This example will check if the block above the block is a Grass Block.
