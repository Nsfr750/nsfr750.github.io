---
lang: pt
lang-niv: fonto
lang-ref: 023-jbk
layout: doc
order: 14 # Opcional: para ordenação no menu
title: 'benchmark'
---

[![Licença: GPL v3](https://img.shields.io/badge/Licença-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![Estilo de código: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

Uma ferramenta moderna de benchmark em Python desenvolvida com PySide6, fornecendo uma interface amigável para executar e analisar testes Pystone e outros benchmarks.

## 📥 Instalação

### Pré-requisitos

- Python 3.9 ou superior
- Windows ou Linux

### Início Rápido

1. Clone o repositório:

   ```bash
   git clone https://github.com/Nsfr750/benchmark.git
   cd benchmark
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

## ✨ Recursos

- **Interface de usuário moderna**: Interface limpa e responsiva construída com PySide6
- **Benchmark abrangente**:
  - Duração personalizável dos testes
  - Acompanhamento em tempo real do progresso
  - Resultados detalhados com estatísticas
  - Comparação com dados históricos
- **Registro**:
  - Registros detalhados de operações
  - Filtragem de registros por nível
  - Rotação de arquivos de log
- **Suporte multilíngue**:
  - Inglês (en)
  - Italiano (it)
- **Acessibilidade**:
  - Atalhos de teclado
  - Modo de alto contraste
  - Tamanho do texto ajustável

## ⌨️ Atalhos de Teclado

- `Ctrl+L`: Visualizar registros do aplicativo
- `F1`: Mostrar ajuda
- `Esc`: Fechar diálogos
- `Ctrl+Q`: Sair do aplicativo

## 📊 Como Usar

1. Defina o número de iterações para o benchmark
2. Clique em "Iniciar Benchmark" para começar
3. Monitore o progresso em tempo real
4. Visualize resultados detalhados e estatísticas
5. Acesse os registros para solução de problemas

## 📂 Estrutura do Projeto

```
benchmark/
├── .github/                            # GitHub Actions
│   ├── workflows/                      # Fluxos de trabalho do GitHub Actions
│   │   └── ci-cd.yml                   # Pipeline CI/CD
│   ├── issues/                         # Problemas do GitHub
│   |   └── templates/                  # Modelos de problemas
│   └── FUNDING.yml                     # Arquivo de financiamento
├── assets/                             # Arquivos de recursos
├── config/                             # Arquivos de configuração
│   ├── config.json                     # Arquivo de configuração
│   └── updates.json                    # Cache de atualizações
├── docs/                               # Documentação
│   ├── images/                         # Imagens da documentação
│   ├── pdf/                            # Documentação em PDF
│   └── USER_GUIDE.md                   # Guia do Usuário
├── lang/                               # Arquivos de idioma
│   ├── en.json                         # Arquivo em inglês
│   └── it.json                         # Arquivo em italiano
├── logs/                               # Arquivos de log
├── script/                             # Código-fonte
│   ├── __init__.py                     # Inicialização do pacote
│   ├── about.py                        # Diálogo "Sobre"
│   ├── benchmark_history.py            # Histórico de benchmarks
│   ├── benchmark_tests.py              # Testes de benchmark
│   ├── CLI_pystone.py                  # Benchmark Pystone via linha de comando
│   ├── config_manager.py               # Gerenciador de configuração
│   ├── export_results.py               # Exportação de resultados
│   ├── hardware_monitor.py             # Monitor de hardware
│   ├── help.py                         # Diálogo de ajuda
│   ├── history_dialog.py               # Diálogo de histórico
│   ├── lang_mgr.py                     # Gerenciador de idiomas
│   ├── logger.py                       # Configuração de logs
│   ├── menu.py                         # Funcionalidade da barra de menu
│   ├── settings.py                     # Diálogo de configurações
│   ├── sponsor.py                      # Diálogo de patrocinadores
│   ├── system_info.py                  # Informações do sistema
│   ├── test_menu.py                    # Menu de testes
│   ├── theme_manager.py                # Gerenciador de temas
│   ├── updates.py                      # Sistema de atualização
│   ├── version.py                      # Sistema de versão
│   ├── view_log.py                     # Visualizador de logs
│   └── visualization.py                # Visualização de benchmarks
├── tests/                              # Arquivos de teste
│   ├── test_benchmark.py               # Teste de benchmark
│   ├── test_hardware_monitor.py        # Teste de monitor de hardware
│   ├── test_monitor_manual.py          # Teste manual de monitor
│   ├── test_monitor.py                 # Teste de monitor
│   └── TEST_README.md                  # LEIAME de testes
├── .gitignore                          # Arquivo .gitignore
├── CHANGELOG.md                        # Registro de alterações
├── CONTRIBUTING.md                     # Diretrizes de contribuição
├── LICENSE                             # Arquivo de licença GPLv3
├── main.py                             # Aplicativo principal
├── README.md                           # Este arquivo
├── requirements.txt                    # Arquivo de dependências
└── TO_DO.md                            # Lista de tarefas
```
