# Entity File format

Each entity is represented by a JSON file 
detailing the construction of that entity using 
components and events.

Components are further broken down into "permanent" components,
always active and component groups, which can be toggled on and 
off by various events and behaviours.
* `minecraft:entity` - Denotes this is entity data
  * `format_version` - The version value for the entity data, used to let the game know what type of data will be found, always 0.1 right now
  * `components` - A key-value set of components, each key is a component name, and the parameters are it's value
  * `component_groups` - A key-value set, denoting groups of components that can be added/removed together
  * `events` - A key-value set of events, containing actions to perform when the event is fired.

````json
{
    "minecraft:entity":{
    "format_version": 0.1,
    "components":{
        "component_name":{ "param1":"value"}
    },
    "component_groups": {
        "group_name":{
            "component_name":{ "param1":"value"}
        } 
    },
    "events":{ 
        "event_name":{ 
            "event_action":{ 
                    "action_param": "value" 
            }
        }
    }
}
}
````
