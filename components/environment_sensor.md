# environment_sensor

This component allows a mob to detect specific damage dealt to it and react (creepers going super-saiyan etc)

## Parameters
**NOTE:** environment\_sensor *MAY* take an array as it's root, allowing it to have multiple entries. 
This is speculated based on damage\_sensor but has not been seen in any vanilla data.

* `on_environment: Object` - Handles which event to fire, and filtering based on environmental conditions

## Example

````json
{
    "minecraft:environment_sensor":{
        "on_environment": {
          "filters": {
            "with_environment_any": "brightness_greater:0.49"
          },
          "event": "minecraft:become_neutral"
        }
      }
    
}
````