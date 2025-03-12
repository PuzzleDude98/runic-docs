---
title: Time Of Day (Entity Condition Type)
date: 2025-03-12
---

# Time Of Day

[Entity Condition Type](../entity_condition_types.md)

Checks the current day time ticks of the world.

Type ID: `time_of_day`


### Fields

| Field        | Type                                      | Default | Description                                                                                       |
| ------------ | ----------------------------------------- | ------- | ------------------------------------------------------------------------------------------------- |
| `comparison` | [Comparison](../data_types/comparison.md) | "=="    | Determines how the current day time ticks of the world should be compared to the specified value. |
| `compare_to` | [Integer](../data_types/integer.md)       |         | The value at which the current day time ticks of the world will be compared to.                   |


### Examples

```json
"condition": {
    "type": "and",
    "conditions": [
        {
            "type": "time_of_day",
            "comparison": ">=",
            "compare_to": 12000
        },
        {
            "type": "time_of_day",
            "comparison": "<=",
            "compare_to": 13000
        }
    ]
}
```

This example will check if it's the sun is currently setting.
