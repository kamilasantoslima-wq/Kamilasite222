<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rede de Apoio e Proteção à Mulher</title>
    <style>
        /* --- ESTILOS GERAIS --- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #FFF0F5; /* Rosa claro suave */
            color: #333;
            line-height: 1.6;
        }

        /* --- BOTÃO DE SAÍDA RÁPIDA (SEGURANÇA) --- */
        .saida-rapida {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background-color: #D32F2F;
            color: white;
            padding: 12px 20px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            box-shadow: 0 4px 10px rgba(0,0,0,0.3);
            z-index: 1000;
            transition: transform 0.2s;
        }
        .saida-rapida:hover {
            transform: scale(1.05);
            background-color: #B71C1C;
        }

        /* --- CABEÇALHO --- */
        header {
            background-color: #FFC0CB; /* Rosa claro */
            border-bottom: 4px solid #C71585; /* Rosa escuro */
            padding: 20px;
            text-align: center;
        }

        header h1 {
            color: #8B008B;
            font-size: 24px;
            margin-bottom: 15px;
        }

        /* --- ABAS (NAVEGAÇÃO) --- */
        nav {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 10px;
        }

        .aba-btn {
            background-color: #FFF;
            color: #C71585;
            border: 2px solid #C71585;
            padding: 10px 20px;
            cursor: pointer;
            font-weight: bold;
            border-radius: 20px;
            transition: all 0.3s;
        }

        .aba-btn:hover, .aba-btn.ativa {
            background-color: #C71585;
            color: white;
        }

        /* --- CONTEÚDO DAS ABAS --- */
        .container {
            max-width: 800px;
            margin: 30px auto;
            padding: 0 20px;
        }

        .conteudo-aba {
            display: none; /* Esconde todas as abas por padrão */
            background-color: white;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(199, 21, 133, 0.1);
            animation: fadeIn 0.5s;
        }

        .conteudo-aba.ativa {
            display: block; /* Mostra apenas a aba ativa */
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* --- ESTILIZAÇÃO INTERNA --- */
        h2 {
            color: #C71585;
            margin-bottom: 20px;
            border-bottom: 2px solid #FFC0CB;
            padding-bottom: 10px;
        }

        .imagem-ilustrativa {
            width: 100%;
            max-height: 300px;
            object-fit: cover;
            border-radius: 8px;
            margin-bottom: 20px;
        }

        /* Cartões de canais de ajuda */
        .card-ajuda {
            background-color: #FFF5F7;
            border-left: 5px solid #C71585;
            padding: 15px;
            margin-bottom: 15px;
            border-radius: 4px;
        }

        .card-ajuda strong {
            color: #8B008B;
            font-size: 18px;
        }

        /* Formulário de denúncia anônima */
        .form-grupo {
            margin-bottom: 15px;
        }

        label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
            color: #C71585;
        }

        input[type="text"], textarea, select {
            width: 100%;
            padding: 10px;
            border: 1px solid #FFC0CB;
            border-radius: 6px;
            background-color: #FFF5F7;
        }

        input:focus, textarea:focus, select:focus {
            outline: none;
            border-color: #C71585;
        }

        button[type="submit"] {
            background-color: #C71585;
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 6px;
            cursor: pointer;
            font-weight: bold;
            width: 100%;
        }

        button[type="submit"]:hover {
            background-color: #8B008B;
        }

        /* --- RODAPÉ --- */
        footer {
            text-align: center;
            padding: 20px;
            color: #C71585;
            font-size: 14px;
            margin-top: 40px;
        }
    </style>
</head>
<body>

    <!-- Botão de Segurança: Redireciona para o Google imediatamente se o agressor se aproximar -->
    <a href="https://google.com" class="saida-rapida" onclick="saidaRapida()">SAÍDA RÁPIDA (FECHAR SITE)</a>

    <header>
        <h1>Você Não Está Sozinha • Rede de Apoio</h1>
        <!-- Abas de Navegação -->
        <nav>
            <button class="aba-btn ativa" onclick="abrirAba(event, 'inicio')">Início</button>
            <button class="aba-btn" onclick="abrirAba(event, 'canais')">Canais de Ajuda</button>
            <button class="aba-btn" onclick="abrirAba(event, 'direitos')">Seus Direitos</button>
            <button class="aba-btn" onclick="abrirAba(event, 'relato')">Relato Seguro</button>
        </nav>
    </header>

    <div class="container">

        <!-- ABA: INÍCIO -->
        <div id="inicio" class="conteudo-aba ativa">
            <h2>Acolhimento e Proteção</h2>
            <!-- Imagem conceitual de união feminina -->
            <img src="https://unsplash.com" alt="Mulheres unidas" class="imagem-ilustrativa">
            <p>Este é um espaço seguro criado para informar, acolher e direcionar mulheres que estão passando por situações de violência doméstica ou de gênero.</p>
            <br>
            <p><strong>Importante:</strong> Se você estiver em perigo imediato, ligue diretamente para a polícia (<strong>190</strong>) ou para a Central de Atendimento à Mulher (<strong>180</strong>).</p>
        </div>

        <!-- ABA: CANAIS DE AJUDA -->
        <div id="canais" class="conteudo-aba">
            <h2>Onde Buscar Ajuda</h2>
            <img src="https://unsplash.com" alt="Mulheres conversando" class="imagem-ilustrativa">
            
            <div class="card-ajuda">
                <strong>Ligue 180 - Central de Atendimento</strong>
                <p>Gratuito, confidencial e funciona 24 horas por dia em todo o país.</p>
            </div>

            <div class="card-ajuda">
                <strong>Ligue 190 - Polícia Militar</strong>
                <p>Para casos de emergência e flagrantes de agressão que estão acontecendo agora.</p>
            </div>

            <div class="card-ajuda">
                <strong>DEAM (Delegacia de Atendimento à Mulher)</strong>
                <p>Unidades especializadas da Polícia Civil para registrar boletins de ocorrência e solicitar medidas protetivas.</p>
            </div>
        </div>

        <!-- ABA: SEUS DIREITOS -->
        <div id="direitos" class="conteudo-aba">
            <h2>Conheça a Lei Maria da Penha</h2>
            <img src="https://unsplash.com" alt="Direitos da mulher" class="imagem-ilustrativa">
            <p>A violência contra a mulher não é apenas física. A legislação brasileira reconhece cinco tipos principais de violência doméstica:</p>
            <br>
            <ul>
                <li><strong>Física:</strong> Ofensas à integridade ou saúde corporal.</li>
                <li><strong>Psicológica:</strong> Humilhação, isolamento, ameaças ou controle de comportamento.</li>
                <li><strong>Sexual:</strong> Presenciar, manter ou participar de relação sexual não desejada mediante coerção.</li>
                <li><strong>Patrimonial:</strong> Retenção, subtração ou destruição de objetos, instrumentos de trabalho e bens.</li>
                <li><strong>Moral:</strong> Calúnia, difamação ou injúria.</li>
            </ul>
        </div>

        <!-- ABA: RELATO SEGURO -->
        <div id="relato" class="conteudo-aba">
            <h2>Relato Seguro e Anônimo</h2>
            <p>Use este formulário para enviar um pedido de ajuda ou relatar seu caso. Suas informações estarão protegidas e você pode escolher não se identificar.</p>
            <br>
            <form id="formDenuncia" onsubmit="enviarFormulario(event)">
                <div class="form-grupo">
                    <label for="nome">Seu Nome (Opcional):</label>
                    <input type="text" id="nome" placeholder="Deixe em branco para anonimato">
                </div>
                <div class="form-grupo">
                    <label for="tipo">Tipo de Apoio Necessário:</label>
                    <select id="tipo" required>
                        <option value="">Selecione...</option>
                        <option value="juridico">Orientação Jurídica</option>
                        <option value="psicologico">Apoio Psicológico</option>
                        <option value="abrigo">Informações sobre Abrigos</option>
                        <option value="outro">Outros</option>
                    </select>
                </div>
                <div class="form-grupo">
                    <label for="mensagem">Mensagem / Relato:</label>
                    <textarea id="mensagem" rows="5" required placeholder="Conte-nos como podemos te apoiar..."></textarea>
                </div>
                <button type="submit">Enviar Pedido de Ajuda</button>
            </form>
        </div>

    </div>

    <footer>
