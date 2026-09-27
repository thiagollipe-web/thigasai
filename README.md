# ✦ THIGAS AI // TERMINAL ENGINE v2.0 ✦

Uma interface web retro responsiva no estilo terminal hacker integrada com Inteligência Artificial local via **Ollama**. Projetada para desenvolvimento de código, execução de scripts, e simulação em sandbox em tempo real, com total compatibilidade para dispositivos móveis (Android) e desktop (Windows/Chromebook).

## 🚀 Funcionalidades

- 🤖 **Interface estilo Terminal:** Design hacker estilizado em blocos ASCII/ANSI nas cores verde, ciano e roxo.
- 🎛️ **Seletor Dinâmico de LLMs:** Alterne entre modelos locais (`thigas-ai`, `gemma2:2b`, `qwen2.5-coder:1.5b`) direto pela barra superior.
- 🧠 **Memória Pré-Programada:** Sistema injetado com instruções estritas para o **THIGAS AI** agir como um Engenheiro de Software e Especialista em Jogos.
- 📦 **Sandbox Integrado:** Renderização e teste automático em tempo real de blocos de código gerados no chat em uma janela iframe.
- 🕹️ **Controles Mobile (D-Pad):** Layout com botões virtuais otimizado para o uso através da tela de smartphones.

## 🛠️ Como Configurar o Backend Local

Como a aplicação web roda do lado do cliente (navegador), ela precisa se conectar com a sua instância do Ollama rodando em segundo plano. Siga as instruções para liberar o acesso:

### 1. Permitir conexões externas (CORS)
Por padrão, o Ollama bloqueia requisições vindas de fora. Ative as origens globais antes de inicializar o servidor.

* **No Linux (Chromebook):**
```bash
export OLLAMA_ORIGINS="*"
ollama serve
```

* **No Windows (PowerShell):**
```powershell
$env:OLLAMA_ORIGINS="*"
ollama serve
```

### 2. Sincronizar o IP para uso no Celular
Se você for abrir o link do GitHub Pages pelo celular Android, garanta que o smartphone e o computador estejam conectados na **mesma rede Wi-Fi**:
1. Descubra o IP local do seu computador rodando `hostname -I` no terminal Linux ou `ipconfig` no Windows.
2. No código do seu arquivo `index.html`, altere a linha de requisição de `127.0.0.1` para o IP do seu computador (exemplo: `http://192.168.1`).

## 📁 Estrutura de Arquivos Usada

- `index.html` — Arquivo principal consolidado contendo toda a estrutura HTML, estilização CSS e lógica JavaScript (anteriormente `dev_anabel.html`).
- `Modelfile` — Arquivo de configuração local usado no Ollama para compilar os pesos do arquivo `.gguf` e injetar a personalidade secreta do **THIGAS AI**.
- `iniciar_ia.sh` — Script utilitário em Bash com painel personalizado inspirado no Google Gemini para inicialização rápida no terminal do Chromebook.

## 📄 Licença

Este projeto é de uso pessoal e de código aberto para a comunidade de desenvolvedores independentes.
