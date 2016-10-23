
# on_target_escape

Used to trigger event when target is no longer available (used by creeper to stop exploding)

## Parameters

* `event: String` - event to trigger 
* `target: String` - entity to target event on

## Example

````json
{
    "minecraft:on_target_escape":{
        "event": "minecraft:stop_exploding",
        "target": "self"
    }
}
````
