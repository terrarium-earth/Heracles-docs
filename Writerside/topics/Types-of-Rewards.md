# Types of Rewards

## Item
Rewards the player with an item. When creating such a reward, the item chooser pop-up allows picking an item from listing of item icons, specifying the item id directly, searching by tags, or using the item currently in the editor's hand.

## Experience
Rewards the player with experience; amount may be specified with units of XP or Levels.

## Loot Table
Loot table must be specified by ID.

## Command
Runs a specified command when the player claims the reward.

## Selectable
Allow the user to choose one of a selection of awards.

> This reward type can only be made be editing the quest json directly. Here's how this would look:
> 
> ```json
> "rewards: {
>   "example select reward": {
>       "type": "heracles:selectable",
>       "amount": 1,
>       "rewards" : {
>           ...
>       }
>   },
>   ...
> }
> ```
> The inner `rewards` key has the same structure as the outer `rewards` key that contains this example `heracles:selectable` reward. It will constitute the list of choices the player may select for this reward.
{style="note"}
