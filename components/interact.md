
# interact

Controls interaction with the entity when right clicked, such as creepers + flint and steel, cow milking, sheep shearing.

## Parameters

* `on_interact: Object` - filters and such to handle when this interact instance should fire 
* `use_item: boolean` - Consume the item used perhaps? true for soup/milking
* `transform_to_item: string` - Change the held item to a new one (bucket -> milk bucket)
* `interact_text: string` - accessibility?
* `event: String` - trigger event
* `target: String` - entity to trigger event on
* `hurt_item: int` - Change item's durability (shears used by shearing sheep)
* `swing: boolean` - arm animation when using?
* `play_sounds: string` - Make a noise when the interaction is performed (cow milking sound)
* `spawn_items: String or Object` -  Spawn in items (wool when shearing sheep), object of `{ "table":"path/to/loottable.json"}`
* `cooldown: float` - time between successive interacts 

## Example
from mushroom_cow

````json
{
    "minecraft:interact":[
      {
        "on_interact": {
          "filters": {
            "other_with_item": "bowl",
            "other_with_families": "player",
            "without_components": "minecraft:transformation"
          }
        },
        "use_item": "true",
        "transform_to_item": "mushroom_stew:0",
        "interact_text": "action.interact.moostew"
      },
      {
        "on_interact": {
          "filters": {
            "other_with_item": "shears",
            "without_components": "minecraft:transformation"
          },
          "event": "become_cow",
          "target": "self"
        },
        "use_item": false,
        "hurt_item": 1,
        "play_sounds": "shear",
        "spawn_items": [
          "red_mushroom",
          "red_mushroom",
          "red_mushroom",
          "red_mushroom",
          "red_mushroom"
        ],
        "interact_text": "action.interact.mooshear"
      },
      {
        "on_interact": {
          "filters": {
            "other_with_item": "bucket:0",
            "other_with_families": "player"
          }
        },
        "use_item": "true",
        "transform_to_item": "bucket:1",
        "play_sounds": "milk",
        "interact_text": "action.interact.milk"
      }
    ]
}
````

from sheep.json (showing dropping items)

````json
{
    "minecraft:interact": [
        {
          "cooldown": 2.5,
          "use_item": false,
          "hurt_item": 1,
          "spawn_items": { "table": "loot_tables/entities/sheep_shear.json" },
          "play_sounds": "shear",
          "interact_text": "action.interact.shear",
          "on_interact": {
            "filters": {
              "other_with_item": "shears",
              "other_with_families": "player",
              "with_components": "minecraft:is_dyeable",
              "without_components": "minecraft:is_baby"
            },
            "event": "minecraft:on_sheared",
            "target": "self"
          }
        }
      ]
}

````