# Breathable

This component allows an entity to breathe underwater

## WARNING: NON-STANDARD FORMAT?
The format of this component is inconsistent with other components, 
it does not follow the standard `minecraft:component` format!!
This may be just data entry on Mojang's part for guardians.

## Parameters

* `totalSupply: int` - Amount of air time for entity when it can't breathe before it suffocates
* `suffocateTime: int` - When the entity suffocates?
* `breathesWater: Boolean` - Sets if the entity can breathe underwater
* `breathesAir: Boolean` - Sets if the entity can breathe air

## Example

````json
{
    "breathable":{
        "breathesWater": true
    }
}
````