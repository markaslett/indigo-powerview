# Hunter Douglas PowerView Shade Indigo Plugin

This plugin lets you control [Hunter Douglas PowerView][hd_powerview] shades
from the [Indigo Domotics][indigo] home control software.

To use this plugin you will need PowerView motorized shades, the PowerView
hub, and the Indigo software.

## Features

* Automatically discover shades for easy first-time setup
* Adjust shade positions from Indigo-supported keypads
* Adjust shades based on criteria beyond schedules including:
  * Window-open sensors
  * Interior or exterior temperature
  * Sun angle

## Usage Notes

The plugin does not poll the hub, so triggers based on the position (or any
other attribute) of shades or the hub will not execute when you expect.

Polling the hub does not solve this as the hub does not have a long-term
memory of shade positions.  To reliably know the shade positions you need to
move the shade somehow (at least jog it) which shortens the battery life of
the shades.

## Supported Actions

The following Indigo actions are supported:

### Activate Scene

Activate a scene you have created in the PowerView mobile app.  This allows
you to reuse your existing PowerView scenes without having to recreate them in
Indigo.

### Activate Scene Collection

Activate a scene collection you have created in the PowerView mobile app.
This allows you to reuse your existing PowerView scenes collections without
having to recreate them in Indigo.

### Calibrate Shade

Rediscovers the movement limits of the shade.

### Jog Shade

Moves the shade a tiny bit.  This helps you identify which shade the device is
interacting with.

### Set Shade Position

Set the shade position of an individual shade.  This allows you to set the top
and bottom positions of a shade for a top-down, bottom-up shade or the shade
position for a single-direction shade.

## See also

Hunter Douglas doesn't seem to have documentation for the hub API so please
see the unofficial [PowerView Hub API][hub_api]

[hd_powerview]: https://www.hunterdouglas.com/operating-systems/powerview-motorization
[indigo]: http://www.indigodomo.com
[hub_api]: PowerView+API.md
