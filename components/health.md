# health

This component gives an entity a "health bar"

## Parameters

* `min: int` -  UNKNOWN, found on npc entity
* `max: int` -  max health
* `value: int or Object` - health amount or a range object (as below)

## Example

````json
{
    "minecraft:health":{
        "min":10,
        "max":20,
        "value":{"range_min":15, "range_max":20},
        "value": 18
    }
    
}
````