Rectangle
Rectangles are polygons with fixed latitudes and longitudes for the north, south, east, and west boundaries. Moving a vertex of the rectangle updates the appropriate edges accordingly.

Properties
Description
Sets or gets the description displayed in the info window that appears when the user taps on the rectangle.
Draggable
Sets or gets whether or not the user can drag a map feature by long-pressing and then dragging the rectangle to a new location.
EastLongitude
Sets or gets the longitude bounding the rectangle on the east. Range: [-180, 180]
EnableInfobox
Enables or disables the infobox window display when the user taps the rectangle.
FillColor
Sets or gets the color used to fill in the rectangle.
NorthLatitude
Sets or gets the latitude, in degrees, bounding the rectangle on the north. Range: [-90, 90]
SouthLatitude
Sets or gets the latitude, in degrees, bounding the rectangle on the south. Range: [-90, 90]
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
Sets or gets the longitude, in degrees, bouding the rectangle on the west. Range: [-180, 180]
Events
Click
Runs when the user taps on the rectangle.
Drag
Runs continuously while a user is dragging the rectangle.
LongClick
Runs when the user long-clicks on the rectangle but does not trigger a drag. Note that this event will only run if Draggable is false.
StartDrag
Runs before a drag operation begins.
StopDrag
Runs after a drag operation completes.
Methods
list Bounds
Returns the bounding box of the Rectangle in the format ((North West) (South East)).
list Center
Returns the center of the Rectangle as a list of the form (Latitude Longitude).
number DistanceToFeature(component mapFeature, boolean centroids)
Computes the distance between the Rectangle and the given mapFeature. If centroids is true, the computation is done between the centroids of the two features. Otherwise, the distance will be computed between the two features based on the closest points. Further, when centroids is false, this method will return 0 if the rectangle intersects or contains the mapFeature. If an error occurs, this method will return -1.
number DistanceToPoint(number latitude, number longitude, boolean centroids)
Computes the distance between the Rectangle and the given latitude and longitude. If centroids is true, the distance is computed from the center of the rectangle to the given point. Otherwise, the distance is computed from the closest point on the rectangle to the given point. Further, this method will return 0 if centroids is false and the point is in the rectangle. If an error occurs, -1 will be returned.
HideInfobox
Hides the rectangle's info box if it is visible. Otherwise, this method has no effect.
SetCenter(number latitude, number longitude)
Moves the Rectangle so that it is centered on the given latitude and longitude while attempting to maintain the width and height of the Rectangle as measured from the center to the edges.
ShowInfobox
Shows the info box for the rectangle if it is not visible. Otherwise, this method has no effect. This method can be used to show the info box even if EnableInfobox is false.
