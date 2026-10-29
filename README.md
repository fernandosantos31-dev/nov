# nov

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Verificação do Goleiro</title>

    <style>
        body {
            font-family: Arial, sans-serif;
            background: #f0f2f5;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
        }

        .container {
            background: white;
            padding: 30px;
            border-radius: 12px;
            text-align: center;
            box-shadow: 0 4px 12px #0002;
            max-width: 350px;
            width: 85%;
        }

        h1 {
            color: #166534;
        }

        select, button {
            width: 100%;
            padding: 12px;
            margin-top: 12px;
            border-radius: 6px;
            font-size: 16px;
        }

        select {
            border: 1px solid #ccc;
        }

        button {
            background: #15803d;
            color: white;
            border: none;
            cursor: pointer;
        }

        button:hover {
            background: #166534;
        }

        #resultado {
            margin-top: 20px;
            font-weight: bold;
        }
    </style>
</head>

<body>
    <div class="container">
        <h1>⚽ Início do Jogo</h1>
        <p>Há um goleiro na equipe?</p>

        <select id="goleiro">
            <option value="">Selecione uma opção</option>
            <option value="sim">Sim</option>
            <option value="nao">Não</option>
        </select>

        <button onclick="verificarGoleiro()">
            Verificar
        </button>

        <p id="resultado"></p>
    </div>

    <script>
        function verificarGoleiro() {
            const goleiroPresente =
                document.getElementById("goleiro").value;

            const resultado =
                document.getElementById("resultado");

            if (goleiroPresente === "sim") {
                resultado.textContent =
                    "✅ O jogo pode começar!";
                resultado.style.color = "green";
            } else if (goleiroPresente === "nao") {
                resultado.textContent =
                    "❌ É necessário um goleiro para começar o jogo.";
                resultado.style.color = "red";
            } else {
                resultado.textContent =
                    "Selecione sim ou não.";
                resultado.style.color = "#b45309";
            }
        }
    </script>
</body>
</html>
