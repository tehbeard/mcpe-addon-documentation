
# inventory

Grants the entity an inventory (note: not the creatures equipment inventory it appears, except for horses...)

## Parameters

* `container_type: String` - Type of UI to show for this container 
* `inventory_size: int` - Number of slots for inventory
* `can_be_siphoned_from: boolean` - Allow hopper interaction with inventory
## Example

For chest minecart.

````json
{
    "minecraft:inventory":{
        "container_type": "minecart_chest",
        "inventory_size": 27,
        "can_be_siphoned_from": true
    }
}
````
