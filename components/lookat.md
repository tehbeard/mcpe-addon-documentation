
# lookat

Make entity interact when looked at?

## Parameters

* `searchRadius: int` - How far to look for lookers
* `setTarget: boolean` - Set the entity looking at us as our target
* `filters: Object` - Limit what kind of entity we want to trigger on.

## Example
Enderman.json, target entities that look at us who are players, but not wearing pumpkins

````json
{
    "minecraft:lookat":{
      "searchRadius": 16,
      "setTarget": true,
      "filters": {
        "other_with_families": "player",
        "other_without_armor": [
          "pumpkin",
          "lit_pumpkin"
        ]
      }
    }
}
````
