# Entity File format

Each entity is represented by a JSON file 
detailing the construction of that entity using 
components and events.

Components are further broken down into "permanent" components,
always active and component groups, which can be toggled on and 
off by various events and behaviours.

````json
{
    "format_version": 0.1, //Always 0.1, will increment in future probably
    "components":{
        "component_name":{ "param1":"value"}
    }, //A map of components, the key is the component name, and value is the parameters
    "component_groups": { //A group of components, the key is the name for that component group
        "group_name":{
            "component_name":{ "param1":"value"}
        } 
    },
    "events":{ //Ties actions to events
        "event_name":{ //The name of an event
            "event_action":{ //An action to perform for an event
                    "action_param": "value" // A parameter for that event
            }
        }
    }
}
````