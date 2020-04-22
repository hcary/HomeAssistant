# HomeAssistant

alert:

  garage_door_open_long:

    name: Garage Door is still open!
    entity_id: group.all_covers
    state: 'open'   # Optional, 'on' is the default value
    repeat:
      - 30
      - 15
    can_acknowledge: true  # Optional, default is true
    skip_first: True  # Optional, false is the default
    notifiers:
      - mypushover
