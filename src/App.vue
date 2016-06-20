<template>
    <div id='map'></div>    
</template>

<script>

    module.exports = {
        data: function() {
            return {
                map: false
            };
        },
        ready: function() {
        L.mapbox.accessToken = 'pk.eyJ1IjoidHVkb3JrIiwiYSI6ImNpcG8zZWd2NDAwMXFoeG1hNTlueGdiYmkifQ.7bd1IQwe1_maMm3BGnDsxw';
// Replace 'mapbox.streets' with your map id.
var mapboxTiles = L.tileLayer('https://api.mapbox.com/v4/mapbox.streets/{z}/{x}/{y}.png?access_token=' + L.mapbox.accessToken, {
    attribution: '© <a href="https://www.mapbox.com/map-feedback/">Mapbox</a> © <a href="http://www.openstreetmap.org/copyright">OpenStreetMap</a>'
});

var map = L.map('map')
    .addLayer(mapboxTiles)
    .setView([42.3610, -71.0587], 15);
           
           }

    };
</script>
<style>
#map {
  height: 800px;
}
</style>