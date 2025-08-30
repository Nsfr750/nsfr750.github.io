---
lang: pt
lang-niv: font
lang-ref: 021-jbk
layout: page
title: 'Utilitário RasPY'
---

# Utilitário RasPY

<div align="center">
  <img src="../images/logo.png" alt="Logo do Utilitário RasPY" width="50%">
</div>

## Bem-vindo à Documentação do Utilitário RasPY

Utilitário RasPY é um aplicativo abrangente para controlar e monitorar pinos GPIO do Raspberry Pi através de uma interface gráfica intuitiva ou API REST.

## Índice

### Introdução
- [Instalação](installazione.md)
- [Guia](guida.md)

### Desenvolvimento
- [Desenvolvimento](sviluppo.md)
- [API](api.md)
- [Interface Gráfica](gui.md)
- [Exemplos](esempi.md)

### Recursos Adicionais
- [Registro de Alterações](changelog.md)
- [Perguntas Frequentes](faq.md)

### Comunidade
- [Contribuir](contribuire.md)
- [Agradecimentos](ringraziamenti.md)

## Principais Recursos

### ✅ **Interface Gráfica Moderna**
- Tema claro/escuro
- Suporte multilíngue
- Visualização em tempo real do status dos pinos
- Integração com bandeja do sistema

### 🔌 **Suporte Completo a GPIO**
- Controle de pinos digitais de entrada/saída
- Simulador integrado para desenvolvimento
- Detecção automática de hardware
- Suporte a GPIO remoto

### 🌐 **Interface Web**
- Servidor web integrado
- Design responsivo para mobile/desktop
- Atualizações em tempo real
- Documentação de API integrada

## Guia Rápido

1. [Instalação](installazione.md) - Como instalar e configurar o Utilitário RasPY
2. [Guia](guida.md) - Guia de uso do aplicativo
3. [API](api.md) - Documentação da API para desenvolvedores
4. [Desenvolvimento](sviluppo.md) - Guia de desenvolvimento e contribuição

## Guia do Usuário

### Interface Gráfica

A interface gráfica do Utilitário RasPY 4 foi projetada para ser intuitiva e fácil de usar.

#### Menu Principal

- **Arquivo**: Controles gerais do aplicativo
- **GPIO**: Gerenciamento de pinos GPIO e simulador
- **Visualizar**: Personalização da interface
- **Ajuda**: Documentação e informações

#### Controle de GPIO

1. Abra a janela de controle de GPIO no menu
2. Selecione o pino para controlar
3. Use os botões para alternar o estado dos pinos
4. Monitore o status em tempo real

#### Simulador de GPIO
O simulador permite testar códigos sem hardware físico:

1. Inicie o simulador no menu GPIO
2. Use a interface para simular entradas/saídas
3. As alterações são refletidas em tempo real

### Registro e Depuração
O aplicativo registra eventos importantes no arquivo `logs/app.log`. Use o Visualizador de Logs integrado para:

- Filtrar mensagens por nível (INFO, AVISO, ERRO)
- Buscar mensagens específicas
- Exportar logs para análise

### Atalhos de Teclado

- **Ctrl+Q**: Sair do aplicativo
- **F1**: Mostrar ajuda
- **Ctrl+L**: Abrir visualizador de logs
- **F5**: Atualizar interface

## Referência da API

### Visão Geral

A API REST do Utilitário RasPY 4 permite controlar pinos GPIO por meio de requisições HTTP.
Todas as respostas estão no formato JSON.

### Endpoints Disponíveis

#### `GET /api/gpio`

Retorna o status de todos os pinos GPIO configurados.

**Exemplo de resposta:**

```json
{
  "17": {"state": 0, "mode": "out", "description": "LED Vermelho"},
  "18": {"state": 1, "mode": "in", "description": "Botão"}
}
```

#### `GET /api/gpio/<int:pin>`

Retorna o status de um pino específico.

**Parâmetros:**
- `pin`: Número do pino GPIO

**Códigos de status:**
- 200: Operação bem-sucedida
- 404: Pino não encontrado

**Exemplo de resposta:**

```json
{
  "state": 0,
  "mode": "out",
  "description": "LED Vermelho"
}
```

#### `POST /api/gpio/<int:pin>/on`

Liga o pino especificado.

**Parâmetros:**
- `pin`: Número do pino GPIO

**Códigos de status:**
- 200: Operação bem-sucedida
- 400: Pino inválido ou não gravável

#### `POST /api/gpio/<int:pin>/off`

Desliga o pino especificado.

**Parâmetros:**
- `pin`: Número do pino GPIO

**Códigos de status:**
- 200: Operação bem-sucedida
- 400: Pino inválido ou não gravável

## Exemplos de Uso

### Controle de GPIO com Python

```python
import requests

BASE_URL = "http://localhost:5000/api/gpio"

# Obter status de todos os pinos
response = requests.get(f"{BASE_URL}")
print("Status atual:", response.json())

# Ligar o pino 17
response = requests.post(f"{BASE_URL}/17/on")
print("Resposta de ativação:", response.status_code)
```

## Recursos Úteis

- [Site oficial do Raspberry Pi](https://www.raspberrypi.org/)
- [Documentação do Python](https://www.python.org/)
