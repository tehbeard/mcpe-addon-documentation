# Boostable

This component speeds up an entity when a boost item is used (such as the carrot on a stick on a pig)

## Parameters

* `speed_multiplier: int` - Increase speed by this multiplier
* `duration: int` - how long speed is increased (seconds?)
* `boost_items: Object[]` - List of items that can cause the boost
    ````json
    {
        "item":"itemanme",
        "item_damage":2, 
        "replaceItem": "new_item_when_broken"
    }

## Example
From pig.json
````json
{
    "minecraft:boostable":{
      "speed_multiplier": 2,
      "duration": 3,
      "boost_items": [
        {
          "item": "carrotOnAStick",
          "item_damage": 2,
          "replaceItem": "fishing_rod"
        }
      ]
    }
}
````