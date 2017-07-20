
```javascript
createHeatMap (){
   if(!window.google){
     return <div>no google</div>
   }
    if(window.google) {
      const google = window.google
      const denver = new google.maps.LatLng(39.7392358, -104.990251)
      const boCo = new google.maps.LatLng(40.0149856, -105.2705456)
      const glendale = new google.maps.LatLng(39.7049873, -104.9335904)
    }

    return (
      <HeatmapLayer data = {[denver, boCo, glendale]} />
    )
  }
  ```