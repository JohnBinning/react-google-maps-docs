```javascript 
///these should usually be paired with a marker
<div key={windowKey}> //react will give a warning if you don't use a unique key identifier
        <InfoWindow
          className="info-window"
          position={marker.coordinates}> //this will be the same format as coordinates on the markers
          <div>
            <h4 className='marker-location'>Denver, CO</h4>
            <p className='marker-info'>Info about Denver goes here</p>
          </div>
        </InfoWindow>
</div>

//consider giving your corresponding marker an onClick prop that will toggle marker visibility

```