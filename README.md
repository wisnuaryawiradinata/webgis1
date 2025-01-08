<!DOCTYPE html>
<html lang="en">
  <head>
    <!-- Helps the browser identify support for mobile applications -->
    <meta charset="utf-8" />

    <meta name="viewport" content="initial-scale=1,user-scalable=no,maximum-scale=1,width=device-width" />

    <meta name="mobile-web-app-capable" content="yes" />
    <meta name="apple-mobile-web-app-capable" content="yes" />
    <!-- Title on the browser tab -->
    <title>WebGIS Minimarket Kulon Progo</title>
    <!-- Leaflet CSS Library -->
    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.0.2/dist/leaflet.css" />
    <!-- Leaflet JavaScript Library -->
    <script src="https://unpkg.com/leaflet@1.0.2/dist/leaflet.js"></script>
    <!-- Style for the fullscreen map display -->
    <style>
      html,
      body,
      #map {
        height: 100%;
        width: 100%;
        margin: 0px;
      }
    </style>
  </head>

  <body>
    <!-- HTML Block to display the map -->
    <div id="map"></div>
    <script>
      /* Initial Map */
      var map = L.map("map").setView([-7.9, 110.1667], 11);

      /* Tile Basemap */
      var basemap0 = L.tileLayer("https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png", {
        maxZoom: 19,
        attribution: '&copy; <a href="http://www.openstreetmap.org/copyright">OpenStreetMap</a>',
      });
      var Esri_WorldImagery = L.tileLayer("https://server.arcgisonline.com/ArcGIS/rest/services/World_Imagery/MapServer/tile/{z}/{y}/{x}", {
        attribution: "Tiles &copy; 23611122 Wisnu Arya Wiradinata Universitas Islam Indonesia",
      });

      Esri_WorldImagery.addTo(map);

      // Custom icon for minimarket/supermarket
      var customIcon1 = L.icon({
        iconUrl: "https://www.freeiconspng.com/uploads/maps-icon-11.png", // Path to your custom minimarket icon
        iconSize: [30, 30], // Adjust the size of the icon as needed
      });

      // 10 Minimarket/Supermarket Locations in Kulon Progo
      var marker1 = L.marker([-7.8611, 110.1579], { icon: customIcon1 });
      marker1.addTo(map);
      marker1.bindPopup("<b>Superindo Wates</b><br>Jl. Bhayangkara No.12, Wates");
      marker1.bindTooltip("Superindo Wates");

      var marker2 = L.marker([-7.8433, 110.2574], { icon: customIcon1 });
      marker2.addTo(map);
      marker2.bindPopup("<b>Alfamart Sentolo</b><br>Jl. Sentolo Raya No.45, Sentolo");
      marker2.bindTooltip("Alfamart Sentolo");

      var marker3 = L.marker([-7.8715, 110.157], { icon: customIcon1 });
      marker3.addTo(map);
      marker3.bindPopup("<b>Indomaret Pengasih</b><br>Jl. Pengasih No.23, Pengasih");
      marker3.bindTooltip("Indomaret Pengasih");

      var marker4 = L.marker([-7.7985, 110.2145], { icon: customIcon1 });
      marker4.addTo(map);
      marker4.bindPopup("<b>Alfamidi Nanggulan</b><br>Jl. Nanggulan-Senten No.78, Nanggulan");
      marker4.bindTooltip("Alfamidi Nanggulan");

      var marker5 = L.marker([-7.8378, 110.2561], { icon: customIcon1 });
      marker5.addTo(map);
      marker5.bindPopup("<b>Indomaret Sentolo</b><br>Jl. Raya Sentolo No.19, Sentolo");
      marker5.bindTooltip("Indomaret Sentolo");

      var marker6 = L.marker([-7.909, 110.1245], { icon: customIcon1 });
      marker6.addTo(map);
      marker6.bindPopup("<b>Superindo Brosot</b><br>Jl. Raya Brosot No.9, Galur");
      marker6.bindTooltip("Superindo Brosot");

      var marker7 = L.marker([-7.8301, 110.0997], { icon: customIcon1 });
      marker7.addTo(map);
      marker7.bindPopup("<b>Alfamart Kokap</b><br>Jl. Raya Kokap No.7, Kokap");
      marker7.bindTooltip("Alfamart Kokap");

      var marker8 = L.marker([-7.905, 110.105], { icon: customIcon1 });
      marker8.addTo(map);
      marker8.bindPopup("<b>Indomaret Temon</b><br>Jl. Raya Temon No.4, Temon");
      marker8.bindTooltip("Indomaret Temon");

      var marker9 = L.marker([-7.7205, 110.231], { icon: customIcon1 });
      marker9.addTo(map);
      marker9.bindPopup("<b>Alfamart Kalibawang</b><br>Jl. Raya Kalibawang No.17, Kalibawang");
      marker9.bindTooltip("Alfamart Kalibawang");

      var marker10 = L.marker([-7.8905, 110.131], { icon: customIcon1 });
      marker10.addTo(map);
      marker10.bindPopup("<b>Indomaret Panjatan</b><br>Jl. Raya Panjatan No.31, Panjatan");
      marker10.bindTooltip("Indomaret Panjatan");
    </script>
  </body>
</html>
