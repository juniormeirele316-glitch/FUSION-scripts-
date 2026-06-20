<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FUSION SCRIPTS</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(180deg, #f5f5f5 0%, #ffffff 100%);
            min-height: 100vh;
            padding: 20px;
            color: #1f2937;
        }

        .container {
            max-width: 600px;
            margin: 0 auto;
        }

        /* PÁGINA INICIAL */
        .home-page {
            display: block;
        }

        .home-page.hidden {
            display: none;
        }

        .header {
            text-align: center;
            margin-bottom: 30px;
        }

        .logo-section {
            margin-bottom: 30px;
        }

        .character {
            width: 120px;
            height: 120px;
            margin: 0 auto 20px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 60px;
            box-shadow: 0 8px 24px rgba(102, 126, 234, 0.3);
        }

        .title {
            font-size: 32px;
            font-weight: 700;
            margin-bottom: 10px;
            text-align: center;
        }

        .title span {
            color: #667eea;
        }

        .description {
            text-align: center;
            color: #6b7280;
            font-size: 14px;
            line-height: 1.6;
            margin-bottom: 30px;
        }

        .stats {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 12px;
            margin-bottom: 20px;
        }

        .stat-card {
            background: white;
            padding: 15px;
            border-radius: 10px;
            text-align: center;
            border: 1px solid #e5e7eb;
        }

        .stat-number {
            font-size: 20px;
            font-weight: 700;
            color: #667eea;
            margin-bottom: 4px;
        }

        .stat-label {
            font-size: 12px;
            color: #6b7280;
        }

        .info-box {
            background: #f0f4ff;
            border-left: 4px solid #667eea;
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 20px;
        }

        .info-box p {
            font-size: 13px;
            color: #1f2937;
            line-height: 1.6;
        }

        .features {
            background: white;
            border-radius: 12px;
            padding: 20px;
            margin-bottom: 20px;
            border: 1px solid #e5e7eb;
        }

        .feature-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 15px;
            gap: 12px;
        }

        .feature-item:last-child {
            margin-bottom: 0;
        }

        .feature-icon {
            width: 24px;
            height: 24px;
            background: #dbeafe;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #667eea;
            font-size: 12px;
            font-weight: bold;
            flex-shrink: 0;
            margin-top: 2px;
        }

        .feature-text h3 {
            font-size: 14px;
            font-weight: 600;
            margin-bottom: 2px;
            color: #1f2937;
        }

        .feature-text p {
            font-size: 12px;
            color: #6b7280;
        }

        .cta-button {
            display: block;
            width: 100%;
            padding: 14px 20px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border: none;
            border-radius: 10px;
            font-size: 14px;
            font-weight: 600;
            cursor: pointer;
            margin-bottom: 12px;
            transition: transform 0.2s ease, box-shadow 0.2s ease;
            text-decoration: none;
            text-align: center;
        }

        .cta-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 20px rgba(102, 126, 234, 0.4);
        }

        /* PÁGINA SCRIPTS */
        .scripts-page {
            display: none;
        }

        .scripts-page.active {
            display: block;
        }

        .back-button {
            background: white;
            color: #667eea;
            border: 2px solid #667eea;
            padding: 10px 16px;
            border-radius: 8px;
            font-size: 12px;
            font-weight: 600;
            cursor: pointer;
            margin-bottom: 20px;
            transition: all 0.2s ease;
        }

        .back-button:hover {
            background: #f0f4ff;
        }

        .scripts-header {
            text-align: center;
            margin-bottom: 30px;
        }

        .scripts-header h1 {
            font-size: 28px;
            font-weight: 700;
            margin-bottom: 8px;
        }

        .scripts-header h1 span {
            color: #667eea;
        }

        .scripts-header p {
            color: #6b7280;
            font-size: 13px;
        }

        .section-title {
            font-size: 14px;
            font-weight: 600;
            color: #1f2937;
            margin-bottom: 16px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .script-item {
            background: white;
            border: 1px solid #e5e7eb;
            border-radius: 10px;
            padding: 16px;
            margin-bottom: 12px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 12px;
        }

        .script-info {
            flex: 1;
        }

        .script-name {
            font-size: 14px;
            font-weight: 600;
            color: #1f2937;
            margin-bottom: 4px;
        }

        .script-code {
            font-size: 12px;
            color: #6b7280;
            font-family: 'Courier New', monospace;
            background: #f3f4f6;
            padding: 8px;
            border-radius: 6px;
            word-break: break-all;
        }

        .copy-btn {
            padding: 10px 16px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border: none;
            border-radius: 8px;
            font-size: 12px;
            font-weight: 600;
            cursor: pointer;
            white-space: nowrap;
            transition: all 0.3s ease;
            flex-shrink: 0;
        }

        .copy-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(102, 126, 234, 0.4);
        }

        .copy-btn:disabled {
            cursor: not-allowed;
            opacity: 0.8;
        }

        .copy-btn.copied {
            background: #10b981;
            color: white;
            font-weight: 700;
        }

        .footer {
            text-align: center;
            color: #9ca3af;
            font-size: 12px;
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px solid #e5e7eb;
        }

        .alert {
            display: none;
            position: fixed;
            top: 20px;
            right: 20px;
            background: #10b981;
            color: white;
            padding: 12px 20px;
            border-radius: 8px;
            font-size: 14px;
            animation: slideIn 0.3s ease;
            z-index: 1000;
        }

        @keyframes slideIn {
            from {
                transform: translateX(400px);
                opacity: 0;
            }
            to {
                transform: translateX(0);
                opacity: 1;
            }
        }

        .badge {
            display: inline-block;
            background: #dbeafe;
            color: #667eea;
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 11px;
            font-weight: 600;
            margin-bottom: 20px;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- PÁGINA INICIAL -->
        <div id="homePage" class="home-page">
            <div class="header">
                <div class="badge">✓ ATUALIZADO</div>
                
                <div class="logo-section">
                    <div class="character">⚡</div>
                    <h1 class="title">FUSION <span>SCRIPTS</span></h1>
                </div>

                <p class="description">
                    Os melhores scripts para seus projetos.<br>
                    Simples, rápido e confiável.
                </p>
            </div>

            <div class="stats">
                <div class="stat-card">
                    <div class="stat-number">100%</div>
                    <div class="stat-label">Funcional</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">5</div>
                    <div class="stat-label">Scripts</div>
                </div>
            </div>

            <div class="info-box">
                <p><strong>🚀 Novidade:</strong> Todos os scripts atualizados e otimizados para máximo desempenho!</p>
            </div>

            <div class="features">
                <div class="feature-item">
                    <div class="feature-icon">✓</div>
                    <div class="feature-text">
                        <h3>Scripts Testados</h3>
                        <p>Códigos validados e confiáveis</p>
                    </div>
                </div>
                <div class="feature-item">
                    <div class="feature-icon">⚙</div>
                    <div class="feature-text">
                        <h3>Fácil Integração</h3>
                        <p>Pronto para usar em seus projetos</p>
                    </div>
                </div>
                <div class="feature-item">
                    <div class="feature-icon">🔄</div>
                    <div class="feature-text">
                        <h3>Sempre Atualizado</h3>
                        <p>Novas versões regularmente</p>
                    </div>
                </div>
            </div>

            <button class="cta-button" onclick="mostrarScripts()">Acessar Scripts</button>

            <div class="footer">
                <p>FUSION SCRIPTS © 2024</p>
                <p>Desenvolvido com ❤️</p>
            </div>
        </div>

        <!-- PÁGINA SCRIPTS -->
        <div id="scriptsPage" class="scripts-page">
            <button class="back-button" onclick="voltarHome()">← Voltar</button>

            <div class="scripts-header">
                <h1>FUSION <span>SCRIPTS</span></h1>
                <p>✅🔥🚀 Os Melhores Scripts Para Blox Fruits - Só Copiar e Colar!</p>
            </div>

            <div class="section-title">📜 Scripts Disponíveis</div>

            <div class="script-item">
                <div class="script-info">
                    <div class="script-name">Bacon Hub</div>
                    <div class="script-code">loadstring(game:HttpGet("https://raw.githubusercontent.com/vinh129150/hack/refs/heads/main/BaconHub.lua"))()</div>
                </div>
                <button class="copy-btn" data-script='loadstring(game:HttpGet("https://raw.githubusercontent.com/vinh129150/hack/refs/heads/main/BaconHub.lua"))()' onclick="copiar(this)">📋 Copiar</button>
            </div>

            <div class="script-item">
                <div class="script-info">
                    <div class="script-name">Leaf Hub</div>
                    <div class="script-code">loadstring(game:HttpGet("https://github.com/LeafHubAcademy/LeafHub/raw/refs/heads/main/Leaf.lua"))()</div>
                </div>
                <button class="copy-btn" data-script='loadstring(game:HttpGet("https://github.com/LeafHubAcademy/LeafHub/raw/refs/heads/main/Leaf.lua"))()' onclick="copiar(this)">📋 Copiar</button>
            </div>

            <div class="script-item">
                <div class="script-info">
                    <div class="script-name">Redz Hub</div>
                    <div class="script-code">loadstring(game:HttpGet("https://raw.githubusercontent.com/huy384/redzHub/refs/heads/main/redzHub.lua"))()</div>
                </div>
                <button class="copy-btn" data-script='loadstring(game:HttpGet("https://raw.githubusercontent.com/huy384/redzHub/refs/heads/main/redzHub.lua"))()' onclick="copiar(this)">📋 Copiar</button>
            </div>

            <div class="script-item">
                <div class="script-info">
                    <div class="script-name">MoonLight</div>
                    <div class="script-code">loadstring(game:HttpGet("https://raw.githubusercontent.com/Dev-Moonlight/Moonlight/refs/heads/main/Main"))()</div>
                </div>
                <button class="copy-btn" data-script='loadstring(game:HttpGet("https://raw.githubusercontent.com/Dev-Moonlight/Moonlight/refs/heads/main/Main"))()' onclick="copiar(this)">📋 Copiar</button>
            </div>

            <div class="script-item">
                <div class="script-info">
                    <div class="script-name">Gravity Hub</div>
                    <div class="script-code">loadstring(game:HttpGet("https://raw.githubusercontent.com/Dev-GravityHub/BloxFruit/refs/heads/main/Main.lua"))()</div>
                </div>
                <button class="copy-btn" data-script='loadstring(game:HttpGet("https://raw.githubusercontent.com/Dev-GravityHub/BloxFruit/refs/heads/main/Main.lua"))()' onclick="copiar(this)">📋 Copiar</button>
            </div>

            <div class="footer">
                <p>FUSION SCRIPTS © 2024</p>
                <p>Scripts copiados com sucesso!</p>
            </div>
        </div>
    </div>

    <div class="alert" id="alert">✓ Copiado para a área de transferência!</div>

    <script>
        function mostrarScripts() {
            console.log('Mostrando scripts');
            document.getElementById('homePage').classList.add('hidden');
            document.getElementById('scriptsPage').classList.add('active');
        }

        function voltarHome() {
            console.log('Voltando para home');
            document.getElementById('homePage').classList.remove('hidden');
            document.getElementById('scriptsPage').classList.remove('active');
        }

        function copiar(botao) {
            // Pegar o texto do atributo data-script
            let texto = botao.getAttribute('data-script');
            
            if (!texto) {
                alert('Erro: script não encontrado');
                return;
            }

            // Tentar copiar com Clipboard API (moderno)
            if (navigator.clipboard) {
                navigator.clipboard.writeText(texto).then(() => {
                    mudarBotao(botao);
                }).catch(err => {
                    // Fallback para método antigo
                    copiarAntigo(texto, botao);
                });
            } else {
                // Fallback para método antigo
                copiarAntigo(texto, botao);
            }
        }

        function copiarAntigo(texto, botao) {
            // Criar textarea temporário
            const textarea = document.createElement('textarea');
            textarea.value = texto;
            document.body.appendChild(textarea);
            textarea.select();
            
            try {
                document.execCommand('copy');
                mudarBotao(botao);
            } catch (err) {
                alert('Erro ao copiar!');
            }
            
            document.body.removeChild(textarea);
        }

        function mudarBotao(botao) {
            const textoOriginal = botao.textContent;
            botao.textContent = 'Copiado!';
            botao.classList.add('copied');
            botao.disabled = true;

            const alert = document.getElementById('alert');
            alert.style.display = 'block';

            setTimeout(() => {
                botao.textContent = textoOriginal;
                botao.classList.remove('copied');
                botao.disabled = false;
                alert.style.display = 'none';
            }, 3000);
        }
    </script>
</body>
</html># FUSION-scripts-
