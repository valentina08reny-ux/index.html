<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,
initial-scale=1.0">
<title>Clima App</title>
<style>
body { font-family: Arial; text-align: center; margin: 20px;
}
input, button { padding: 10px; margin: 5px; }
#result { margin-top: 20px; }
</style>
</head>
<body>
<h1>Consulta el Clima</h1>
<input type="text" id="city" placeholder="Ciudad">
<button onclick="fetchWeather()">Buscar</button>
<div id="result"></div>
<script>
function fetchWeather() {
const city = document.getElementById("city").value;
// Simulación de datos (sin API real)
const mockData = {
name: city,
main: { temp: Math.floor(Math.random() * 30) + 10 },
weather: [{ description: "soleado" }]
};
document.getElementById("result").innerHTML =
`<h2>${mockData.name}</h2>
<p>Temperatura: ${mockData.main.temp}°C</p>
<p>Clima: ${mockData.weather[0].description}</p>`;
}
</script>
</body>
</html>