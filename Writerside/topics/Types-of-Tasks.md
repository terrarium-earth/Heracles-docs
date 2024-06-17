# Types of Tasks

Heracles has several task types:

- Changed Dimension
- Structure
- Experience
- Dummy*
- Entity Integration
- Biome
- Item Interaction
- Block Interaction
- Kill Entity
- Acquire Item
- Advancement
- Recipe
- Check
- Stat

> By design, the `dummy` task is un-completable. It is meant for halting the players progress along a quest line until its quest is completed for the player by [command](Commands.md).
>
{style="warning"}

> If the object you want to require with a task needs some NBT data to specify it correctly, you can do so by editing the quest's underlying json file directly.
> 
> Here is an example of an Entity Interaction task that needs a Taiga type villager with a Cleric profession to complete:
> 
> ```json
>     "traderjoe": {
>      "type": "heracles:entity_interaction" 
>      "entity": "minecraft:villager",
>      "nbt": {
>        "VillagerData": {
>          "profession": "cleric",
>          "type": "taiga"
>        }
>      },
>    }
> ```
>
{style="tip"}

> There is one more task type, `heracles:composite`, that must be specified by editing a quest's json file directly. Such a task will complete when any _X_ of its child tasks are complete (where _X_ is specified with the json key "amount")—but currently there are restrictions on the set of child tasks it can have.
>
{style="note"}
