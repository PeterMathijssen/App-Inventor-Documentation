# Polygon

Polygon encloses an arbitrary 2-dimensional area on a Map. Polygons can be used for drawing a perimeter, such as a campus, city, or country. Polygons begin as basic triangles. New vertices can be created by dragging the midpoint of a polygon away from the edge. Clicking on a vertex will remove the vertex, but a minimum of 3 vertices must exist at all times.

---

### Properties

#### Description

Sets or gets the description displayed in the info window that appears when the user taps on the polygon.

#### Draggable

Sets or gets whether or not the user can drag the polygon by long-pressing and then dragging it to a new location.

#### EnableInfobox

Enables or disables the infobox window display when the user taps the polygon.

#### FillColor

Sets or gets the color used to fill in the polygon.

#### HolePoints

Sets or gets the lists of points that comprise the polygon's holes. Points are given as (Latitude Longitude) pairs and should be given counterclockwise.

#### HolePointsFromString

Sets the list of hole points from a string in GeoJSON format.

#### Points

Sets or gets the list of points that comprise the polygon. Points are given as (Latitude Longitude) pairs and should be given clockwise.

#### PointsFromString

Sets the list of points from a string in GeoJSON format.

#### StrokeColor

Sets or gets the color used to outline the polygon.

#### StrokeWidth

Sets or gets the width of the stroke used to outline the polygon.

#### Title

Sets or gets the title displayed in the info window that appears when the user clicks on the map feature.

#### Type

Gets the type of the feature. For Polygon, this will always be "Polygon".

#### Visible

Sets or gets whether the component should be visible on the screen. Value is true if the component is showing and false if hidden.

---

### Events

#### Click

Runs when the user taps on the polygon.

#### Drag

Runs continuously while a user is dragging the polygon.

#### LongClick

Runs when the user long-clicks on the polygon but does not trigger a drag. Note that this event will only run if Draggable is false.

#### StartDrag

Runs before a drag operation begins.

#### StopDrag

Runs after a drag operation completes.

---

### Methods

#### Centroid

Returns the centroid of the polygon as a list of the form (Latitude Longitude).

#### DistanceToFeature(component mapFeature, boolean centroid)

Computes the distance between the polygon and the given mapFeature. If centroids is true, the computation is done between the centroids of the two features. Otherwise, the distance will be computed between the two features based on the closest points. Further, if centroids is false, this method will return 0 if the polygon intersects or contains the mapFeature. If an error occurs, this method will return -1.

#### DistanceToPoint(number latitude, number longtitude, boolean centroid)

Computes the distance between the Polygon and the given latitude and longitude. If centroids is true, the distance is computed from the center of the polygon to the given point. Otherwise, the distance is computed from the closest point on the polygon to the given point. Further, this method will return 0 if centroids is false and the point is in the polygon. If an error occurs, -1 will be returned.

#### HideInfobox

Hides the polygon's info box if it is visible. Otherwise, this method has no effect.

#### ShowInfobox

Shows the info box for the polygon if it is not visible. Otherwise, this method has no effect. This method can be used to show the info box even if EnableInfobox is false.
