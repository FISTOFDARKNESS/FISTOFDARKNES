
 html>

<html>

<head>

  <title>Sistema de Acesso</title>

  <style>

    body {

      background-color: #1f1f1f;

      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;

      display: flex;

      justify-content: center;

      align-items: center;

      height: 100vh;

      margin: 0;

    }

    .container {

      width: 400px;

      padding: 40px;

      background-color: #333;

      border-radius: 10px;

      box-shadow: 0px 0px 20px rgba(0, 0, 0, 0.4);

    }

    h1 {

      font-size: 28px;

      font-weight: bold;

      text-align: center;

      margin-bottom: 30px;

      color: #fff;

      text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);

    }

    .form-group {

      margin-bottom: 20px;

    }

    .form-group label {

      display: block;

      font-size: 18px;

      font-weight: bold;

      margin-bottom: 10px;

      color: #fff;

      text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);

    }

    .form-group input {

      width: 100%;

      height: 40px;

      font-size: 16px;

      padding: 5px;

      border: none;

      border-bottom: 2px solid #555;

      background-color: #444;

      color: #fff;

      transition: border-color 0.3s ease;

    }

    .form-group input:focus {

      border-color: #2ecc71;

      outline: none;

    }

    .button-group {

      display: flex;

      justify-content: space-between;

      margin-top: 30px;

    }

    .button-group button {

      flex-basis: 48%;

      height: 40px;

      font-size: 16px;

      font-weight: bold;

      border: none;

      border-radius: 5px;

      cursor: pointer;

      transition: background-color 0.3s ease;

    }

    #submit-button {

      background-color: #2ecc71;

      color: #fff;

    }

    #submit-button:hover {

      background-color: #27ae60;

    }

  </style>

  <script>

    function gerarChave() {

      var key = generateRandomKey(31, 100);

      document.getElementById('key-input').value = key;

      document.getElementById('submit-button').style.display = 'block';

      document.getElementById('submit-button').setAttribute('data-generated-key', key);

    }

    function verificarChave() {

      var key = document.getElementById('key-input').value;

      var generatedKey = document.getElementById('submit-button').getAttribute('data-generated-key');

      if (key === generatedKey) {

        window.location.href = 'https://www.roblox.com/games/12963782523/EARLY-ACCESS-BLANK-FRUITS-0-5-beta?gameSetTypeId=100000003&isAd=false&numberOfLoadedTiles=50&page=sortDetailPageHome&placeId=12963782523&position=18&universeId=4533760049';

      } else {

        alert('Chave incorreta. Tente novamente.');

        document.getElementById('key-input').value = '';

      }

    }

    function generateRandomKey(minLength, maxLength) {

      var length = Math.floor(Math.random() * (maxLength - minLength + 1)) + minLength;

      var characters = 'qwQwWeErRtTyYuUiIoOpPaAsSdDfFgGhHjJkKlLxXcCvVbBnNmM192837465';

      var key = '';

      for (var i = 0; i < length; i++) {

        key += characters.charAt(Math.floor(Math.random() * characters.length));

      }

      return key;

    }

  </script>

</head>

<body>

  <div class="container">

    <h1>Sistema de Acesso</h1>

    <div class="form-group">

      <label for="key-input">Chave de Acesso:</label>

      <input type="text" id="key-input" placeholder="Insira a chave de acesso" autofocus>

    </div>

    <div class="button-group">

      <button onclick="gerarChave()">Gerar Chave Aleatória</button>

      <button id="submit-button" onclick="verificarChave()" style="display: none;">Entrar</button>

    </div>

  </div>

</body>

</html>

  
