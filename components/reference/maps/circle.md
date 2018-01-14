# Circle

The Circle component visualizes a circle of a given radius, in meters, at a latitude and longitude. The circle's appearnce can be customized using properties such as FillColor, StrokeColor, and StrokeWidth.

The Circle component can also be used to implement features such as geofencing, a mechanism where the user's presence within an area is used to trigger other behaviors. Using the DistanceToPoint method combined with the LocationSensor, you can determine whether a user's location is inside or outside of the circle. You can use this feature to trigger additional actions.

---

### Properties

#### Description

Sets or gets the description displayed in the info window. The info window appears when the user taps on the circle.

#### Draggable

Sets or gets whether or not the user can drag a map feature. This feature is accessed by long-pressing and then dragging the circle to a new location.

#### EnableInfobox

Enables or disables the infobox window display when the user taps the circle.

#### FillColor

Sets or gets the color used to fill in the circle.

#### Latitude

Sets or gets the latitude of the center of the circle, in degrees. Positive values representing north of the equator and negative values representing south of the equator. To update the latitude and longitude simultaneously, use the SetLocation method.

#### Longitude

Sets or gets the longitude of the center of the circle, in degrees. Positive values representing east of the prime meridian and negative values representing west of the prime meridian. To update the latitude and longitude simultaneously, use the SetLocation method.

#### Radius

Sets or gets the radius of the circle, in meters.

#### StrokeColor

Sets or gets the color used to outline the circle.

#### StrokeWidth

Sets or gets the width of the stroke used to outline the circle.

#### Title

Sets or gets the title displayed in the info window that appears when the user clicks on the map feature.

#### Type

Gets the type of the feature. For Circle, this will always be "Circle".

#### Visible

Sets or gets whether the component should be visible on the screen. Value is true if the component is showing and false if hidden.

---

### Events

#### Click

Runs when the user taps on the circle.

#### Drag

Runs during drag operations.

#### LongClick

Runs after the user long clicks on the circle but does not trigger a drag. Note that this event will only trigger if Draggable is false.

#### StartDrag

Runs before a drag operation begins. Use this to save the current position of the circle, for example.

#### StopDrag

Runs after a drag operation completes. Use this to save the new position of the circle, for example.

---

### Methods

#### DistanceToFeature(component mapFeature, boolean centroids)

Computes the distance between the Circle and the given mapFeature. If centroids is true, the computation is done between the centroids of the two features. Otherwise, the distance will be computed between the two features based on the closest points. Further, when centroids is false, this method will return 0 if the circle intersects or contains the mapFeature. If an error occurs, this method will return -1.

#### DistanceToPoint(number latitude, number longitude, boolean centroids)

Computes the distance between the Circle and the given latitude and longitude. If centroids is true, the distance is computed from the center of the circle to the given point. Otherwise, the distance is computed from the closest point on the circle to the given point. Further, this method will return 0 if centroids is false and the point is in the circle. If an error occurs, -1 will be returned.

#### HideInfobox

Hides the circle's info box if it is visible. Otherwise, no action is taken.

#### SetLocation(number latitude, number longitude)

Moves the center of the circle to the given latitude and longitude. This method is more efficient than setting latitude and longitude separately.

#### ShowInfobox

Shows the info box for the circle if it is not visible. Otherwise, this method has no effect. This method can be used to show the info box even if EnableInfobox is false.
