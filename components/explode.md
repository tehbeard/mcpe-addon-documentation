# explode
*This section sponsered by The Torgue corporation*

KABOOM!

## Parameters

* `fuseLength: int or Object` - HOW LONG UNTIL KABOOM (object is `{range_min: 0.5, range_max:2}` for TNT when detonated by proximity)
* `fuseLit: boolean` - UNKNOWN, MAYBE LETS YOU SWITCH OFF THE BOOM? WHY WOULD YOU DO THAT?! MAYBE IT LETS YOU HIDE THE EXPLOSION UNTIL IT EXPLODES?
* `power: int` - HOW BIG A BOOM DO WE WANT
* `causesFire: boolean` - FLAMES ARE A VITAL PART OF POST-EXPLOSION DESTRUCTION!
## Example
FROM TNT.JSON
````json
{
    "minecraft:explode":{
      "fuseLength": 4,
      "fuseLit": true,
      "power": 4,
      "causesFire": false
    }
    
}
````
FROM TNT.JSON, WHEN EXPLODED BY OTHER EXPLOSIONS
````json
{
    "minecraft:explode":{
      "fuseLength": {
        "range_min": 0.5,
        "range_max": 2
      },
      "fuseLit": true,
      "power": 4,
      "causesFire": false
    }
    
}
````

      
