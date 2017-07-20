

```javascript
export const createMarkers = (marker) => {

    return (
        <div key={windowKey}>
            <Marker
            position={marker.coordinates}
            id={marker.id}
            key={marker.id}
            icon={url}
            style={{height: "5xpx", width: "5px"}}
            className={'marker'}
            />
        </div>
        )
}
```