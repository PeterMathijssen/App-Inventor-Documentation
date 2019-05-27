# Switch

Switch components can detect user taps and can change their boolean state in response. They are identical to Checkboxes except in appearance.

Switches have an on (true) state and an off (false) state. A switch component raises an event when the user taps it to toggle between states.

## Properties

### BackgroundColor
Color for switch background.

### Enabled
If set, user can switch to change state and trigger event.
### Height
Switch height (y-size).
### Width
Switch width (x-size).
### On
True if the switch is in the On state, false otherwise.
### Text
Text to display on switch.
### TextColor
Color for switch text.
### ThumbColorActive
Color of the switch button when the switch is in the On state.
### ThumbColorInactive
Color of the switch button when the switch is in the Off state.
### TrackColorActive
Color of the switch slider when the switch is in the On state.
### TrackColorInactive
Color of the switch slider when the switch is in the Off state.
### Visible
If set, switch is visible.
## Events
### Changed()
User change the state of the switch from On to Off or back.
### GotFocus()
Check box became the focused component.
### LostFocus()
Check box stopped being the focused component.
