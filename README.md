```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cyber Security | Tema Integrador</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        cyber: {
                            dark: '#050A18',
                            darker: '#020510',
                            blue: '#009ED9',
                            purple: '#6B21D9',
                            red: '#E02040',
                            green: '#00C860',
                            gray: '#10172A',
                            light: '#E6E6F2',
                            white: '#F8FAFC',
                            orange: '#F59E0B',
                        },
                    },
                    fontFamily: {
                        cyber: ['sans-serif'],
                        sans: ['system-ui', 'sans-serif'],
                    },
                    animation: {
                        'pulse-slow': 'pulse 3s cubic-bezier(0.4, 0, 0.6, 1) infinite',
                    }
                }
            }
        }
    </script>
    <link rel="stylesheet" href="estilos.css">
</head>
<body class="bg-cyber-dark text-cyber-light transition-colors duration-300">
    <div id="bgGrid" class="fixed inset-0 grid-bg opacity-40 pointer-events-none z-0"></div>

    <!-- BOTÃO DE ACESSIBILIDADE -->
    <button id="accessibilityToggle" class="fixed bottom-6 right-6 z-[100] w-14 h-14 rounded-full bg-cyber-blue/30 border-2 border-cyber-blue flex items-center justify-center text-cyber-blue text-2xl hover:bg-cyber-blue/50 transition-all focus-outline shadow-lg cursor-pointer" aria-label="Abrir painel de acessibilidade">
        <i class="fa fa-universal-access"></i>
    </button>

    <!-- PAINEL DE ACESSIBILIDADE -->
    <div id="accessibilityPanel" class="fixed bottom-24 right-6 z-[100] w-80 bg-cyber-gray/95 border-glow rounded-xl p-5 backdrop-blur-md hidden transition-all duration-300">
        <h3 class="text-xl font-bold text-cyber-blue mb-4 text-center">♿ Acessibilidade</h3>
        <div class="space-y-3">
            <button id="btnFontSize" class="w-full py-3 px-4 rounded-lg border border-cyber-blue/50 text-left flex items-center gap-3 hover:bg-cyber-blue/10 transition focus-outline">
                <i class="fa fa-text-height text-cyber-blue"></i>
                <span>Aumentar Fonte</span>
                <span id="fontStatus" class="ml-auto text-xs px-2 py-0.5 rounded-full bg-gray-700">OFF</span>
            </button>
            <button id="btnContrast" class="w-full py-3 px-4 rounded-lg border border-cyber-purple/50 text-left flex items-center gap-3 hover:bg-cyber-purple/10 transition focus-outline">
                <i class="fa fa-adjust text-cyber-purple"></i>
                <span>Modo Alto Contraste</span>
                <span id="contrastStatus" class="ml-auto text-xs px-2 py-0.5 rounded-full bg-gray-700">OFF</span>
            </button>
            <button id="btnTheme" class="w-full py-3 px-4 rounded-lg border border-cyber-green/50 text-left flex items-center gap-3 hover:bg-cyber-green/10 transition focus-outline">
                <i id="themeIcon" class="fa fa-sun-o text-cyber-green"></i>
                <span id="themeText">Modo Claro</span>
                <span id="themeStatus" class="ml-auto text-xs px-2 py-0.5 rounded-full bg-gray-700">OFF</span>
            </button>
            <button id="btnSpeak" class="w-full py-3 px-4 rounded-lg border border-cyber-red/50 text-left flex items-center gap-3 hover:bg-cyber-red/10 transition focus-outline">
                <i class="fa fa-volume-up text-cyber-red"></i>
                <span>Leitor de Voz</span>
                <span id="speakStatus" class="ml-auto text-xs px-2 py-0.5 rounded-full bg-gray-700">OFF</span>
            </button>
            <button id="btnZoom" class="w-full py-3 px-4 rounded-lg border border-cyber-orange/50 text-left flex items-center gap-3 hover:bg-cyber-orange/10 transition focus-outline">
                <i class="fa fa-search-plus text-cyber-orange"></i>
                <span>Zoom</span>
                <span id="zoomStatus" class="ml-auto text-xs px-2 py-0.5 rounded-full bg-gray-700">OFF</span>
            </button>
        </div>
    </div>

    <!-- NAVEGAÇÃO -->
    <nav class="fixed top-0 left-0 right-0 z-40 bg-cyber-darker/80 backdrop-blur-md border-b border-cyber-blue/20 transition-colors duration-300">
        <div class="container mx-auto px-4 py-3 flex items-center justify-between">
            <div class="flex items-center gap-3">
                <div class="w-10 h-10 rounded-lg bg-cyber-blue/20 flex items-center justify-center text-cyber-blue text-xl">
                    <i class="fa fa-shield"></i>
                </div>
                <span class="font-bold text-lg text-cyber-blue">CYBER SECURITY</span>
            </div>
            <div class="hidden md:flex items-center gap-6 text-sm">
                <a href="#inicio" class="hover:text-cyber-blue transition">Início</a>
                <a href="#projeto" class="hover:text-cyber-blue transition">Projeto</a>
                <a href="#trilha" class="hover:text-cyber-blue transition">Trilha</a>
                <a href="#mercado" class="hover:text-cyber-blue transition">Mercado</a>
                <a href="#etica" class="hover:text-cyber-blue transition">Ética</a>
                <a href="#historias" class="hover:text-cyber-blue transition">Histórias</a>
                <a href="#referencias" class="hover:text-cyber-blue transition">Referências</a>
                <a href="#dicas" class="hover:text-cyber-blue transition">Segurança</a>
                <a href="#casos" class="hover:text-cyber-blue transition">Casos Reais</a>
            </div>
        </div>
    </nav>

    <!-- CONTEÚDO PRINCIPAL -->
    <main id="mainContent" class="pt-24 pb-32 relative z-10 transition-transform duration-300">
        <div class="container mx-auto px-4 max-w-5xl">

            <!-- INÍCIO -->
            <section id="inicio" class="min-h-[80vh] flex flex-col items-center justify-center text-center py-20">
                <div class="w-20 h-20 rounded-full bg-cyber-blue/10 flex items-center justify-center text-cyber-blue text-4xl mb-8 animate-pulse-slow">
                    <i class="fa fa-shield"></i>
                </div>
                <h1 class="text-4xl md:text-6xl font-bold mb-6 bg-gradient-to-r from-cyber-blue to-cyber-purple bg-clip-text text-transparent">CYBER SECURITY</h1>
                <p class="text-xl md:text-2xl mb-4 text-cyber-blue/80">Plataforma Educacional de Cibersegurança</p>
                <p class="text-lg max-w-2xl mb-8 text-gray-300">Tema Integrador – Gestão de Carreira</p>
                
                <div class="flex flex-col sm:flex-row gap-4 mb-12">
                    <div class="px-6 py-3 border-glow rounded-lg bg-cyber-gray/30">
                        <span class="text-cyber-blue font-semibold">Matheus de Souza Gonçalves</span>
                    </div>
                    <div class="px-6 py-3 border-glow rounded-lg bg-cyber-gray/30">
                        <span class="text-cyber-purple font-semibold">Débora Cristina Soares Ribeiro</span>
                    </div>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mt-12 w-full max-w-3xl">
                    <div class="p-5 border-glow rounded-xl bg-cyber-gray/20 hover:bg-cyber-green/5 transition-all">
                        <h3 class="text-cyber-green font-bold mb-2">ODS 8</h3>
                        <p class="text-sm">Trabalho Decente e Crescimento Econômico</p>
                    </div>
                    <div class="p-5 border-glow rounded-xl bg-cyber-gray/20 hover:bg-cyber-blue/5 transition-all">
                        <h3 class="text-cyber-blue font-bold mb-2">ODS 9</h3>
                        <p class="text-sm">Indústria, Inovação e Infraestrutura</p>
                    </div>
                    <div class="p-5 border-glow rounded-xl bg-cyber-gray/20 hover:bg-cyber-red/5 transition-all">
                        <h3 class="text-cyber-red font-bold mb-2">ODS 10</h3>
                        <p class="text-sm">Redução das Desigualdades</p>
                    </div>
                </div>
                <div class="mt-16 text-cyber-blue/50">
                    <i class="fa fa-angle-down text-2xl"></i>
                </div>
            </section>

            <!-- PROJETO -->
            <section id="projeto" class="py-20">
                <h2 class="text-3xl font-bold mb-12 text-center text-cyber-blue"><span class="text-glow">// IDENTIFICAÇÃO E ESCOPO</span></h2>
                <div class="space-y-10">
                    <div class="p-6 border-glow rounded-xl bg-cyber-gray/10">
                        <h3 class="text-xl font-bold text-cyber-green mb-4">🎯 Público-Alvo</h3>
                        <p>Microempreendedores locais, profissionais autônomos, ONGs e associações comunitárias sem fins lucrativos. Agentes sociais e pequenos negócios que necessitam de maior visibilidade digital e normalmente não possuem recursos para contratar desenvolvimento web profissional.</p>
                    </div>
                    <div class="p-6 border-glow rounded-xl bg-cyber-gray/10">
                        <h3 class="text-xl font-bold text-cyber-purple mb-4">🌐 Área de Atuação</h3>
                        <p>Desenvolvimento Web, Engenharia de Requisitos, Tecnologia da Informação e Transformação Digital Comunitária. Combinando IA generativa e versionamento de código com Git/GitHub para impacto social e econômico local.</p>
                    </div>
                    <div class="p-6 border-glow rounded-xl bg-cyber-gray/10">
                        <h3 class="text-xl font-bold text-cyber-blue mb-4">📌 Sobre a Plataforma</h3>
                        <p><strong>Cyber Security</strong> — uma plataforma educacional que instrui sobre a área de cibersegurança, mostrando sua evolução, áreas de crescimento e pontos essenciais.</p>
                    </div>
                </div>
            </section>

            <!-- TRILHA DE APRENDIZAGEM -->
            <section id="trilha" class="py-20">
                <h2 class="text-3xl font-bold mb-12 text-center text-cyber-blue"><span class="text-glow">// TRILHA DE APRENDIZAGEM</span></h2>
                <div class="space-y-10">
                    <div class="p-6 border-glow rounded-xl bg-cyber-gray/10 border-l-4 border-cyber-green">
                        <h3 class="text-xl font-bold text-cyber-green mb-4">🟢 FASE 1 — Básica: Fundamentos e Infraestrutura</h3>
                        <ul class="space-y-2 ml-4 list-disc">
                            <li><strong>Redes e Protocolos:</strong> TCP/IP, modelo OSI, DNS, HTTP/HTTPS, portas</li>
                            <li><strong>Sistemas Operacionais:</strong> Linux (comandos, permissões), Windows Server, Active Directory</li>
                            <li><strong>Segurança Teórica:</strong> Tríade CIA, criptografia básica, controle de acesso</li>
                        </ul>
                    </div>
                    <div class="p-6 border-glow rounded-xl bg-cyber-gray/10 border-l-4 border-cyber-blue">
                        <h3 class="text-xl font-bold text-cyber-blue mb-4">🔵 FASE 2 — Intermediária: Ataque e Defesa</h3>
                        <ul class="space-y-2 ml-4 list-disc">
                            <li><strong>Automação:</strong> Python e Bash</li>
                            <li><strong>Segurança Ofensiva:</strong> OWASP Top 10, Nmap, Burp Suite, Metasploit — TryHackMe</li>
                            <li><strong>Segurança Defensiva:</strong> SOC, monitoramento de logs, SIEM, hardening</li>
                            <li><strong>Marco:</strong> CompTIA Security+</li>
                        </ul>
                    </div>
                    <div class="p-6 border-glow rounded-xl bg-cyber-gray/10 border-l-4 border-cyber-red">
                        <h3 class="text-xl font-bold text-cyber-red mb-4">🔴 FASE 3 — Avançada: Especialização</h3>
                        <ul class="space-y-2 ml-4 list-disc">
                            <li><strong>DFIR:</strong> Forense digital, resposta a incidentes, engenharia reversa de malware</li>
                            <li><strong>Cloud Security:</strong> AWS/Azure, Zero Trust, DevSecOps</li>
                            <li><strong>Elite:</strong> Red Teaming avançado — OSCP, CISSP</li>
                        </ul>
                    </div>
                </div>
            </section>

            <!-- MERCADO DE TRABALHO -->
            <section id="mercado" class="py-20">
                <h2 class="text-3xl font-bold mb-12 text-center text-cyber-blue"><span class="text-glow">// MERCADO DE TRABALHO</span></h2>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-12">
                    <div class="p-5 border-glow rounded-xl bg-cyber-gray/10">
                        <h4 class="font-bold text-cyber-blue mb-2">🛡️ Blue Team</h4>
                        <p class="text-sm mb-2">Defesa cibernética, SOC, monitoramento de ameaças</p>
                        <span class="text-xs text-cyber-green">Cert: Security+, CySA+</span>
                    </div>
                    <div class="p-5 border-glow rounded-xl bg-cyber-gray/10">
                        <h4 class="font-bold text-cyber-red mb-2">⚔️ Red Team / Pentest</h4>
                        <p class="text-sm mb-2">Simulação de ataques, vulnerabilidades</p>
                        <span class="text-xs text-cyber-green">Cert: eJPT, OSCP, PNPT</span>
                    </div>
                    <div class="p-5 border-glow rounded-xl bg-cyber-gray/10">
                        <h4 class="font-bold text-cyber-purple mb-2">☁️ Cloud Security</h4>
                        <p class="text-sm mb-2">Segurança em nuvem, DevSecOps</p>
                        <span class="text-xs text-cyber-green">Cert: AWS Security, CCSP</span>
                    </div>
                    <div class="p-5 border-glow rounded-xl bg-cyber-gray/10">
                        <h4 class="font-bold text-cyber-green mb-2">📋 GRC</h4>
                        <p class="text-sm mb-2">Governança, Risco e Conformidade — ISO 27001, LGPD</p>
                        <span class="
