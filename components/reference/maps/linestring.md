# LineString

LineString is a component for drawing an open, continuous sequence of lines on a Map. To add new points to a LineString, drag the midpoint of any segment away from the line to introduce a new vertex. Move a vertex by clicking and dragging the vertex to a new location. Clicking on a vertex will delete the vertex.

---

### Properties

#### Description

The description displayed in the info window that appears when the user clicks on the map feature.

#### Draggable

Sets or gets whether or not the user can drag a line string by long-pressing and then dragging it to a new location.

#### EnableInfobox

Enable or disable the infobox window display when the user taps the feature.

#### Points

The list of points, as pairs of latitudes and longitudes, in the LineString.

#### PointsFromString

A GeoJSON-encoded string of points to populate the LineString. Editing the LineString in the designer will update this property.

#### StrokeColor

The paint color used to outline the map feature.

#### StrokeWidth

The width of the stroke used to outline the map feature.

#### Title

The title displayed in the info window that appears when the user clicks on the map feature.

#### Type

Gets the type of the feature. For LineString, this will always be "LineString".

#### Visible

Specifies whether the component should be visible on the screen. Value is true if the component is showing and false if hidden.

---

### Events

#### Click

Runs when the user taps on or very close to the line string.

#### Drag

Runs during a drag operation.

#### LongClick

Runs after the user long clicks on the line string but does not trigger a drag (within a given threshold).

#### StartDrag

Runs immediately after the user begins a drag operation but before any Drag events.

#### StopDrag

Runs after the user releases the LineString from a Drag operation.

---

### Methods

#### DistanceToFeature(component mapFeature, boolean centroids)

Computes the distance between the LineString and the given mapFeature. If centroids is true, the computation is done between the centroids of the two features. If false, the distance will be computed between the two features based on the closests points. If the linestring intersects the mapFeature, this method will return 0. If an error occurs, -1 will be returned.

#### DistanceToPoint(number latitude, number longitude, boolean centroids)

Computes the distance between the LineString and the given latitude and longitude. If centroids is true, the computation is done between the weighted midpoint of the LineString to the point. If false, the distance is computed from the closest point on the LineString to the point. If the point is on the LineString, this method will return 0. If an error occurs -1 will be returned.

#### HideInfobox

Hides the line string's info box if it is visible. Otherwise, this method has no effect.

#### ShowInfobox

Shows the info box for the line string if it is not visible. Otherwise, this method has no effect. This method can be used to show the info box even if EnableInfobox is false.
