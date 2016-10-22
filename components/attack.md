# Attack

This component changes the damage a mob inflicts

## Parameters

* `damage: int` - Damage the mob does (in half-hearts)
* `range_min: int` - Used to make a varying damage per attack (used on iron golems)
* `range_max: int` - Used to make a varying damage per attack (used on iron golems)
* `effect_name: String` - Effect mob applies with damage (used by husks/withers)
* `effect_duration: int` - Duration of effect in seconds?
## Example

````json
{
    "minecraft:attack":{
      "damage": 3,
      "effect_name": "hunger",
      "effect_duration": 30
    }
}
````