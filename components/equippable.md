# equippable

This component used by horses for saddles?

## Parameters

* `slots: Object[]` - collection of items that an entity has, and what event to fire when equipped/unequipped.

## Example

````json
{
    "minecraft:equippable":{
        "slots": [
        {
          "item": "saddle",
          "on_equip": {
            "event": "minecraft:horse_saddled"
          },
          "on_unequip": {
            "event": "minecraft:horse_unsaddled"
          }
        }
      ]
    }
    
}
````