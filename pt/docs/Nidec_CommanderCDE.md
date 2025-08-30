---
lang: pt
lang-niv: fonto
lang-ref: 017-jbk
layout: page
title: 'Nidec CommanderCDE'
---

# Nidec CommanderCDE

Um aplicativo GUI abrangente em Python para controlar e monitorar inversores Nidec Commander CDE via Modbus RTU.

## ✨ Recursos

- **Suporte Multilíngue**: Interface completa em inglês e italiano com troca de idioma dinâmica
- **Suporte a Múltiplos Modelos**: Compatível com os modelos de inversores CDE400, CDE550, CDE750 e CDE1100S
- **Controle do Inversor**:
  - Conexão a inversores Nidec Commander CDE via RS-485/Modbus RTU
  - Controle de velocidade e direção do motor
  - Partida/Parada do inversor
  - Monitoramento em tempo real do status e diagnóstico do inversor
  - Detecção de falhas e função de reset
  - Backup e restauração de parâmetros
- **Interface do Usuário**:
  - Interface moderna com abas e controles intuitivos
  - Painel abrangente com métricas em tempo real
  - Barra de status com informações de conexão e status do inversor
  - Design responsivo com suporte a temas Claro/Escuro
  - Elementos de interface personalizáveis
- **Gerenciamento de Dados**:
  - Monitoramento e registro em tempo real de parâmetros do inversor
  - Exportação de dados para CSV/Excel
  - Visualização gráfica de tendências de parâmetros
  - Intervalos de registro de dados configuráveis
- **Diagnósticos**:
  - Monitoramento abrangente de parâmetros
  - Histórico de falhas e registro
  - Indicadores de status do sistema
  - Métricas de desempenho em tempo real

## 🆕 Novidades na v0.0.4

### Novos Recursos
- Adicionado suporte para múltiplos modelos de inversores Nidec (CDE400, CDE550, CDE750, CDE1100S)
- Traduções completas para italiano em todos os elementos da interface
- Sistema de ajuda aprimorado com documentação detalhada
- Tema azul para melhor legibilidade nas seções de ajuda

### Melhorias
- Interface do usuário atualizada para melhor experiência
- Mensagens de erro e logs aprimorados
- Desempenho otimizado para monitoramento em tempo real
- Corrigidos problemas de compatibilidade com PyQt6
- Corrigida a troca de idioma nas caixas de diálogo de ajuda

## 🚀 Requisitos

- Python 3.8 ou superior
- PyQt6 >= 6.6.1
- pyserial >= 3.5
- pymodbus >= 3.5.4
- PyQt6-QScintilla >= 2.14.1
- python-dotenv >= 1.0.0

## 🛠 Instalação e Configuração

1. Clone o repositório:

   ```bash
   git clone https://github.com/Nsfr750/nidec-commandercde.git
   cd nidec-commandercde
   ```

2. Crie e ative um ambiente virtual (recomendado):

   ```bash
   python -m venv venv
   # No Windows:
   .\venv\Scripts\activate
   # No Unix ou MacOS:
   # source venv/bin/activate
   ```

3. Instale os pacotes necessários:

   ```bash
   pip install -r requirements.txt
   ```

## 🚀 Uso Básico

1. Conecte seu inversor Nidec Commander CDE ao seu computador usando um adaptador RS-485
2. Inicie o aplicativo:

   ```bash
   python main.py
   ```

3. Selecione a porta COM apropriada e a taxa de transmissão
4. Clique em 'Conectar' para estabelecer comunicação com o inversor
5. Use a interface para controlar e monitorar o inversor

## Configurações de Conexão

- Taxa de transmissão: 9600
- Bits de dados: 8
- Paridade: Par
- Bits de parada: 1
- Endereço Modbus: 1 (padrão, pode ser alterado nos parâmetros do inversor)

## Notas Importantes

- Este software é fornecido "como está", sem garantias de qualquer tipo
- Sempre certifique-se de fazer as conexões elétricas corretamente e seguir as medidas de segurança ao trabalhar com inversores de motor
- Os endereços de registro padrão são baseados em configurações típicas de inversores Nidec, mas podem precisar de ajustes para seu modelo específico
- Consulte o manual do Nidec CDE 400 Commander para obter informações detalhadas sobre parâmetros e endereços de registro
