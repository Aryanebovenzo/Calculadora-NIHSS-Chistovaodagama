<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Calculadora NIHSS</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 20px; max-width: 700px; }
    h1 { color: #004080; }
    .item { margin-bottom: 15px; }
    label { font-weight: bold; display: block; }
    select { width: 100%; padding: 5px; }
    #resultado { font-size: 20px; margin-top: 20px; font-weight: bold; color: #006400; }
    button { padding: 10px 20px; background-color: #004080; color: white; border: none; border-radius: 5px; }
  </style>
</head>
<body>
  <h1>Calculadora NIHSS</h1>

  <form id="formNIHSS">
    <div class="item">
      <label for="consciencia">1. Nível de Consciência:</label>
      <select id="consciencia">
        <option value="0">0 - Alerta</option>
        <option value="1">1 - Sonolento</option>
        <option value="2">2 - Estupor</option>
        <option value="3">3 - Coma</option>
      </select>
    </div>

    <div class="item">
      <label for="olhar">2. Paralisia do Olhar:</label>
      <select id="olhar">
        <option value="0">0 - Normal</option>
        <option value="1">1 - Parcial</option>
        <option value="2">2 - Paralisia Total</option>
      </select>
    </div>

    <!-- Adicione mais campos conforme os outros critérios do NIHSS -->

    <button type="button" onclick="calcular()">Calcular NIHSS</button>
  </form>

  <div id="resultado"></div>

  <script>
    function calcular() {
      const consciencia = parseInt(document.getElementById("consciencia").value);
      const olhar = parseInt(document.getElementById("olhar").value);

      // Adicione outras variáveis aqui conforme expandir o formulário

      const total = consciencia + olhar;

      document.getElementById("resultado").innerText = "NIHSS Total: " + total;
    }
  </script>
</body>
</html>
# Calculadora-NIHSS-Chistovaodagama
