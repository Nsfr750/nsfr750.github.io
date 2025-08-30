---
lang: pt
lang-niv: fonto
lang-ref: 019-jbk
layout: doc
order: 10
title: 'Localizador de PDF'
---

# Localizador de PDFs Duplicados

[![Licença: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Estilo de código: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

Uma ferramenta poderosa para encontrar e gerenciar arquivos PDF duplicados no seu computador. O Localizador de PDFs Duplicados ajuda você a identificar e remover documentos PDF duplicados, economizando espaço em disco e organizando seus arquivos com mais eficiência.

## ✨ Recursos

- 🔍 **Comparação Inteligente de PDFs**: Encontra PDFs duplicados com base no conteúdo, não apenas em nomes ou tamanhos de arquivo
- 📝 **Comparação Baseada em Texto**: Identifica duplicatas mesmo com pequenas diferenças visuais usando análise de texto avançada
- 👁 **Visualizador de PDF Integrado**: Visualize PDFs diretamente no aplicativo
- 📋 **Interface de Dupla Visualização**: Visualize a lista de arquivos e grupos de duplicatas em abas separadas
- 🎯 **Filtragem Avançada**: Filtre por tamanho de arquivo, data de modificação e padrões de nome
- 🚀 **Digitalização Rápida**: Algoritmos otimizados para digitalização rápida de grandes coleções de PDFs
- 🎨 **Interface Intuitiva**: Interface limpa e fácil de usar com suporte a temas claro/escuro
- 🔄 **Processamento em Lote**: Processe vários arquivos ou pastas inteiras de uma vez
- 📊 **Análise Detalhada**: Visualize detalhes dos arquivos, visualizações e resultados de comparação
- 🛠 **Ferramentas Avançadas**: Múltiplos modos de seleção, filtragem e opções de classificação
- 🌍 **Suporte a Múltiplos Idiomas**: Disponível em vários idiomas
- 📊 **Acompanhamento de Progresso**: Barra de progresso em tempo real para operações de processamento de arquivos
- ⏱ **Arquivos Recentes**: Acesso rápido a arquivos abertos recentemente com opções de menu de contexto

## 📦 Instalação

### Pré-requisitos

- Python 3.8 ou superior
- pip (gerenciador de pacotes Python)
- Backends opcionais para renderização de PDF (fallback automático seguro):
  - PyMuPDF (fitz) — padrão e incluído via requirements
  - Ghostscript (para Wand) — instale o Ghostscript e defina o caminho do executável nas Configurações

Consulte [PREREQUISITES.md](PREREQUISITES.md) para configuração específica da plataforma.

### Instalação a partir do Código Fonte

1. Clone o repositório:

   ```bash
   git clone https://github.com/Nsfr750/PDF_finder.git
   cd PDF_finder
   ```

2. Crie e ative um ambiente virtual (recomendado):

   ```bash
   python -m venv venv
   .\venv\Scripts\activate  # Windows
   source venv/bin/activate  # Linux/Mac
   ```

3. Instale as dependências necessárias:

   ```bash
   pip install -r requirements.txt
   ```

## Como Usar

1. Inicie o aplicativo:

   ```bash
   python main.py
   ```

2. Clique em "Escanear Pasta" para selecionar um diretório e procurar por PDFs duplicados.

3. Revise os resultados na janela principal. Após a conclusão de uma varredura, a lista de arquivos é preenchida automaticamente com os PDFs digitalizados e os grupos de duplicatas.

4. Use as ferramentas para gerenciar duplicatas:
   - Marque os arquivos para manter
   - Exclua as duplicatas indesejadas
   - Visualize os arquivos antes de tomar qualquer ação

## Principais Recursos em Detalhe

### Comparação Inteligente de PDFs

- Compara o conteúdo de PDFs usando algoritmos avançados de hash
- Detecta documentos semelhantes mesmo com nomes de arquivo ou metadados diferentes
- Limiar de similaridade configurável para resultados refinados

### Otimizações de Desempenho

- Digitalização com múltiplas threads para processamento mais rápido
- Manipulação eficiente de memória para arquivos PDF grandes
- Acompanhamento de progresso e suporte a cancelamento

### Experiência do Usuário

- Interface moderna e responsiva
- Opções de visualização personalizáveis
- Atalhos de teclado abrangentes
- Informações detalhadas de arquivos e visualizações
- Barra de ferramentas com espaçamento aprimorado e clareza visual
- A caixa de diálogo Configurações inclui um botão "Testar backends" para validar a disponibilidade do PyMuPDF e Ghostscript

### Backends de PDF e Fallback

- Escolha seu backend preferido em Configurações → Renderização de PDF
- Use "Testar backends" para verificar se o Ghostscript está configurado corretamente
- Se o backend selecionado falhar, o aplicativo retornará para um backend disponível e exibirá um aviso na barra de status (localizado)

## Histórico de Versões

Consulte [CHANGELOG.md](CHANGELOG.md) para obter uma lista completa de alterações em cada versão.

## Contribuições

Contribuições são bem-vindas! Por favor, leia nossas [Diretrizes de Contribuição](CONTRIBUTING.md) para obter detalhes sobre como contribuir para este projeto.

## 📄 Licença

Este projeto está licenciado sob a Licença Pública Geral GNU v3.0 - consulte o arquivo [LICENÇA](LICENÇA) para obter detalhes.

## 🙏 Agradecimentos

- Agradecemos a todos os colaboradores que ajudaram a melhorar o Localizador de PDFs Duplicados
- Construído com ❤️ usando Python e PyQt6

## 🐞 Problemas Conhecidos

- A seleção de idioma não está funcionando

---

📅 **Última Atualização**: Agosto de 2025  
🐍 **Versão do Python**: 3.8+  
📜 **Licença**: GPL-3.0
