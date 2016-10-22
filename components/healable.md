# healable

This component makes you heal mobs by smashing items in their face.

## Parameters

* `items: String[] or Object[]` - List of items and their values or just items (unknown default heal value)
    ````json
    {
        "item":"golden_carrot",
        "heal_amount": 4
    }
    ````
## Example

````json
{
    "minecraft:healable":{
        "items": [
        {
          "item": "wheat",
          "heal_amount": 2
        },
        {
          "item": "sugar",
          "heal_amount": 1
        },
        {
          "item": "tile.hay_block",
          "heal_amount": 20
        },
        {
          "item": "apple",
          "heal_amount": 3
        },
        {
          "item": "golden_carrot",
          "heal_amount": 4
        },
        {
          "item": "golden_apple",
          "heal_amount": 10
        },
        {
          "item": "appleEnchanted",
          "heal_amount": 10
        }
      ]
    }
    
}
````