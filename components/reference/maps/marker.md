# Marker

The Marker component indicates points on a Map, such as buildings or points of interest. Markers can be customized in many ways, such as using custom images from the app's assets. Markers can also be created dynamically using the CreateMarker method and configured using the "Any Component" blocks.

---

### Properties

#### AnchorHorizontal

Sets or gets the horizontal offset of the marker center relative to its image. Valid values are 1 (Left), 2 (Right), 3 (Center)

#### AnchorVertical

Sets or gets the vertical offset of the marker center relative to its image. Valid values are 1 (Top), 2 (Center), 3 (Bottom).

#### Description

Sets or gets the description displayed in the info window that appears when the user taps on the marker.

#### Draggable

The Draggable property is used to control whether or not the user can drag the marker by long-pressing and then dragging the marker to a new location.

#### EnableInfobox

Enables or disables the infobox window display when the user taps the marker.

#### FillColor

Sets or gets the color used to fill in the marker. This property only applies for markers using vector image assets, including the default icon.

#### Height

Sets or gets the height of the marker, in pixels.

#### HeightPercent

Sets the height of the marker as a percentage of the screen height.

#### ImageAsset

Sets or gets the image shown for the marker. If set to the empty string "", then the default marker icon will be used.

#### Latitude

Sets or gets the latitude of the marker, in degrees, with positive values representing north of the equator and negative values representing south of the equator. To update the latitude and longitude simultaneously, use the SetLocation method.

#### Longitude

Sets or gets the longitude of the marker, in degrees, with positive values representing east of the prime meridian and negative values representing west of the prime meridian. To update the latitude and longitude simultaneously, use the SetLocation method.

#### StrokeColor

Sets or gets the color used to outline the marker.

#### StrokeWidth

Sets or gets the width of the stroke used to outline the marker.

#### Title

Sets or gets the title displayed in the info window that appears when the user clicks on the marker.

#### Type

Gets the type of the feature. For Marker, this will always be "Marker".

#### Visible

Sets or gets whether the component should be visible on the screen. Value is true if the component is showing and false if hidden.

#### Width

Sets or gets the width of the marker, in pixels.

#### WidthPercent

Sets the width of the marker as a percentage of the screen width.

---

### Events

#### Click

Runs when the user taps on the marker.

#### Drag

Runs continuously while a user is dragging the marker.

#### LongClick

Runs when the user long-clicks on the marker but does not trigger a drag. Note that this event will only run if Draggable is false.

#### StartDrag

Runs before a drag operation begins.

#### StopDrag

Runs after a drag operation completes.

---

### Methods

#### BearingToFeature(component mapFeature, boolean centroids)

Returns the bearing from the Marker to the given mapFeature, in degrees from due north. If the centroids paremter is true, the bearing will be to the center of the map feature. Otherwise, the bearing will be computed to the point in the feature nearest the Marker.

#### BearingToPoint(number latitude, number longitude, boolean centroids)

Returns the bearing from the Marker to the given latitude and longitude, in degrees from due north.

#### DistanceToFeature(component mapFeature, boolean centroids)

Computes the distance between the Marker and the given mapFeature. If centroids is true, the computation is done between the centroids of the two features. Otherwise, the distance will be computed between the two features based on the closest points. Further, when centroids is false, this method will return 0 if the marker intersects or contains the mapFeature. If an error occurs, this method will return -1.

#### DistanceToPoint(number latitude, number longitude, boolean centroids)

Computes the distance between the Marker and the given latitude and longitude. If centroids is true, the distance is computed from the center of the circle to the given point. Otherwise, the distance is computed from the closest point on the marker to the given point. If an error occurs, -1 will be returned.

#### HideInfobox

Hides the circle's info box if it is visible. Otherwise, no action will be taken.

#### SetLocation(number latitude, number longitude)

Moves the center of the circle to the given latitude and longitude. This method is more efficient than setting latitude and longitude separately.

#### ShowInfobox

Shows the info box for the circle if it is not visible. Otherwise, no action will be taken. This method can be used to show the info box even if EnableInfobox is false.
