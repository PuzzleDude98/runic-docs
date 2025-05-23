---
title: Meta Condition Types
date: 2025-03-14
---

# Meta Condition Types

Meta Condition Types are implemented for all types of conditions. They basically combine or modify other conditions. The conditions which are modified have to be of the type the field of the meta condition requires. For example, if you have a field which requires an [Entity Condition Type](entity_condition_types.md) and you insert an [And (Meta Condition Type)](meta_condition_types/and.md), the condition types you need to provide inside that condition type will have to be an [Entity Condition Type](entity_condition_types.md) as well.


### List

* [And](meta_condition_types/and.md)
* [Chance](meta_condition_types/chance.md)
* [Constant](meta_condition_types/constant.md)
* [Not](meta_condition_types/not.md)
* [Or](meta_condition_types/or.md)

## Bi-entity Conditions

* [Actor Condition](bientity_condition_types/actor_condition.md)
* [Both](bientity_condition_types/both.md)
* [Either](bientity_condition_types/either.md)
* [Invert](bientity_condition_types/invert.md)
* [Target Condition](bientity_condition_types/target_condition.md)
* [Undirected](bientity_condition_types/undirected.md)

## Block Conditions

* [Offset](block_condition_types/offset.md)
