# Openstreet Map Component

The latest MIT App Inventor Openstreet Map component is now available in AppyBuilder.  This component is a two-dimensional container that renders map tiles in the background and allows for multiple Marker elements to identify points on the map. Map tiles are supplied by OpenStreetMap contributors and the United States Geological Survey.

The Map component provides three utilities for manipulating its boundaries within App Inventor. First, a locking mechanism allows the map to be moved relative to other components on the Screen. Second, when unlocked, the user can pan the Map to any location. At this new location, the “Set Initial Boundary” button can be pressed to save the current Map coordinates to its properties. Lastly, if the Map is moved to a different location, for example to add Markers off-screen, then the “Reset Map to Initial Bounds” button can be used to recenter the Map at the starting location.

{% youtube %}https://www.youtube.com/watch?v=-rRmMnO2oQ4{% endyoutube %}

## Circle {#Circle}

The Circle component visualizes a circle of a given radius, in meters, at a latitude and longitude. The circle's appearnce can be customized using properties such as[`FillColor`](http://gold.appybuilder.com/reference/components/maps.html#Circle.FillColor),[`StrokeColor`](http://gold.appybuilder.com/reference/components/maps.html#Circle.StrokeColor), and[`StrokeWidth`](http://gold.appybuilder.com/reference/components/maps.html#Circle.StrokeWidth).

The Circle component can also be used to implement features such as geofencing, a mechanism where the user's presence within an area is used to trigger other behaviors. Using the[`DistanceToPoint`](http://gold.appybuilder.com/reference/components/maps.html#Circle.DistanceToPoint)method combined with the[LocationSensor](http://gold.appybuilder.com/reference/components/sensors.html#LocationSensor), you can determine whether a user's location is inside or outside of the circle. You can use this feature to trigger additional actions.

### Properties

Description

Sets or gets the description displayed in the info window. The info window appears when the user taps on the circle.

Draggable

Sets or gets whether or not the user can drag a map feature. This feature is accessed by long-pressing and then dragging the circle to a new location.

EnableInfobox

Enables or disables the infobox window display when the user taps the circle.

FillColor

Sets or gets the color used to fill in the circle.

Latitude

Sets or gets the latitude of the center of the circle, in degrees. Positive values representing north of the equator and negative values representing south of the equator. To update the latitude and longitude simultaneously, use the

[`SetLocation`](http://gold.appybuilder.com/reference/components/maps.html#Circle.SetLocation)

method.

Longitude

Sets or gets the longitude of the center of the circle, in degrees. Positive values representing east of the prime meridian and negative values representing west of the prime meridian. To update the latitude and longitude simultaneously, use the

[`SetLocation`](http://gold.appybuilder.com/reference/components/maps.html#Circle.SetLocation)

method.

Radius

Sets or gets the radius of the circle, in meters.

StrokeColor

Sets or gets the color used to outline the circle.

StrokeWidth

Sets or gets the width of the stroke used to outline the circle.

Title

Sets or gets the title displayed in the info window that appears when the user clicks on the map feature.

Type

Gets the type of the feature. For Circle, this will always be "Circle",

Visible

Sets or gets whether the component should be visible on the screen. Value is true if the component is showing and false if hidden.

### Events

Click

Runs when the user taps on the circle.

Drag

Runs during drag operations.

LongClick

Runs after the user long clicks on the circle but does not trigger a drag. Note that this event will only trigger if

[`Draggable`](http://gold.appybuilder.com/reference/components/maps.html#Circle.Draggable)

is false.

StartDrag

Runs before a drag operation begins. Use this to save the current position of the circle, for example.

StopDrag

Runs after a drag operation completes. Use this to save the new position of the circle, for example.

### Methods

number DistanceToFeature\(component mapFeature, boolean centroids\)

Computes the distance between the Circle and the given mapFeature. If

`centroids`

is true, the computation is done between the centroids of the two features. Otherwise, the distance will be computed between the two features based on the closest points. Further, when

`centroids`

is false, this method will return 0 if the circle intersects or contains the

`mapFeature`

. If an error occurs, this method will return -1.

number DistanceToPoint\(number latitude, number longitude, boolean centroids\)

Computes the distance between the Circle and the given latitude and longitude. If

`centroids`

is true, the distance is computed from the center of the circle to the given point. Otherwise, the distance is computed from the closest point on the circle to the given point. Further, this method will return 0 if

`centroids`

is false and the point is in the circle. If an error occurs, -1 will be returned.

HideInfobox

Hides the circle's info box if it is visible. Otherwise, no action is taken.

SetLocation\(number latitude, number longitude\)

Moves the center of the circle to the given latitude and longitude. This method is more efficient than setting latitude and longitude separately.

ShowInfobox

Shows the info box for the circle if it is not visible. Otherwise, this method has no effect. This method can be used to show the info box even if

[`EnableInfobox`](http://gold.appybuilder.com/reference/components/maps.html#Circle.EnableInfobox)

is false.

## FeatureCollection {#FeatureCollection}

A FeatureCollection groups one or more map features together. Any events that occur within a feature in the collection will also trigger the corresponding event in the collection component. FeatureCollections can be loaded from exernal resources to populate Maps with content. GeoJSON is the only format supported at this time.

### Properties

Features

Returns a list of features present in the feature collection, if any.

FeaturesFromGeoJSON

Populates the feature collection from a string containing GeoJSON content. Given the size of such strings, it is recommended to load the feature collection from assets or the web using the Source property.

Source

The source of the content for the feature collection, such as a filename or a URL.

Visible

Specifies whether the component should be visible on the screen. Value is true if the component is showing and false if hidden.

### Events

FeatureClick\(component feature\)

When a feature is clicked, the feature collection containing it \(if any\) will also receive a

`FeatureClick`

event. The feature parameter indicates which child feature was clicked.

FeatureDrag\(component feature\)

When a feature is dragged, the parent collection will also receive a

`FeatureDrag`

event. The feature parameter indicates which child feature was dragged.

FeatureLongClick\(component feature\)

When a feature is long clicked, the parent collection will also receive a

`FeatureLongClick`

event. The feature parameter indicates which child feature was long clicked.

FeatureStartDrag\(component feature\)

When the user begins dragging a feature, the parent collection will also receive a

`FeatureStartDrag`

event. The feature parameter indicates which child feature was dragged.

FeatureStopDrag\(component feature\)

When the user stops dragging a feature, the parent collection will also receive a

`FeatureStopDrag`

event. The feature parameter indicates which child feature was dragged.

GotFeatures\(text url, list features\)

The GotFeatures event is run when when a feature collection is successfully read from the given

`url`

. The

`features`

parameter will be a list of feature descriptions that can be converted into components using the

[`FeatureFromDescription`](http://gold.appybuilder.com/reference/components/maps.html#FeatureCollection.FeatureFromDescription)

method.

LoadError\(text url, list features\)

The LoadError event is run when an error occurs while processing a feature collection document at the given

`url`

. The

`responseCode`

parameter will contain an HTTP status code and the

`errorMessage`

parameter will contain a detailed error message.

### Methods

any FeatureFromDescription\(list description\)

Returns a new component based on the description provided. If there is an error in the properties, such as incorrectly formatted data, then the method will return text describing the error. Use the

[`is-text?`](http://appinventor.mit.edu/explore/ai2/support/blocks/text.html#istext)

block to test whether the result is an error message. is an error or not. Properties of features are converted into App Inventor properties using the following case-insensitive mapping:

* description → Description
* draggable → Draggable
* infobox → EnableInfobox
* fill → FillColor
* image → ImageAsset
* stroke → StrokeColor
* stroke-width → StrokeWidth
* title → Title
* visible → Visible

LoadFromURL\(text url\)

Call this method to load a GeoJSON description of a feature collection from a URL \(including file URLs\). If successful, the set of features managed by the feature collection will be replaced by the new features and LoadFeatureCollection event will be run. If an error occurs, the ErrorLoadingFeatureCollection event will be run instead.

## LineString {#LineString}

LineString is a component for drawing an open, continuous sequence of lines on a Map. To add new points to a LineString, drag the midpoint of any segment away from the line to introduce a new vertex. Move a vertex by clicking and dragging the vertex to a new location. Clicking on a vertex will delete the vertex.

### Properties

Description

The description displayed in the info window that appears when the user clicks on the map feature.

Draggable

Sets or gets whether or not the user can drag a line string by long-pressing and then dragging it to a new location.

EnableInfobox

Enable or disable the infobox window display when the user taps the feature.

Points

The list of points, as pairs of latitudes and longitudes, in the LineString.

PointsFromString

A GeoJSON-encoded string of points to populate the LineString. Editing the LineString in the designer will update this property.

StrokeColor

The paint color used to outline the map feature.

StrokeWidth

The width of the stroke used to outline the map feature.

Title

The title displayed in the info window that appears when the user clicks on the map feature.

Type

Gets the type of the feature. For LineString, this will always be "LineString",

Visible

Specifies whether the component should be visible on the screen. Value is true if the component is showing and false if hidden.

### Events

Click

Runs when the user taps on or very close to the line string.

Drag

Runs during a drag operation.

LongClick

Runs after the user long clicks on the line string but does not trigger a drag \(within a given threshold\).

StartDrag

Runs immediately after the user begins a drag operation but before any Drag events.

StopDrag

Runs after the user releases the LineString from a Drag operation.

### Methods

number DistanceToFeature\(component mapFeature, boolean centroids\)

Computes the distance between the LineString and the given

`mapFeature`

. If

`centroids`

is true, the computation is done between the centroids of the two features. If false, the distance will be computed between the two features based on the closests points. If the linestring intersects the

`mapFeature`

, this method will return 0. If an error occurs, -1 will be returned.

number DistanceToPoint\(number latitude, number longitude, boolean centroids\)

Computes the distance between the LineString and the given

`latitude`

and

`longitude`

. If

`centroids`

is true, the computation is done between the weighted midpoint of the LineString to the point. If false, the distance is computed from the closest point on the LineString to the point. If the point is on the LineString, this method will return 0. If an error occurs -1 will be returned.

HideInfobox

Hides the line string's info box if it is visible. Otherwise, this method has no effect.

ShowInfobox

Shows the info box for the line string if it is not visible. Otherwise, this method has no effect. This method can be used to show the info box even if

[`EnableInfobox`](http://gold.appybuilder.com/reference/components/maps.html#LineString.EnableInfobox)

is false.

## Map {#Map}

A two-dimensional container that renders map tiles in the background and allows for multiple Marker elements to identify points on the map. Map tiles are supplied by OpenStreetMap contributors and the United States Geological Survey.

The Map component provides three utilities for manipulating its boundaries within App Inventor. First, a locking mechanism allows the map to be moved relative to other components on the Screen. Second, when unlocked, the user can pan the Map to any location. At this new location, the "Set Initial Boundary" button can be pressed to save the current Map coordinates to its properties. Lastly, if the Map is moved to a different location, for example to add Markers off-screen, then the "Reset Map to Initial Bounds" button can be used to recenter the Map at the starting location.

### Properties

BoundingBox

Sets or gets the current boundary for the map's drawn view. The value is a list of lists containing the northwest and southeast coordinates of the current view in the form

`((North West) (South East))`

.

CenterFromString

Sets the center of the map from a given "latitude, longitude" string. This is used mainly to populate the center of the Map from the designer. See also the

[`PanTo`](http://gold.appybuilder.com/reference/components/maps.html#Map.PanTo)

method to animate a change to the Map center.

EnablePan

Enables or disables the ability of the user to move the Map.

EnableRotation

Enables or disables the two-finger rotation gesture to rotate the Map.

EnableZoom

Enables or disables the two-finger pinch gesture to zoom the Map.

Features

Sets or gets a list of features present on the Map. Setting this to an empty list will clear the Map.

Height

Sets or gets the height of the Map.

HeightPercent

Sets the height of the Map to a percentage of the Screen.

Latitude

Gets the latitude of the center of the Map. To change the latitude, use the

[`PanTo`](http://gold.appybuilder.com/reference/components/maps.html#Map.PanTo)

method.

LocationSensor

Uses the provided LocationSensor for user location data rather than the built-in location provider.

Longitude

Gets the longitude of the center of the Map. To change the longitude, use the

[`PanTo`](http://gold.appybuilder.com/reference/components/maps.html#Map.PanTo)

method.

MapType

Sets or gets the tile layer used to draw the Map background. Defaults to Roads. Valid values are 1 \(Roads\), 2 \(Aerial\), or 3 \(Terrain\). Road layers are provided by OpenStreetMap and aerial and terrain layers are provided by the U.S. Geological Survey.

ShowCompass

Shows or hides a compass overlay on the Map. The compass will be rotated based on the device's orientation if a digital compass is present in hardware.

ShowUser

Shows or hides an icon indicating the user's current location on the Map. The availability and accuracy of this feature will depend on whether the user has location services enabled and which location providers are available.

ShowZoom

Shows or hides the Android native zoom buttons to allow the user to zoom the Map in or out. This can be used in place of the two-finger pinch-to-zoom gesture.

UserLatitude

Returns the user's latitude if ShowUser is enabled.

UserLongitude

Returns the user's longitude if ShowUser is enabled.

Visible

Sets or gets whether the Map is visible.

Width

Sets or gets the width of the Map.

WidthPercent

Sets the Width of the Map to a percentage of the Screen.

ZoomLevel

Gets or sets the zoom level for the Map. Valid values range from 1-20. Not all tile layers will support each zoom level at every location. For example, detailed aerial photography is likely not available for tiles in the middle of the ocean or at the poles. Highest zoom levels will likely occur in major city centers due to the amount of detailed data available.

### Events

BoundsChange

Runs when the user changes the map bounds, either by zooming, panning, or rotating the view.

DoubleTapAtPoint\(number latitude, number longitude\)

Runs when the user double-taps at a point on the map.

`latitude`

and

`longitude`

indicate the location of the tap event in map coordinates. This event may be followed by a

[`ZoomChange`](http://gold.appybuilder.com/reference/components/maps.html#Map.ZoomChange)

event if zooming gestures are enabled and the map is not at the highest possible zoom level.

FeatureClick\(component feature\)

When a feature is clicked, the parent map will also receive a

`FeatureClick`

event. The

`feature`

parameter indicates which child feature was clicked.

FeatureDrag\(component feature\)

When a feature is dragged, the parent map will also receive a

`FeatureDrag`

event. The

`feature`

parameter indicates which child feature was dragged.

FeatureLongClick\(component feature\)

When a feature is long clicked, the parent map will also receive a

`FeatureLongClick`

event. The

`feature`

parameter indicates which child feature was long clicked.

FeatureStartDrag\(component feature\)

When the user begins dragging a feature, the parent map will also receive a

`FeatureStartDrag`

event. The

`feature`

parameter indicates which child feature was dragged.

FeatureStopDrag\(component feature\)

When the user stops dragging a feature, the parent map will also receive a

`FeatureStopDrag`

event. The

`feature`

parameter indicates which child feature was dragged.

GotFeatures\(text url, list features\)

The

`GotFeatures`

event runs after a call to

[`LoadFromURL`](http://gold.appybuilder.com/reference/components/maps.html#Map.LoadFromURL)

successfully reads feature description from

`url`

. The

`features`

parameter will be a list of feature descriptions that can be converted into components using the

[`FeatureFromDescription`](http://gold.appybuilder.com/reference/components/maps.html#FeatureCollection.FeatureFromDescription)

method.

InvalidPoint\(text message\)

Runs when the program encounters an invalid point while processing geographical data. Points are considered invalid when the latitude or longitude for the point is outside the acceptable range \(\[-90, 90\] and \[-180, 180\], respectively\). The

`message`

parameter will contain an explanation for the error.

LoadError\(text url, number responseCode, text errorMessage\)

The LoadError event runs when processing a feature collection document at the given

`url`

produces an error. The

`responseCode`

parameter will contain an HTTP status code and the

`errorMessage`

parameter will contain a detailed error message.

LongPressAtPoint\(number latitude, number longitude\)

Runs when the user long presses a point on the map.

`Latitude`

and

`longitude`

indicate the location of the long press in map coordinates. Note that this event will not trigger if

[`EnablePan`](http://gold.appybuilder.com/reference/components/maps.html#Map.EnablePan)

is true as a long press causes a panning event instead.

Ready

Runs when the map has initalized and is ready for use.

TapAtPoint\(number latitude, number longitude\)

Runs when the user taps at a point on the map. The tapped location will be reported in map coordinates via the

`latitude`

and

`longitude`

parameters.

ZoomChange

Runs when the user changes the zoom level, such as through a pinch gesture or double-tapping.

### Methods

component CreateMarker\(number latitude, number longitude\)

Creates a new marker on the map at the given

`latitude`

and

`longitude`

. The marker can be manipulated using the "any component" blocks.

any FeatureFromDescription\(list description\)

Returns a new component based on the description provided. If there is an error in the properties, such as incorrectly formatted data, then the method will return text describing the error. Use the

[`is-text?`](http://appinventor.mit.edu/explore/ai2/support/blocks/text.html#istext)

block to test whether you get an error. Feature properties converted into App Inventor properties use the following case-insentive mapping:

* description → Description
* draggable → Draggable
* infobox → EnableInfobox
* fill → FillColor
* image → ImageAsset
* stroke → StrokeColor
* stroke-width → StrokeWidth
* title → Title
* visible → Visible

LoadFromURL\(text url\)

Call this method to load a feature collection from a URL \(including file URLs\). If the event is successful, the feature descriptions are passed as a list to the

[`GotFeatures`](http://gold.appybuilder.com/reference/components/maps.html#Map.GotFeatures)

event. If it fails, the

[`LoadError`](http://gold.appybuilder.com/reference/components/maps.html#Map.LoadError)

event will be run. At this time, GeoJSON is the only supported format.

PanTo\(number latitude, number longitude, number zoom\)

Pans the map center to the given

`(Latitude Longitude)`

and zooms to the given

`zoom`

. The movement is animated.

Save\(text path\)

Saves descriptions of the map contents to the given path. Currently, this will only save the features using the GeoJSON format.

## Marker {#Marker}

The Marker component indicates points on a Map, such as buildings or points of interest. Markers can be customized in many ways, such as using custom images from the app's assets. Markers can also be created dynamically using the[`CreateMarker`](http://gold.appybuilder.com/reference/components/maps.html#Map.CreateMarker)method and configured using the "Any Component" blocks.

### Properties

AnchorHorizontal

Sets or gets the horizontal offset of the marker center relative to its image. Valid values are 1 \(Left\), 2 \(Right\), 3 \(Center\)

AnchorVertical

Sets or gets the vertical offset of the marker center relative to its image. Valid values are 1 \(Top\), 2 \(Center\), 3 \(Bottom\).

Description

Sets or gets the description displayed in the info window that appears when the user taps on the marker.

Draggable

The Draggable property is used to control whether or not the user can drag the marker by long-pressing and then dragging the marker to a new location.

EnableInfobox

Enables or disables the infobox window display when the user taps the marker.

FillColor

Sets or gets the color used to fill in the marker. This property only applies for markers using vector image assets, including the default icon.

Height

Sets or gets the height of the marker, in pixels.

HeightPercent

Sets the height of the marker as a percentage of the screen height.

ImageAsset

Sets or gets the image shown for the marker. If set to the empty string

`""`

, then the default marker icon will be used.

Latitude

Sets or gets the latitude of the marker, in degrees, with positive values representing north of the equator and negative values representing south of the equator. To update the latitude and longitude simultaneously, use the

[`SetLocation`](http://gold.appybuilder.com/reference/components/maps.html#Marker.SetLocation)

method.

Longitude

Sets or gets the longitude of the marker, in degrees, with positive values representing east of the prime meridian and negative values representing west of the prime meridian. To update the latitude and longitude simultaneously, use the

[`SetLocation`](http://gold.appybuilder.com/reference/components/maps.html#Marker.SetLocation)

method.

StrokeColor

Sets or gets the color used to outline the marker.

StrokeWidth

Sets or gets the width of the stroke used to outline the marker.

Title

Sets or gets the title displayed in the info window that appears when the user clicks on the marker.

Type

Gets the type of the feature. For Marker, this will always be "Marker",

Visible

Sets or gets whether the component should be visible on the screen. Value is true if the component is showing and false if hidden.

Width

Sets or gets the width of the marker, in pixels.

WidthPercent

Sets the width of the marker as a percentage of the screen width.

### Events

Click

Runs when the user taps on the marker.

Drag

Runs continuously while a user is dragging the marker.

LongClick

Runs when the user long-clicks on the marker but does not trigger a drag. Note that this event will only run if

[`Draggable`](http://gold.appybuilder.com/reference/components/maps.html#Marker.Draggable)

is false.

StartDrag

Runs before a drag operation begins.

StopDrag

Runs after a drag operation completes.

### Methods

number BearingToFeature\(component mapFeature, boolean centroids\)

Returns the bearing from the Marker to the given

`mapFeature`

, in degrees from due north. If the

`centroids`

paremter is true, the bearing will be to the center of the map feature. Otherwise, the bearing will be computed to the point in the feature nearest the Marker.

number BearingToPoint\(number latitude, number longitude, boolean centroids\)

Returns the bearing from the Marker to the given latitude and longitude, in degrees from due north.

number DistanceToFeature\(component mapFeature, boolean centroids\)

Computes the distance between the Marker and the given

`mapFeature`

. If

`centroids`

is true, the computation is done between the centroids of the two features. Otherwise, the distance will be computed between the two features based on the closest points. Further, when

`centroids`

is false, this method will return 0 if the marker intersects or contains the

`mapFeature`

. If an error occurs, this method will return -1.

number DistanceToPoint\(number latitude, number longitude, boolean centroids\)

Computes the distance between the Marker and the given latitude and longitude. If

`centroids`

is true, the distance is computed from the center of the circle to the given point. Otherwise, the distance is computed from the closest point on the marker to the given point. If an error occurs, -1 will be returned.

HideInfobox

Hides the circle's info box if it is visible. Otherwise, no action will be taken.

SetLocation\(number latitude, number longitude\)

Moves the center of the circle to the given latitude and longitude. This method is more efficient than setting latitude and longitude separately.

ShowInfobox

Shows the info box for the circle if it is not visible. Otherwise, no action will be taken. This method can be used to show the info box even if EnableInfobox is false.

## Polygon {#Polygon}

Polygon encloses an arbitrary 2-dimensional area on a Map. Polygons can be used for drawing a perimeter, such as a campus, city, or country. Polygons begin as basic triangles. New vertices can be created by dragging the midpoint of a polygon away from the edge. Clicking on a vertex will remove the vertex, but a minimum of 3 vertices must exist at all times.

### Properties

Description

Sets or gets the description displayed in the info window that appears when the user taps on the polygon.

Draggable

Sets or gets whether or not the user can drag the polygon by long-pressing and then dragging it to a new location.

EnableInfobox

Enables or disables the infobox window display when the user taps the polygon.

FillColor

Sets or gets the color used to fill in the polygon.

HolePoints

Sets or gets the lists of points that comprise the polygon's holes. Points are given as

`(Latitude Longitude)`

pairs and should be given counterclockwise.

HolePointsFromString

Sets the list of hole points from a string in GeoJSON format.

Points

Sets or gets the list of points that comprise the polygon. Points are given as

`(Latitude Longitude)`

pairs and should be given clockwise.

PointsFromString

Sets the list of points from a string in GeoJSON format.

StrokeColor

Sets or gets the color used to outline the polygon.

StrokeWidth

Sets or gets the width of the stroke used to outline the polygon.

Title

Sets or gets the title displayed in the info window that appears when the user clicks on the map feature.

Type

Gets the type of the feature. For Polygon, this will always be "Polygon",

Visible

Sets or gets whether the component should be visible on the screen. Value is true if the component is showing and false if hidden.

### Events

Click

Runs when the user taps on the polygon.

Drag

Runs continuously while a user is dragging the polygon.

LongClick

Runs when the user long-clicks on the polygon but does not trigger a drag. Note that this event will only run if

[`Draggable`](http://gold.appybuilder.com/reference/components/maps.html#Polygon.Draggable)

is false.

StartDrag

Runs before a drag operation begins.

StopDrag

Runs after a drag operation completes.

### Methods

list Centroid

Returns the centroid of the polygon as a list of the form

`(Latitude Longitude)`

.

number DistanceToFeature\(component mapFeature, boolean centroid\)

Computes the distance between the polygon and the given mapFeature. If centroids is true, the computation is done between the centroids of the two features. Otherwise, the distance will be computed between the two features based on the closest points. Further, if centroids is false, this method will return 0 if the polygon intersects or contains the mapFeature. If an error occurs, this method will return -1.

number DistanceToPoint\(number latitude, number longtitude, boolean centroid\)

Computes the distance between the Polygon and the given latitude and longitude. If centroids is true, the distance is computed from the center of the polygon to the given point. Otherwise, the distance is computed from the closest point on the polygon to the given point. Further, this method will return 0 if centroids is false and the point is in the polygon. If an error occurs, -1 will be returned.

HideInfobox

Hides the polygon's info box if it is visible. Otherwise, this method has no effect.

ShowInfobox

Shows the info box for the polygon if it is not visible. Otherwise, this method has no effect. This method can be used to show the info box even if

[`EnableInfobox`](http://gold.appybuilder.com/reference/components/maps.html#Polygon.EnableInfobox)

is false.

## Rectangle {#Rectangle}

Rectangles are polygons with fixed latitudes and longitudes for the north, south, east, and west boundaries. Moving a vertex of the rectangle updates the appropriate edges accordingly.

### Properties

Description

Sets or gets the description displayed in the info window that appears when the user taps on the rectangle.

Draggable

Sets or gets whether or not the user can drag a map feature by long-pressing and then dragging the rectangle to a new location.

EastLongitude

Sets or gets the longitude bounding the rectangle on the east. Range: \[-180, 180\]

EnableInfobox

Enables or disables the infobox window display when the user taps the rectangle.

FillColor

Sets or gets the color used to fill in the rectangle.

NorthLatitude

Sets or gets the latitude, in degrees, bounding the rectangle on the north. Range: \[-90, 90\]

SouthLatitude

Sets or gets the latitude, in degrees, bounding the rectangle on the south. Range: \[-90, 90\]

StrokeColor

Sets or gets the color used to outline the rectangle.

StrokeWidth

Sets or gets the width of the stroke used to outline the rectangle.

Title

Sets or gets the title displayed in the info window that appears when the user clicks on the rectangle.

Type

Gets the type of the feature. For Rectangle, this will always be "Rectangle",

Visible

Sets or gets whether the component should be visible on the screen. Value is true if the component is showing and false if hidden.

WestLongitude

Sets or gets the longitude, in degrees, bouding the rectangle on the west. Range: \[-180, 180\]

### Events

Click

Runs when the user taps on the rectangle.

Drag

Runs continuously while a user is dragging the rectangle.

LongClick

Runs when the user long-clicks on the rectangle but does not trigger a drag. Note that this event will only run if

[`Draggable`](http://gold.appybuilder.com/reference/components/maps.html#Rectangle.Draggable)

is false.

StartDrag

Runs before a drag operation begins.

StopDrag

Runs after a drag operation completes.

### Methods

list Bounds

Returns the bounding box of the Rectangle in the format

`((North West) (South East))`

.

list Center

Returns the center of the Rectangle as a list of the form

`(Latitude Longitude)`

.

number DistanceToFeature\(component mapFeature, boolean centroids\)

Computes the distance between the Rectangle and the given mapFeature. If centroids is true, the computation is done between the centroids of the two features. Otherwise, the distance will be computed between the two features based on the closest points. Further, when centroids is false, this method will return 0 if the rectangle intersects or contains the

`mapFeature`

. If an error occurs, this method will return -1.

number DistanceToPoint\(number latitude, number longitude, boolean centroids\)

Computes the distance between the Rectangle and the given latitude and longitude. If centroids is true, the distance is computed from the center of the rectangle to the given point. Otherwise, the distance is computed from the closest point on the rectangle to the given point. Further, this method will return 0 if centroids is false and the point is in the rectangle. If an error occurs, -1 will be returned.

HideInfobox

Hides the rectangle's info box if it is visible. Otherwise, this method has no effect.

SetCenter\(number latitude, number longitude\)

Moves the Rectangle so that it is centered on the given

`latitude`

and

`longitude`

while attempting to maintain the width and height of the Rectangle as measured from the center to the edges.

ShowInfobox

Shows the info box for the rectangle if it is not visible. Otherwise, this method has no effect. This method can be used to show the info box even if EnableInfobox is false.

