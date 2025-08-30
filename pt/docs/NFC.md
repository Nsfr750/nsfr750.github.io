---
lang: pt
lang-niv: fonto
lang-ref: 016-jbk
layout: doc
order: 7
title: 'NFC'
---

# 🚀 Aplicativo Leitor/Gravador NFC

[![Licença: GPL v3](https://img.shields.io/badge/Licença-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![Estilo de código: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

Um poderoso aplicativo baseado em PySide6 para ler e gravar em vários tipos de tags NFC com recursos avançados e interface amigável.

## Instalação

### Pré-requisitos

- Python 3.9 ou superior
- Hardware leitor NFC (ACR122U, ACR1252U, etc.)

### Início Rápido

1. Clone o repositório:

   ```bash
   git clone https://github.com/Nsfr750/NFC.git
   cd NFC
   ```

2. Crie e ative um ambiente virtual:

   ```bash
   python -m venv venv
   .\venv\Scripts\activate  # Windows
   source venv/bin/activate  # Linux/Mac
   ```

3. Instale as dependências:

   ```bash
   pip install -r requirements.txt
   ```

4. Execute o aplicativo:

   ```bash
   python main.py
   ```

Para instruções detalhadas de instalação, consulte [PRÉ-REQUISITOS.md](PRÉ-REQUISITOS.md).

## Recursos

- **Suporte Multi-tags**: Suporte abrangente para vários tipos de tags NFC, incluindo:
  - NTAG (NTAG213, NTAG215, NTAG216)
  - MIFARE Classic (1K, 4K)
  - MIFARE Ultralight
  - FeliCa (Sony)
  - Cartões ISO 14443 Tipo A/B

- **Suporte Completo a Tags**: [Ver operações suportadas](docs/supported_operations.md) para todos os tipos de tags

- **Operações NDEF**:
  - Ler e gravar registros NDEF
  - Criar e gerenciar múltiplos registros NDEF
  - Suporte para vários tipos de registros NDEF (Texto, URI, Smart Poster, etc.)
  - Visualização hexadecimal para inspeção de dados brutos

- **Gerenciamento de Tags**:
  - Ler informações da tag (UID, layout de memória, capacidades)
  - Gravar dados em tags com validação
  - Bloquear tags para evitar gravações não autorizadas
  - Formatar tags para uso NDEF

- **Interface do Usuário**:
  - Design moderno e responsivo com sphinx_rtd_theme
  - Suporte a temas Claro/Escuro/Sistema
  - Detecção de tags em tempo real e atualizações de status
  - Painel detalhado de informações da tag
  - Visualizador de logs com opções de filtragem
  - Documentação abrangente em inglês e italiano

- **Recursos de Segurança**:
  - 🔒 Proteção por senha para operações sensíveis
  - 🔑 Hash seguro de senha com PBKDF2
  - 🔄 Funcionalidade de alteração de senha
  - ⚙️ Alternar para ativar/desativar proteção por senha
  - 🔐 Operações protegidas incluem Ferramentas de Tag, Banco de Dados e Clonador

- **Recursos Avançados**:
  - Modo de emulação de tag (experimental)
  - Operações em lote para processar múltiplas tags
  - Execução de comandos personalizados
  - Sistema de log com múltiplos níveis de detalhamento
  - Documentação da API para desenvolvedores
  - Guia de solução de problemas para questões comuns
  - Diretrizes de contribuição para colaboração em código aberto

## 🚀 Requisitos

- Python 3.8 ou superior
- Leitor/Gravador NFC compatível:
  - ACR122U
  - PN532 (via USB/UART)
  - Leitores compatíveis com PC/SC
- Windows 10/11 ou Linux com suporte a PC/SC
- Pacotes Python necessários (ver `requirements.txt`)

## 📖 Documentação

Documentação abrangente está disponível em inglês e italiano, incluindo:

- Guia do Usuário
- Referência da API
- Guia de Solução de Problemas
- Perguntas Frequentes
- Diretrizes de Contribuição

Para construir a documentação localmente:

```bash
# Instalar requisitos de documentação
pip install -r requirements-docs.txt

# Construir documentação em português
cd docs/POR
make html
```

A documentação estará disponível no diretório `_build/html` da pasta de cada idioma.

## 📦 Instalação

1. Clone este repositório:

   ```bash
   git clone https://github.com/Nsfr750/NFC.git
   cd NFC
   ```

2. Crie e ative um ambiente virtual (recomendado):

   ```bash
   # Windows
   python -m venv venv
   .\venv\Scripts\activate

   # Linux/macOS
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Instale os pacotes necessários:

   ```bash
   pip install -r requirements.txt
   ```

4. (Opcional) Instale os drivers PC/SC se ainda não estiverem instalados:
   - Windows: Instale [drivers CCID](https://ccid.apdu.fr/)
   - Linux: Instale os pacotes `pcscd` e `libpcsclite-dev`

5. Execute o aplicativo:

   ```bash
   python main.py
   ```

## 🚀 Como Usar

### Operações Básicas

1. **Conecte seu leitor NFC**
   - O aplicativo detectará automaticamente dispositivos suportados
   - O status da conexão é mostrado na barra de status

2. **Leia uma tag**
   - Aproxime uma tag NFC do leitor
   - As informações da tag serão exibidas na janela principal
   - Visualize o layout de memória detalhado no editor hexadecimal

3. **Grave em uma tag**
   - Navegue até a aba "Gravar"
   - Selecione o tipo de registro (Texto, URI, etc.)
   - Digite seu conteúdo e clique em "Gravar na Tag"

4. **Bloqueie uma tag**
   - Use o botão "Bloquear" para evitar gravações futuras
   - Algumas tags suportam bloqueio permanente (tenha cuidado!)

### 🛠️ Recursos Avançados

- **Emulação de Tag**: Emule uma tag NFC (experimental)
- **Comandos Personalizados**: Envie comandos APDU brutos para a tag
- **Visualização de Memória**: Inspecione e edite a memória bruta da tag
- **Registros**: Visualize registros detalhados de operações com opções de filtragem

### ⚙️ Configurações

Acesse as configurações em `Ferramentas > Configurações` ou pressione `Ctrl+,`:

- **Geral**:
  - Conectar automaticamente na inicialização
  - Seleção de idioma
  - Verificar atualizações

- **NFC**:
  - Tempo limite do leitor
  - Leitura automática na detecção de tag
  - Som ao detectar tag

- **Interface**:
  - Tema (Claro/Escuro/Sistema)
  - Tamanho e família da fonte
  - Comportamento da janela

- **Avançado**:
  - Nível de log
  - Comandos personalizados
  - Opções de desenvolvedor

### ⌨️ Atalhos de Teclado

| Atalho       | Ação                     |
|-------------|--------------------------|
| `Ctrl+N`    | Novo projeto             |
| `Ctrl+A`    | Abrir arquivo            |
| `Ctrl+S`    | Salvar dados atuais      |
| `Ctrl+Shift+S` | Salvar como...        |
| `Ctrl+L`    | Ler tag                  |
| `Ctrl+E`    | Escrever na tag          |
| `Ctrl+B`    | Apagar tag               |
| `Ctrl+K`    | Bloquear tag             |
| `Ctrl+,`    | Abrir configurações      |
| `F1`        | Mostrar ajuda            |
| `F5`        | Atualizar tag            |
| `Ctrl+Q`    | Sair do aplicativo       |

## 🤝 Contribuições

Contribuições são bem-vindas! Aqui estão algumas formas de ajudar:

1. Reporte bugs abrindo uma issue
2. Sugira novos recursos ou melhorias
3. Envie pull requests
4. Melhore a documentação
5. Compartilhe seus comentários e ideias

## 📝 Licença

Este projeto está licenciado sob a Licença GPL-3.0

## 👤 Autor

- **Nsfr750**
  - Email: [nsfr750@yandex.com](mailto:nsfr750@yandex.com)
  - GitHub: [@Nsfr750](https://github.com/Nsfr750)
  - Discord: [Junte-se à nossa comunidade](https://discord.gg/ryqNeuRYjD)

## 💖 Apoie

Se você achar este projeto útil, considere apoiar seu desenvolvimento:

- [Torne-se um Patrocinador](https://www.patreon.com/Nsfr750)
- [Doe via PayPal](https://paypal.me/3dmega)
- Doe Monero:

  ```text
  47Jc6MC47WJVFhiQFYwHyBNQP5BEsjUPG6tc8R37FwcTY8K5Y3LvFzveSXoGiaDQSxDrnCUBJ5WBj6Fgmsfix8VPD4w3gXF
  ```

## 📞 Contato

Para suporte, solicitações de recursos ou dúvidas, abra uma issue no [GitHub](https://github.com/Nsfr750/NFC/issues) ou junte-se ao nosso [servidor no Discord](https://discord.gg/ryqNeuRYjD).
