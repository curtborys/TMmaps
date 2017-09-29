<!DOCTYPE html>
<html>
  <head>
  <style>
    #map-canvas { width:500px; height:400px; }
    .layer-wizard-search-label { font-family: sans-serif };
  </style>
  <script type="text/javascript"
    src="http://maps.google.com/maps/api/js?sensor=false">
  </script>
  <script type="text/javascript">
    var map;
    var layer_1;
    var layer_0;
    function initialize() {
      map = new google.maps.Map(document.getElementById('map-canvas'), {
        center: new google.maps.LatLng(52.64358630115554, -105.28242345312498),
        zoom: 6,
        mapTypeId: google.maps.MapTypeId.ROADMAP
      });
      layer_1 = new google.maps.FusionTablesLayer({
        query: {
          select: "col5",
          from: "1LjrrpEWKluFJm7r3H2hF0LhQw0Lq7Pd0tsWogJp6"
        },
        map: map,
        styleId: 2,
        templateId: 2
      });
      layer_0 = new google.maps.FusionTablesLayer({
        query: {
          select: "col8",
          from: "1QU5qSSah59a6rT4SbK5rCToexvbBVheZKcrtCpsT"
        },
        map: map,
        styleId: 2,
        templateId: 2
      });
    }
    google.maps.event.addDomListener(window, 'load', initialize);
  </script>
  </head>
  <body>
    <div id="map-canvas"></div>
  </body>
</html>
