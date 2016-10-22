# Ageable

This component controls the age of a mob that may be a "baby"
 
## Parameters

* `duration: int` - time entity is a "baby", a duration of -1 is seen on zombie_pigmen in the baby state.
* `threshold: int` - time entity is a "baby", seems to be used instead of duration in some cases, maybe this is a count up instead of a countdown?
* `feedItems: string` - A single item to feed the entity
* `feedItems: string[]` - A list of items to feed the entity
* `feedItems: object[]` - A list of items in the following format, allowing different items to speed up ageing differently
  ````json
  {
      "item":"sugar",
      "growth": 0.025 
  }
  ````
* `grow_up: object` - Sets which event to fire when the entity ages
    ````json
    {
        "event":"minecraft:event_name_here",
        "target":"self"
    }
    ````
## Example
From mule.json
````json
{
    "minecraft:ageable":{
        "duration": 1200,
      "feedItems": [
        {
          "item": "wheat",
          "growth": 0.016667
        },
        {
          "item": "sugar",
          "growth": 0.025
        },
        {
          "item": "tile.hay_block",
          "growth": 0.15
        },
        {
          "item": "apple",
          "growth": 0.05
        },
        {
          "item": "golden_carrot",
          "growth": 0.05
        },
        {
          "item": "golden_apple",
          "growth": 0.2
        },
        {
          "item": "appleEnchanted",
          "growth": 0.2
        }
      ],
      "grow_up": {
        "event": "minecraft:ageable_grow_up",
        "target": "self"
      }
    }
}
````