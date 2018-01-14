# FeatureCollection

A FeatureCollection groups one or more map features together. Any events that occur within a feature in the collection will also trigger the corresponding event in the collection component. FeatureCollections can be loaded from exernal resources to populate Maps with content. GeoJSON is the only format supported at this time.

---

### Properties

#### Features

Returns a list of features present in the feature collection, if any.

#### FeaturesFromGeoJSON

Populates the feature collection from a string containing GeoJSON content. Given the size of such strings, it is recommended to load the feature collection from assets or the web using the Source property.

#### Source

The source of the content for the feature collection, such as a filename or a URL.

#### Visible

Specifies whether the component should be visible on the screen. Value is true if the component is showing and false if hidden.

---

### Events

#### FeatureClick(component feature)

When a feature is clicked, the feature collection containing it (if any) will also receive a FeatureClick event. The feature parameter indicates which child feature was clicked.

#### FeatureDrag(component feature)

When a feature is dragged, the parent collection will also receive a FeatureDrag event. The feature parameter indicates which child feature was dragged.

#### FeatureLongClick(component feature)

When a feature is long clicked, the parent collection will also receive a FeatureLongClick event. The feature parameter indicates which child feature was long clicked.

#### FeatureStartDrag(component feature)

When the user begins dragging a feature, the parent collection will also receive a FeatureStartDrag event. The feature parameter indicates which child feature was dragged.

#### FeatureStopDrag(component feature)

When the user stops dragging a feature, the parent collection will also receive a FeatureStopDrag event. The feature parameter indicates which child feature was dragged.

#### GotFeatures(text url, list features)

The GotFeatures event is run when when a feature collection is successfully read from the given url. The features parameter will be a list of feature descriptions that can be converted into components using the FeatureFromDescription method.

#### LoadError(text url, list features)

The LoadError event is run when an error occurs while processing a feature collection document at the given url. The responseCode parameter will contain an HTTP status code and the errorMessage parameter will contain a detailed error message.

---

### Methods

#### FeatureFromDescription(list description)

Returns a new component based on the description provided. If there is an error in the properties, such as incorrectly formatted data, then the method will return text describing the error. Use the is-text? block to test whether the result is an error message. is an error or not. Properties of features are converted into App Inventor properties using the following case-insensitive mapping:
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

Call this method to load a GeoJSON description of a feature collection from a URL (including file URLs). If successful, the set of features managed by the feature collection will be replaced by the new features and LoadFeatureCollection event will be run. If an error occurs, the ErrorLoadingFeatureCollection event will be run instead.
