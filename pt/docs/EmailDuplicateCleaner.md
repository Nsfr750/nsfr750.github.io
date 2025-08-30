---
lang: pt
lang-niv: fonto
lang-ref: 013-jbk
layout: page
title: 'Email Duplicate Cleaner'
---

# 📧 Limpador de Emails Duplicados

Uma ferramenta abrangente em Python projetada para escanear, identificar e remover e-mails duplicados em vários clientes de e-mail. Inclui interfaces web, desktop e linha de comando.

## 🚀 Versão

**Versão Atual:**
[![Versão no GitHub](https://img.shields.io/badge/vers%C3%A3o-v2.5.2-green)](https://github.com/Nsfr750/EmailDuplicateCleaner)
[![Documentação](https://img.shields.io/badge/documenta%C3%A7%C3%A3o-dispon%C3%ADvel-brightgreen)](https://github.com/Nsfr750/EmailDuplicateCleaner/blob/master/README.md)
[![Versões do Python](https://img.shields.io/badge/python-3.8%20|%203.9%20|%203.10%20|%203.11%20|%203.12-blue)](https://www.python.org/)
[![Licença: GPL v3](https://img.shields.io/badge/Licen%C3%A7a-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![PyPI](https://img.shields.io/pypi/v/email-duplicate-cleaner)](https://pypi.org/project/email-duplicate-cleaner/)
[![Doar](https://img.shields.io/badge/Doar-PayPal-green.svg)](https://paypal.me/3dmega)
[![Apoiar](https://img.shields.io/badge/Apoiar-Patreon-ff69b4.svg)](https://www.patreon.com/Nsfr750)

## ✨ Novidades na Versão 2.5.2

- 🚀 Atualização para a versão 2.5.2
- 🐛 Corrigida a exibição do número da versão na caixa de diálogo Sobre
- 📚 Documentação atualizada com as últimas alterações

## ✨ Novidades na Versão 2.5.1

- 🐛 Corrigido erro de importação do QAction na interface gráfica do PySide6
- 🌐 Adicionadas traduções completas para o inglês
- 📄 Incluído arquivo de licença GPL-3.0
- 🔄 Melhor tratamento de erros na inicialização da interface gráfica
- ⬆️ Atualizadas dependências para maior estabilidade

## ✨ Recursos

### 🔍 Detecção de Duplicatas

- Múltiplos critérios de detecção:
  - Rigoroso: Comparação abrangente
  - Apenas Conteúdo: Análise do corpo da mensagem
  - Cabeçalhos: Correspondência baseada em metadados
  - Assunto+Remetente: Identificação focada

### 📊 Análise de E-mails

- Análise avançada de e-mails:
  - Análise de remetentes: Identifica principais remetentes e domínios
  - Análise temporal: Visualiza padrões de e-mail ao longo do tempo
  - Análise de anexos: Tipos, tamanhos e frequências de arquivos
  - Análise de tópicos: Visualiza e gerencia conversas
  - Análise de duplicatas: Detalhes sobre a detecção de duplicatas
  - Relatórios exportáveis em vários formatos (Texto, HTML, JSON)

### 🖥️ Suporte a Múltiplas Interfaces

- **Interface Web** - Design moderno e responsivo com modo claro/escuro
- **Interface de Desktop** - Experiência nativa de desktop com PySide6
- **Interface de Linha de Comando** - Poderoso suporte para automação e scripts

### 🌓 Experiência do Usuário Aprimorada

- Interface web moderna com modo claro/escuro
- Visualização interativa com atualizações em tempo real
- Sistema de ajuda abrangente
- Modo de depuração com registro detalhado
- Modo de demonstração para testes e aprendizado

### 🔒 Compatibilidade com Clientes de E-mail

Suporta:

- Mozilla Thunderbird
- Apple Mail
- Microsoft Outlook
- Formatos genéricos mbox/maildir

### 🏗️ Destaques Técnicos

- Interface web moderna construída com Flask
- SQLAlchemy para gerenciamento de banco de dados
- Sistema de ajuda abrangente com conteúdo dinâmico
- Arquitetura modular com separação clara de responsabilidades
- Compatibilidade multiplataforma
- Tratamento abrangente de erros e registro

## 🛠️ Pré-requisitos

- Python 3.8 ou superior
- pip
- Sistemas operacionais suportados: Windows, macOS, Linux

## 🚀 Início Rápido

### 💰 Apoie Este Projeto

Se você achar esta ferramenta útil, considere apoiar seu desenvolvimento:

- [![Doar](https://img.shields.io/badge/Doar-PayPal-green.svg)](https://paypal.me/3dmega) Apoie via PayPal
- [![Apoiar](https://img.shields.io/badge/Apoiar-Patreon-ff69b4.svg)](https://www.patreon.com/Nsfr750) Torne-se um Patrocinador
- :money_with_wings: **Monero (XMR)**: 
  ```
  47Jc6MC47WJVFhiQFYwHyBNQP5BEsjUPG6tc8R37FwcTY8K5Y3LvFzveSXoGiaDQSxDrnCUBJ5WBj6Fgmsfix8VPD4w3gXF
  ```

## 📦 Instalação

1.  Clone o repositório:

    ```bash
    git clone https://github.com/Nsfr750/EmailDuplicateCleaner.git
    cd EmailDuplicateCleaner
    ```

2.  Instale as dependências:

    ```bash
    pip install -r requirements.txt
    ```

### Executando o Aplicativo

#### Interface Web

```bash
python app.py
```

Acesse em `http://localhost:5000`

#### Interface Gráfica de Desktop

```bash
python email_cleaner_gui.py
```

#### Demonstração na Linha de Comando

```bash
python email_duplicate_cleaner.py --demo
```

## 🤝 Contribuindo

Interessado em contribuir? Confira nosso [Guia de Contribuição](CONTRIBUTING.md)!

## 📄 Licença

Este projeto está licenciado sob a Licença MIT.

## 🐛 Problemas

Encontrou um bug? [Abra uma issue](https://github.com/Nsfr750/EmailDuplicateCleaner/issues)

## 📊 Métodos de Detecção

- `strict`: ID da Mensagem + Data + De + Assunto + Conteúdo
- `content`: Apenas conteúdo
- `headers`: ID da Mensagem + Data + De + Assunto
- `subject-sender`: Apenas campos de Assunto e Remetente

## Recursos de Segurança

- Sempre preserva pelo menos uma cópia de cada e-mail
- Mantém o e-mail mais antigo por padrão
- E-mails originais recuperáveis da lixeira
- Modo de demonstração para testes seguros

## Estrutura do Projeto

- `email_cleaner_web.py`: Interface web
- `email_cleaner_gui.py`: Interface gráfica de desktop
- `email_duplicate_cleaner.py`: Funcionalidade principal e CLI
- `static/`: Recursos web (CSS, JS)
- `templates/`: Modelos HTML

## Fluxos de Trabalho

- Modo Demonstração: Executa com e-mails de teste
- Ajuda: Mostra informações de uso
- Modo Interface Gráfica: Inicia a interface de desktop
- Modo Web: Inicia o servidor web

## Estrutura da Interface Gráfica

- **Interface Gráfica (`email_cleaner_gui.py`)**: Uma interface gráfica amigável construída com Tkinter. Fornece uma maneira intuitiva de selecionar clientes de e-mail, escanear pastas e gerenciar duplicatas.
- **Linha de Comando (`email_cleaner_cli.py`)**: Uma interface de linha de comando para usuários que preferem trabalhar no terminal.
- **Web (`app.py`)**: Uma interface baseada na web construída com Flask, acessível a partir de qualquer navegador.

### Módulos Auxiliares (`struttura/`)

O diretório `struttura/` contém todos os módulos auxiliares que suportam a interface gráfica, como janelas de diálogo e menus.

- **`menu.py`**: Gerencia a criação e funcionalidade da barra de menu principal, mantendo o arquivo principal da interface gráfica limpo e focado em seu layout central.
- **`about.py`**, **`help.py`**, **`sponsor.py`**: Definir as janelas de diálogo `Sobre`, `Ajuda` e `Patrocinador`, cada uma encapsulada em sua própria classe.
- **`log_viewer.py`**: Um visualizador de logs simples para exibir os logs do aplicativo.

## Recursos da Interface Gráfica

- **Interface Intuitiva**: Uma interface gráfica limpa e fácil de usar para gerenciar contas de e-mail e verificar duplicatas.
- **Seleção Múltipla**: Use `Shift+Setas` e `Ctrl+Setas` para selecionar várias caixas de correio e pastas.
- **Suporte a Múltiplos Idiomas**: Disponível em inglês e italiano.
