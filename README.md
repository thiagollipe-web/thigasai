# ✦ THIGAS A.I // BROWSER ENGINE v3.7 ✦

Um motor de terminal interativo executado inteiramente no navegador web. Este projeto funde uma interface de linha de comandos (CLI) de inspiração retro com capacidades de Inteligência Artificial local e um ecrã de renderização gráfica (*Canvas*), perfeitamente otimizado para dispositivos móveis.

## 🚀 Visão Geral

O THIGAS A.I Terminal Engine foi concebido para ser uma ferramenta leve, responsiva e poderosa para a experimentação de algoritmos, desenvolvimento de mecânicas de jogos digitais e interação com modelos de linguagem de grande escala (LLMs) sem necessidade de ligação a servidores externos para o processamento de texto. 

A interface divide-se de forma dinâmica: apresenta o terminal de comandos e, simultaneamente, um ambiente gráfico limpo (`<canvas>`), preparando o terreno para a programação visual e desenvolvimento de lógicas de jogo.

## ✨ Funcionalidades

*   **Processamento de IA Local:** Integração com a biblioteca Hugging Face `Transformers.js`, permitindo descarregar e correr modelos (como o SmolLM2) diretamente na RAM/VRAM do dispositivo através de WebAssembly e WebGPU.
*   **Otimização Mobile-First:** 
    *   Design responsivo utilizando `100dvh` para evitar conflitos com teclados virtuais e barras de navegação em telemóveis.
    *   Controlos D-Pad integrados na interface com eventos `onpointerdown` para eliminar o atraso tátil de 300ms, ideal para controlo de jogos digitais.
    *   Bloqueio inteligente de ampliação (zoom) acidental no ecrã.
*   **Renderização de Terminal Autêntica:**
    *   Preservação estrutural de arte ASCII.
    *   Motor personalizado de interpretação (Parsing) de códigos de escape ANSI, convertendo cores de terminal reais em estilos HTML dinâmicos.
*   **Ecrã Gráfico Integrado:** Um elemento HTML5 Canvas maximizado, pronto para receber renderizações gráficas 2D e rotinas de jogos.

## 🛠️ Tecnologias Utilizadas

*   **HTML5 & CSS3:** Estrutura da interface, tipografia monospace, variáveis de cor dinâmicas e layouts flexíveis (`Flexbox` e `Grid`).
*   **JavaScript (ES6+):** Lógica assíncrona (`async/await`), manipulação do DOM e interceptação de eventos de ponteiro.
*   **Transformers.js:** Pipeline de processamento de inferência de LLMs em ambiente cliente.
*   **HTML5 Canvas API:** Superfície de desenho preparada para a prototipagem gráfica.

## 📦 Como Instalar e Executar

Sendo uma *Single Page Application* (SPA) baseada em tecnologias cliente, a implementação é direta:

1. **Clone o repositório** ou faça o download dos ficheiros.
2. Devido às políticas de segurança dos navegadores modernos (CORS) e aos requisitos da biblioteca `Transformers.js`, não é recomendado abrir o ficheiro clicando diretamente nele (`file://`).
3. **Inicie um servidor local.** Se utilizar o Visual Studio Code, a extensão *Live Server* é a opção mais rápida. Alternativamente, utilize o Python através da linha de comandos na pasta do projeto:
   ```bash
   python -m http.server 8000
