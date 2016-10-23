
# leashable

Allows mob to be attached to a leash.

## Parameters

* `soft_distance: int` - Start moving when leash this long?
* `hard_distance: int` - Pull mob harshly when leash this long?
* `max_distance: int` - Break leash at this distance 
* `on_leash: Object` - Event to trigger when leashed
* `on_unleash: Object` - Event to trigger when unleashed

## Example

````json
{
    "minecraft:leashable":{
      "soft_distance": 4,
      "hard_distance": 6,
      "max_distance": 10,
      "on_leash": {
        "event": "minecraft:on_leash",
        "target": "self"
      },
      "on_unleash": {
        "event": "minecraft:on_unleash",
        "target": "self"
      }
    }
}
````
