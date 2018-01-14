# Map

A two-dimensional container that renders map tiles in the background and allows for multiple Marker elements to identify points on the map. Map tiles are supplied by OpenStreetMap contributors and the United States Geological Survey.

The Map component provides three utilities for manipulating its boundaries within App Inventor. First, a locking mechanism allows the map to be moved relative to other components on the Screen. Second, when unlocked, the user can pan the Map to any location. At this new location, the "Set Initial Boundary" button can be pressed to save the current Map coordinates to its properties. Lastly, if the Map is moved to a different location, for example to add Markers off-screen, then the "Reset Map to Initial Bounds" button can be used to recenter the Map at the starting location.

---

### Properties

#### BoundingBox

Sets or gets the current boundary for the map's drawn view. The value is a list of lists containing the northwest and southeast coordinates of the current view in the form ((North West) (South East)).

#### CenterFromString

Sets the center of the map from a given "latitude, longitude" string. This is used mainly to populate the center of the Map from the designer. See also the PanTo method to animate a change to the Map center.

#### EnablePan

Enables or disables the ability of the user to move the Map.

#### EnableRotation

Enables or disables the two-finger rotation gesture to rotate the Map.

#### EnableZoom

Enables or disables the two-finger pinch gesture to zoom the Map.

#### Features

Sets or gets a list of features present on the Map. Setting this to an empty list will clear the Map.

#### Height

Sets or gets the height of the Map.

#### HeightPercent

Sets the height of the Map to a percentage of the Screen.

#### Latitude

Gets the latitude of the center of the Map. To change the latitude, use the PanTo method.

#### LocationSensor

Uses the provided LocationSensor for user location data rather than the built-in location provider.

#### Longitude

Gets the longitude of the center of the Map. To change the longitude, use the PanTo method.

#### MapType

Sets or gets the tile layer used to draw the Map background. Defaults to Roads. Valid values are 1 (Roads), 2 (Aerial), or 3 (Terrain). Road layers are provided by OpenStreetMap and aerial and terrain layers are provided by the U.S. Geological Survey.

#### ShowCompass

Shows or hides a compass overlay on the Map. The compass will be rotated based on the device's orientation if a digital compass is present in hardware.

#### ShowUser

Shows or hides an icon indicating the user's current location on the Map. The availability and accuracy of this feature will depend on whether the user has location services enabled and which location providers are available.

#### ShowZoom

Shows or hides the Android native zoom buttons to allow the user to zoom the Map in or out. This can be used in place of the two-finger pinch-to-zoom gesture.

#### UserLatitude

Returns the user's latitude if ShowUser is enabled.

#### UserLongitude

Returns the user's longitude if ShowUser is enabled.

#### Visible

Sets or gets whether the Map is visible.

#### Width

Sets or gets the width of the Map.

#### WidthPercent

Sets the Width of the Map to a percentage of the Screen.

#### ZoomLevel

Gets or sets the zoom level for the Map. Valid values range from 1-20. Not all tile layers will support each zoom level at every location. For example, detailed aerial photography is likely not available for tiles in the middle of the ocean or at the poles. Highest zoom levels will likely occur in major city centers due to the amount of detailed data available.

---

### Events

#### BoundsChange

Runs when the user changes the map bounds, either by zooming, panning, or rotating the view.

#### DoubleTapAtPoint(number latitude, number longitude)

Runs when the user double-taps at a point on the map. latitude and longitude indicate the location of the tap event in map coordinates. This event may be followed by a ZoomChange event if zooming gestures are enabled and the map is not at the highest possible zoom level.

#### FeatureClick(component feature)

When a feature is clicked, the parent map will also receive a FeatureClick event. The feature parameter indicates which child feature was clicked.

#### FeatureDrag(component feature)

When a feature is dragged, the parent map will also receive a FeatureDrag event. The feature parameter indicates which child feature was dragged.

#### FeatureLongClick(component feature)

When a feature is long clicked, the parent map will also receive a FeatureLongClick event. The feature parameter indicates which child feature was long clicked.

#### FeatureStartDrag(component feature)

When the user begins dragging a feature, the parent map will also receive a FeatureStartDrag event. The feature parameter indicates which child feature was dragged.

#### FeatureStopDrag(component feature)

When the user stops dragging a feature, the parent map will also receive a FeatureStopDrag event. The feature parameter indicates which child feature was dragged.

#### GotFeatures(text url, list features)

The GotFeatures event runs after a call to LoadFromURL successfully reads feature description from url. The features parameter will be a list of feature descriptions that can be converted into components using the FeatureFromDescription method.

#### InvalidPoint(text message)

Runs when the program encounters an invalid point while processing geographical data. Points are considered invalid when the latitude or longitude for the point is outside the acceptable range ([-90, 90] and [-180, 180], respectively). The message parameter will contain an explanation for the error.

#### LoadError(text url, number responseCode, text errorMessage)

The LoadError event runs when processing a feature collection document at the given url produces an error. The responseCode parameter will contain an HTTP status code and the errorMessage parameter will contain a detailed error message.

#### LongPressAtPoint(number latitude, number longitude)

Runs when the user long presses a point on the map. Latitude and longitude indicate the location of the long press in map coordinates. Note that this event will not trigger if EnablePan is true as a long press causes a panning event instead.

#### Ready

Runs when the map has initalized and is ready for use.

#### TapAtPoint(number latitude, number longitude)

Runs when the user taps at a point on the map. The tapped location will be reported in map coordinates via the latitude and longitude parameters.

#### ZoomChange

Runs when the user changes the zoom level, such as through a pinch gesture or double-tapping.

---

### Methods

#### CreateMarker(number latitude, number longitude)

Creates a new marker on the map at the given latitude and longitude. The marker can be manipulated using the "any component" blocks.

#### FeatureFromDescription(list description)

Returns a new component based on the description provided. If there is an error in the properties, such as incorrectly formatted data, then the method will return text describing the error. Use the is-text? block to test whether you get an error. Feature properties converted into App Inventor properties use the following case-insentive mapping:
* description → Description
* draggable → Draggable
* infobox → EnableInfobox
* fill → FillColor
* image → ImageAsset
* stroke → StrokeColor
* stroke-width → StrokeWidth
* title → Title
* visible → Visible

#### LoadFromURL(text url)

Call this method to load a feature collection from a URL (including file URLs). If the event is successful, the feature descriptions are passed as a list to the GotFeatures event. If it fails, the LoadError event will be run. At this time, GeoJSON is the only supported format.

#### PanTo(number latitude, number longitude, number zoom)

Pans the map center to the given (Latitude Longitude) and zooms to the given zoom. The movement is animated.

#### Save(text path)

Saves descriptions of the map contents to the given path. Currently, this will only save the features using the GeoJSON format.
