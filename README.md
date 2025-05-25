# Temperature Converter (HTML + JS + Python)

## Версія 1: HTML + JavaScript

```html
<!DOCTYPE html>
<html>
<head>
  <title>Temperature Converter</title>
</head>
<body>
  <h2>Temperature Converter</h2>
  <input id="celsius" placeholder="Enter °C" oninput="convertToFahrenheit()" />
  <p id="fahrenheit"></p>

  <script>
    function convertToFahrenheit() {
      const celsius = parseFloat(document.getElementById("celsius").value);
      if (!isNaN(celsius)) {
        const fahrenheit = (celsius * 9/5) + 32;
        document.getElementById("fahrenheit").innerText = `${fahrenheit.toFixed(2)}°F`;
      } else {
        document.getElementById("fahrenheit").innerText = "";
      }
    }
  </script>
</body>
</html>
