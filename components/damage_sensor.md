# damage_sensor

This component allows a mob to detect specific damage dealt to it and react (creepers going super-saiyan etc)

## Parameters
**NOTE:** damage_sensor takes an array as it's root, allowing it to have multiple entries. This is used by villagers
to allow them to transform into witches on lightning strikes, or zombies when "bitten".

* `on_damage: Object` - Handles which event to fire, and filtering based on type of damage and fatality
* `deals_damage: boolean` - Does the event still deal damage 

## Example

````json
{
    "minecraft:damage_sensor":[
        {
        "on_damage": {
          "filters": {
            "other_with_families": "lightning"
          },
          "event": "become_witch"
        },
        "deals_damage": false
      },
      {
        "on_damage": {
          "filters": {
            "other_with_families": "zombie",
            "with_damage_fatal": true
          },
          "event": "become_zombie"
        }
      }
    ]
}
````