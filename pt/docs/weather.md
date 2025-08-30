---
lang: pt
lang-niv: fonto
lang-ref: 022-jbk
layout: page
title: 'Tempo'
---

# Documentação do Aplicativo de Previsão do Tempo (v1.6.0)

Bem-vindo à documentação do Aplicativo de Previsão do Tempo! Este aplicativo fornece informações meteorológicas em tempo real e previsões de vários provedores de dados meteorológicos.

## Recursos

- 🌦️ Condições climáticas atuais com métricas detalhadas
- 📅 Previsão do tempo para 7 dias com detalhamento por hora
- 📖 Visualizador de documentação Markdown integrado
- 📊 Visualizador de logs do aplicativo para diagnóstico
- 🌍 Múltiplos provedores de dados meteorológicos
- 🌐 Suporte a vários idiomas
- ⭐ Localizações favoritas com histórico aprimorado
- ⚙️ Configurações e temas personalizáveis

## Atualizações Recentes

Para uma lista detalhada de alterações, consulte o arquivo [CHANGELOG.md](CHANGELOG.md).

## Primeiros Passos

1. [Guia de Instalação](installation.md) - Como instalar e configurar o aplicativo
2. [Guia do Usuário](usage.md) - Como usar o aplicativo
3. [Configuração](configuration.md) - Como configurar o aplicativo

## Tópicos Avançados

- [Provedores Meteorológicos](providers.md) - Informações sobre os provedores de dados meteorológicos suportados
- [Traduções](translations.md) - Como adicionar ou modificar traduções
- [Guia de Desenvolvimento](development.md) - Como contribuir para o projeto
- [Solução de Problemas](troubleshooting.md) - Problemas comuns e soluções

## Suporte

Para suporte, por favor abra uma issue em nosso [repositório no GitHub](https://github.com/Nsfr750/weather).

## Licença

Este projeto está licenciado sob a Licença GPLv3 - consulte o arquivo [LICENÇA](https://github.com/Nsfr750/weather/blob/main/LICENSE) para obter detalhes.

# Guia do Usuário

## Primeiros Passos

1. **Iniciando o Aplicativo**
   - Dê um duplo clique no ícone do aplicativo ou execute pelo terminal
   - A janela principal será aberta mostrando o tempo da localização padrão
   - Na primeira execução, você será guiado pela configuração inicial

2. **Procurando por uma Localização**
   - Digite o nome de uma cidade na caixa de pesquisa
   - Pressione Enter ou clique no botão de pesquisa (🔍)
   - Para resultados mais precisos, inclua o código do país (ex: "São Paulo, BR")
   - Clique com o botão direito no mapa para selecionar uma localização

## Interface Principal

### Exibição do Tempo

- **Tempo Atual**: Mostra temperatura, condições e detalhes adicionais
  - Clique em qualquer métrica para alternar entre unidades (ex: °C/°F, km/h/mph)
  - Passe o mouse sobre os ícones para obter mais informações

- **Previsão para 7 Dias**: Mostra a previsão do tempo para os próximos 7 dias
  - Clique em um dia para ver a previsão horária
  - Probabilidade de precipitação codificada por cores
  - Inclui variações de temperatura e condições climáticas para cada dia

- **Detalhes do Tempo**: Inclui:
  - Sensação térmica
  - Umidade e ponto de orvalho
  - Velocidade e direção do vento
  - Pressão e visibilidade
  - Índice UV e qualidade do ar
  - Horários do nascer e pôr do sol

### Navegação

- **Barra de Pesquisa**: Encontre o tempo para qualquer localização
  - As pesquisas recentes são salvas automaticamente
  - Pesquise por nome da cidade, CEP ou coordenadas

- **Seletor de Tema**: Alterne entre tema claro, escuro ou do sistema

- **Barra de Menu**: Acesse recursos e configurações adicionais
  - Arquivo: Nova janela, configurações, sair
  - Visualizar: Alternar elementos da interface, atualizar dados, mapas e radar
  - Favoritos: Gerenciar localizações salvas
  - Ajuda: Visualizador de documentação, visualizador de logs, sobre, verificar atualizações

## Mapas e Radar Meteorológico

O recurso de Mapas e Radar Meteorológico fornece visualizações interativas de padrões e condições climáticas.

### Acessando os Mapas Meteorológicos

1. Clique em **Visualizar** na barra de menu
2. Selecione **Mapas e Radar Meteorológico**
3. O diálogo de Mapas Meteorológicos será aberto com várias abas

### Recursos

#### Aba Radar
- **Tipo de Mapa**: Alterne entre diferentes mapas base (OpenStreetMap, OpenTopoMap, Stamen Terrain)
- **Camada**: Ative/desative sobreposições de radar e satélite
- **Pesquisar**: Encontre localizações por nome ou coordenadas

#### Aba Temperatura
- Visualize as variações de temperatura entre as regiões
- Alterne entre Celsius e Fahrenheit
- Ajuste a opacidade da sobreposição de temperatura

#### Aba Precipitação
- Veja a precipitação atual e prevista
- Ative/desative diferentes camadas de precipitação
- Visualize chuva, neve e outros tipos de precipitação

#### Aba Vento
- Visualize a velocidade e direção do vento
- Ative/desative setas ou linhas de fluxo
- Ajuste as unidades de velocidade do vento (km/h, m/s, mph, nós)

### Usando o Mapa
- **Zoom**: Use a roda do mouse ou os botões +/-
- **Mover**: Clique e arraste o mapa
- **Pesquisar**: Digite um local na caixa de pesquisa e pressione Enter
- **Camadas**: Ative/desative diferentes camadas meteorológicas usando os controles
- **Tela Cheia**: Clique no botão de tela cheia para uma visualização maior

### Dicas
- O mapa centralizará automaticamente em sua localização atual se os serviços de localização estiverem ativados
- Clique no mapa para obter informações meteorológicas detalhadas daquele local
- Use os controles de linha do tempo para visualizar dados de previsão para horários diferentes
- Clique com o botão direito no mapa para definir um marcador ou obter coordenadas

## Recursos

### Favoritos

- **Adicionar aos Favoritos**: Clique na estrela (☆) para salvar uma localização

- **Ver Favoritos**: Acesse as localizações salvas no menu Favoritos
  - Reordene os favoritos arrastando e soltando
  - Clique com o botão direito para ações rápidas

- **Sincronizar Favoritos**: Ative a sincronização em nuvem nas configurações

- **Remover dos Favoritos**: Clique na estrela preenchida (★) para remover

### Configurações

1. Clique no ícone de engrenagem (⚙️) ou vá para Menu > Configurações
2. Configure opções como:
   - **Geral**: Idioma, tema, unidades
   - **Tempo**: Configurações do provedor, frequência de atualização
   - **Exibição**: Layout, animações, tamanho da fonte
   - **Notificações**: Alertas meteorológicos, alertas de chuva
   - **Avançado**: Cache, registro, opções de desenvolvedor
3. Clique em "Salvar" para aplicar as alterações

### Interface de Linha de Comando

```bash
# Uso básico
weather-app [localização] [opções]

# Exemplos
weather-app "Rio de Janeiro, BR"
weather-app --provider openweathermap --units metric
weather-app --config ~/.config/weather/config.ini

# Opções
  -h, --help            Mostrar mensagem de ajuda e sair
  -v, --version         Mostrar informações de versão
  -c, --config ARQUIVO  Especificar arquivo de configuração
  -d, --debug           Ativar modo de depuração
  --provider PROVEDOR   Definir provedor meteorológico
  --units {metric,imperial}
                        Definir sistema de unidades
  --lang IDIOMA         Definir código de idioma
  --tema {claro,escuro,sistema}
                        Definir esquema de cores
  --sem-interface       Executar em modo console
```

## Atalhos de Teclado

### Atalhos Globais

| Atalho | Ação |
|--------|------|
| `Ctrl + F` | Focar na barra de pesquisa |
| `Ctrl + ,` | Abrir Configurações |
| `Ctrl + Q` | Sair do Aplicativo |
| `F1` | Mostrar Ajuda |
| `Esc` | Fechar diálogos ou limpar pesquisa |
| `F5` | Atualizar dados meteorológicos |
| `Ctrl + R` | Atualizar todos os dados |
| `Ctrl + W` | Fechar janela atual |
| `Ctrl + N` | Nova janela |

### Atalhos de Navegação

| Atalho | Ação |
|--------|------|
| `Ctrl + Tab` | Alternar entre localizações |
| `Ctrl + F` | Alternar favoritos |
| `Ctrl + L` | Alternar lista de localizações |
| `Ctrl + M` | Alternar visualização do mapa |

## Dicas e Truques

- **Clique com o botão direito** em qualquer card do tempo para ações rápidas
- **Duplo clique** na temperatura para alternar entre Celsius e Fahrenheit
- **Clique do meio** no mapa para definir uma localização personalizada
- Use a **roda do mouse** na previsão para rolar pelas horas
- **Arraste e solte** para reordenar os locais favoritos
- **Fixar** a janela para mantê-la sobre outras aplicações
- Use o **ícone na bandeja do sistema** para acesso rápido

### Visualizador de Documentação

- Acesse a documentação Markdown integrada no menu Ajuda
- Navegue por documentação abrangente
- Funcionalidade de busca para encontrar tópicos específicos
- Zoom para melhor legibilidade
- Sumário para navegação fácil

### Visualizador de Logs

- Visualize os logs do aplicativo no menu Ajuda
- Filtre logs por nível (Depuração, Informação, Aviso, Erro)
- Pesquise em mensagens de log
- Copie logs para a área de transferência para solução de problemas

### Mapas Meteorológicos
- Acesse mapas meteorológicos no menu Visualizar
- Mapa interativo com várias camadas:
  - Temperatura
  - Precipitação
  - Velocidade do vento
  - Cobertura de nuvens
- Navegue e aplique zoom para explorar diferentes regiões
- Clique no mapa para obter informações meteorológicas daquele local

## Solução de Problemas

Se encontrar algum problema:
1. Verifique sua conexão com a internet
2. Verifique suas chaves de API nas Configurações
3. Tente mudar para um provedor meteorológico diferente
4. Verifique os logs do aplicativo em busca de erros
5. Reinicie o aplicativo
6. Redefina as configurações, se necessário

Para obter ajuda adicional, visite nosso [repositório no GitHub](https://github.com/Nsfr750/weather) ou consulte o [Guia de Solução de Problemas](troubleshooting.md).

## Feedback

Agradecemos seu feedback! Por favor, nos informe:
- Quais recursos você gostaria de ver
- Quaisquer problemas que encontrar
- Sua experiência com o aplicativo

Você pode enviar feedback pelo aplicativo (Ajuda > Enviar Feedback) ou em nossa página de [Issues do GitHub](https://github.com/Nsfr750/weather/issues).
