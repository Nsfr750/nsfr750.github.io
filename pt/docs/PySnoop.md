---
lang: pt
lang-niv: fonto
lang-ref: 020-jbk
layout: page
title: 'PySnoop'
---

# PySnoop

[![Licença: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Python 3.7+](https://img.shields.io/badge/python-3.7+-blue.svg)](https://www.python.org/downloads/)
[![Estilo de código: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

Um aplicativo moderno baseado em Python para leitura, gravação e análise de dados de tarjas magnéticas de cartões. Este projeto é uma continuação do projeto original StripeSnoop, reconstruído com Python moderno e uma interface amigável.

## ✨ Recursos

- **Leitura de cartões**: Lê cartões de tarja magnética usando leitores compatíveis
- **Gerenciamento de banco de dados**: Armazena e gerencia dados de cartões com segurança
- **Múltiplos formatos**: Exporta/Importa dados de cartões em vários formatos
- **Interface gráfica moderna**: Interface de usuário intuitiva com suporte a temas
- **Multiplataforma**: Funciona no Windows, macOS e Linux
- **Executável independente**: Pode ser compilado como um único arquivo executável para fácil distribuição
- **Versões de depuração**: Configuração especial de depuração para solução de problemas
- **Segurança**: Armazenamento seguro para dados sensíveis de cartões
- **Validação**: Validação integrada de números de cartão (C10/Luhn)
- **Documentação**: Documentação abrangente e exemplos

## 🚀 Instalação

### Pré-requisitos

- Python 3.7 ou superior
- pip (gerenciador de pacotes Python)
- Git (opcional, para desenvolvimento)

### Início Rápido

1. Clone o repositório:

   ```bash
   git clone https://github.com/Nsfr750/PySnoop.git
   cd PySnoop
   ```

2. Crie e ative um ambiente virtual:

   ```bash
   # Windows
   python -m venv venv
   .\venv\Scripts\activate
   
   # macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Instale as dependências:

   ```bash
   pip install -r requirements.txt
   ```

## 🏗️ Construindo o Aplicativo

O PySnoop pode ser compilado em um executável independente usando Nuitka. Fornecemos dois scripts de compilação:

### Versão de Depuração

```bash
.\snoop_debug.bat
```

Isso cria uma versão de depuração do aplicativo com a janela do console habilitada para solução de problemas.

### Versão de Lançamento

```bash
.\snoop.bat
```

Isso cria uma versão otimizada de lançamento do aplicativo.

### Saídas da Compilação

- Versão de depuração: `build\PySnoop_debug.exe`
- Versão de lançamento: `build\PySnoop.exe`

## 🛠️ Desenvolvimento
   ```bash
   pip install -r requirements.txt
   ```

## 💻 Como Usar

### Modo Gráfico (Recomendado)

```bash
python pysnoop_gui.py
```

### Interface de Linha de Comando

```bash
python pysnoop.py [opções]
```

### Opções Disponíveis

```bash
-h, --help      Mostra a mensagem de ajuda e sai
-v, --verbose   Habilita saída detalhada
--version       Mostra informações da versão
```

## 🔌 Dispositivos Suportados

- Leitor/Gravador de Cartão de Tarja Magnética MSR605
- Outros leitores de cartão compatíveis com HID (experimental)

## 📚 Documentação

Para documentação detalhada, incluindo referência de API e exemplos de uso, visite a [documentação](https://nsfr750.github.io/PySnoop/ "Documentação do PySnoop").

## 🤝 Contribuindo

Contribuições são bem-vindas! Por favor, leia nossas [diretrizes de contribuição](CONTRIBUTING.md) para começar.

## 📄 Licença

Este projeto está licenciado sob a Licença GPLv3 - veja o arquivo [LICENÇA](LICENÇA) para detalhes.

## 🙏 Apoio

Se você achar este projeto útil, considere apoiar seu desenvolvimento:

[![Doar via PayPal](https://img.shields.io/badge/Doar-PayPal-blue.svg)](https://paypal.me/3dmega)
[![Torne-se um Patrocinador](https://img.shields.io/badge/Apoie-Patreon-laranja.svg)](https://www.patreon.com/Nsfr750)

## 📧 Contato

Para dúvidas ou suporte, por favor, abra uma issue ou entre em contato com [Nsfr750](mailto:nsfr750@yandex.com).

## Créditos

- Baseado no projeto original StripeSnoop (http://stripesnoop.sourceforge.net)

## Como Contribuir

Contribuições são bem-vindas! Sinta-se à vontade para enviar um Pull Request.
