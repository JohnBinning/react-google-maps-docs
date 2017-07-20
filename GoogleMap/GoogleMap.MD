
```javascript
const GMap = withGoogleMap((props) => {
  let {  markers, createMarkers } = props
  return (
    <div>
    <GoogleMap
      defaultOptions={{ styles: mapStyle}} //for custom styles
      defaultZoom={2} 
      defaultCenter={{ lat: 21.9071923, lng: -45.0368707 }}>
          {markers.map(createMarkers)}
    </GoogleMap>
  </div>
  )
})
```

Then call Gmap

```javascript
//import createMarkers from Markers/Markers.MD
//import createHeatmap from Heatmap/Heatmap.MD

render() {

    //you must give your map a width and a height for your mapElement AND containerElement props or the map will not display 
    let mapWidth = "100%"
    const mapHeight = "600px"

    //the markers prop below takes an array of objects.  each object must have a key of coordinates that has a value of an object, with keys of lat and lng.
    const markerList = [
        { coordinates: {lat: 39.7392358, lng: -104.990251},
        { coordinates: {lat: 41.8781136, lng: -87.6297982},
        ]

    return (
      <div>
        <GMap mapElement={ <div className='map-element' style={{ height: mapHeight, width: mapWidth}}/> }
        containerElement={ <div className='container-element' style={{ height: mapHeight, width: mapWidth}}/>}
        markers={markerList}
        createMarkers={(marker) => createMarkers(marker)}
        createHeat={() => createHeatMap()}
        className="g-map"
      />
      </div>
    )
  }
}
```