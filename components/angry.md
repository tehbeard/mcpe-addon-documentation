# Angry

This component seems to be tied to mob "angriness" and swarm behaviours, such as silverfish, enderman and cave spiders?

## Parameters

* `duration: int` - number of ticks to be angry once triggered?
* `broadcastAnger: boolean` - Trigger anger in other nearby mobs?
* `broadcastRange: int` - range in pixels? to broadcast to
* `calm_event: Object` - Settings for event to trigger when mob is no longer angry
    ````json
    {
        "event": "event_name",
        "target": "self"
    }    

## Example

````json
{
    "minecraft:angry":{
      "duration": 25,
      "broadcastAnger": true,
      "broadcastRange": 20,
      "calm_event": {
        "event": "minecraft:on_calm",
        "target": "self"
    }
}
````