---
lang: pt
lang-niv: font
lang-ref: 012-jbk
layout: doc
order: 3
title: 'CDE550-Sim'
---

# Simulador Nidec Commander CDE 550

[![Versão do Python](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Licença: GPL v3](https://img.shields.io/badge/Licen%C3%A7a-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Versão](https://img.shields.io/badge/vers%C3%A3o-0.0.2-green.svg)](CHANGELOG.md)

Simulador de software para o inversor Nidec Commander CDE 550 com interface gráfica, desenvolvido em Python com PyQt6.

## Novidades na Versão 0.0.2

- **Localização completa** da interface do usuário em português
- **Melhor tratamento de alarmes** com menos falsos positivos
- **Otimizações de desempenho** durante a inicialização e variações de carga
- **Documentação atualizada** com registro de alterações detalhado

## Recursos

- Simulação realista do comportamento do inversor Nidec Commander CDE 550
- Interface gráfica intuitiva com PyQt6 totalmente localizada em português
- Comunicação serial via pyserial
- Suporte para comandos de controle principais
- Simulação de falhas e alarmes com gerenciamento avançado
- Monitoramento em tempo real de parâmetros
- Registro de eventos e erros

## Pré-requisitos

- Python 3.8 ou superior
- Pip (gerenciador de pacotes Python)
- Ambiente virtual Python (recomendado)

## Instalação

1. Clone o repositório:
   ```bash
   git clone https://github.com/Nsfr750/CDE550-sim.git
   cd CDE550-sim
   ```

2. Crie e ative um ambiente virtual (opcional mas recomendado):
   ```bash
   # No Windows
   python -m venv venv
   .\venv\Scripts\activate
   
   # No macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```

## Como Usar

1. Inicie o simulador:
   ```bash
   python main.py
   ```

2. A interface gráfica mostrará:
   - Status do inversor
   - Parâmetros operacionais
   - Registro de eventos
   - Controles de simulação

3. Para conexão serial:
   - Vá para Conexão -> Conectar
   - Selecione a porta COM desejada
   - Configure a velocidade de comunicação (baud rate)
   - Clique em "Conectar"

## Comandos Seriais Suportados

| Comando | Descrição | Exemplo |
|---------|-----------|---------|
| `RUN` | Inicia o inversor | `RUN` |
| `STOP` | Para o inversor | `STOP` |
| `RST` | Reinicia alarmes | `RST` |
| `FREQ <valor>` | Define a frequência (Hz) | `FREQ 50.0` |
| `DIR <1\|-1>` | Define a direção | `DIR 1` (frente) |
| `STATUS` | Mostra status completo | `STATUS` |
| `HELP` | Mostra lista de comandos | `HELP` |

## Estrutura do Projeto

```
CDE550-sim/
├── main.py              # Ponto de entrada do aplicativo
├── inverter_sim.py      # Lógica de simulação do inversor
├── serial_handler.py    # Manipulação de comunicação serial
├── script/              # Interface do usuário e arquivos de ajuda
│   ├── help.py          # Janela de ajuda
│   ├── serial_dialog.py # Janela de conexão serial
│   └── version.py       # Gerenciamento de versão
├── requirements.txt     # Dependências do projeto
├── README.md            # Documentação principal
└── CHANGELOG.md         # Registro de alterações
```

## Contribuições

Contribuições são bem-vindas! Para propor melhorias:

1. Faça um fork do projeto
2. Crie um branch de recurso (`git checkout -b feature/RecursoIncrivel`)
3. Faça commit das suas alterações (`git commit -m 'Adicionei um Recurso Incrível'`)
4. Envie para o branch (`git push origin feature/RecursoIncrivel`)
5. Abra um Pull Request

## Licença

Distribuído sob a Licença GPL-3.0. Consulte o arquivo `LICENSE` para obter mais informações.

## Contato

- Autor: Nsfr750
- E-mail: [nsfr750@yandex.com]
- Repositório: https://github.com/Nsfr750/CDE550-sim

---

<div align="center">
  <sub>Desenvolvido com ❤️ por Nsfr750</sub>
</div>
