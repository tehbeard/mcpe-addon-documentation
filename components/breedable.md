# Breedable

This component makes the entity able to make babies

## Parameters

* `requireTame: boolean` - Entity must be tamed before hand (requires: tameable component?)
* `inheritTamed: boolean` - Baby is also tame?
* `breedsWith: Object[]` - list of entities it can breed with, and what that breeding produces
  E.g. for a donkey, breeding with a donkey = a donkey, while breeding with a horse makes a mule instead
  ````json
  [
        {
          "mateType": "minecraft:donkey",
          "babyType": "minecraft:donkey",
          "breed_event": {
            "event": "minecraft:entity_born",
            "target": "baby"
          }
        },
        {
          "mateType": "minecraft:horse",
          "babyType": "minecraft:mule",
          "breed_event": {
            "event": "minecraft:entity_born",
            "target": "baby"
          }
        }
      ]
  ````
* `breedItems: String[]` - List of items that can make the entity go into breeding mode.
* `mutation_factor: Object` - UNKNOWN, found on rabbits
  ````json
  {
     "variant": 0.2
  }
  ````
## Example
From horse.json
````json
{
    "minecraft:breedable":{
      "requireTame": true,
      "inheritTamed": false,
      "breedsWith": [
        {
          "mateType": "minecraft:horse",
          "babyType": "minecraft:horse",
          "breed_event": {
            "event": "minecraft:entity_born",
            "target": "baby"
          }
        },
        {
          "mateType": "minecraft:donkey",
          "babyType": "minecraft:mule",
          "breed_event": {
            "event": "minecraft:entity_born",
            "target": "baby"
          }
        }
      ],
      "breedItems": [
        "golden_carrot",
        "golden_apple",
        "appleEnchanted"
      ]
    }
}
````