# Switch Component

A Switch is a User Interface two-state toggle component that can select between two options. The user may drag the "thumb" back and forth to choose the selected option, or simply tap to toggle as if it were a checkbox. \(Tutorial s_ource can be downloaded from _[_HERE_](http://AppyBuilder.com/tutorials/switch/Tut_Switch.aia)_.\)_

![](/assets/tutSwitch3.png)

![](/assets/tutSwitch1.png)

This component includes Designer properties that allows for changing the default Text, TrackColor, ThumbColor, etc. It also includes blocks and events for capturing user clicks. Using the Click event, allows you to change properties such as Text, and Thumb/Track colors:

![](/assets/tutSwitch5.png)

To implement the logic, we use blocks shown below. The Click event-block is used to capture taps. The Checked block is used to determine the Switch state \(checked or not checked\). IF -ELSE control-block is used to change Text, ThumbColor and TrackColor:![](/assets/tutSwitch4.png)

