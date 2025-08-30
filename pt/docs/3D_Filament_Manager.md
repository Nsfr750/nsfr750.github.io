---
lang: pt
lang-niv: fonto
lang-ref: 010-jbk
layout: page
title: 'Gerenciador de Filamento 3D'
---

# Gerenciador de Filamento 3D

![Gerenciador de Filamento 3D](assets/logo.png)

Um aplicativo de desktop para gerenciar seu inventário de filamentos de impressão 3D. Acompanhe materiais, cores, uso, custos e configurações de fatiamento em um único lugar.

## ✨ Recursos

* **🌐 Suporte Multilíngue**: Disponível em inglês, espanhol e italiano
* **🎨 Interface Moderna**: Design limpo com ícones de emoji e suporte a temas (modo claro/escuro)
* **📊 Gerenciamento Abrangente de Filamentos**:
  * Armazene informações detalhadas do filamento (marca, material, cor, diâmetro, etc.)
  * Acompanhe o uso e a quantidade restante do filamento
  * Calcule custos de material
  * Acompanhamento de preços e histórico
  * Análise interativa de preços com visualizações
  * Comparação de preços entre fornecedores
* **⚙️ Integração com Fatiadores**:
  * Salve e gerencie perfis de fatiamento (Cura, PrusaSlicer, eQuidiSlicer)
  * Perfis de impressão personalizados para diferentes impressoras
* **🔍 Busca e Filtragem Avançada**:
  * Pesquise por qualquer propriedade do filamento
  * Ordene por qualquer coluna
  * Filtre por tipo de material, cor ou tags personalizadas
* **📂 Importar/Exportar**:
  * Faça backup e restaure sua biblioteca de filamentos
  * Compartilhe perfis com outros usuários
  * Suporte a importação/exportação em lote
* **🔒 Segurança de Dados**:
  * Configurações salvas no diretório `config/`
  * Nenhuma conexão com a internet necessária
  * Armazenamento local de dados

## 🚀 Requisitos

* Python 3.8 ou superior
* Pacotes necessários (instalados automaticamente):
  * `lxml` - Processamento rápido de XML
  * `pillow` - Processamento de imagens para ícones
  * `matplotlib` - Visualização de dados para análise de preços

## 🛠️ Instalação

### Pré-requisitos

* Python 3.8 ou superior
* Git (opcional, para desenvolvimento)

### Passos de Instalação

1. **Clone o repositório** (ou baixe como ZIP):

   ```bash
   git clone https://github.com/Nsfr750/3D_Filament_Manager.git
   cd 3D_Filament_Manager
   ```

2. **Crie e ative um ambiente virtual** (recomendado):

   ```bash
   # No Windows
   python -m venv venv
   .\venv\Scripts\activate
   
   # No macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Instale as dependências**:

   ```bash
   pip install -r requirements.txt
   ```

4. **Execute o aplicativo**:

   ```bash
   python main.py
   ```

### Armazenamento de Dados

* Os perfis de filamento são armazenados no diretório `fdm/`
* As configurações do aplicativo são salvas no diretório `config/`
* Os logs são gravados no diretório `logs/`

## 🤝 Contribuições

Aceitamos contribuições! Aqui estão algumas maneiras de ajudar:

* Relate bugs abrindo uma [issue](https://github.com/Nsfr750/3D_Filament_Manager/issues)
* Sugira novos recursos ou melhorias
* Envie pull requests com alterações de código
* Ajude a melhorar a documentação
* Traduza o aplicativo para novos idiomas

### Configuração de Desenvolvimento

1. Faça um fork do repositório
2. Crie um branch de recurso (`git checkout -b feature/recurso-incrivel`)
3. Faça commit das suas alterações (`git commit -m 'Adicionei um recurso incrível'`)
4. Envie para o branch (`git push origin feature/recurso-incrivel`)
5. Abra um Pull Request

### Estilo de Código

* Siga as diretrizes do [PEP 8](https://www.python.org/dev/peps/pep-0008/)
* Use dicas de tipo para maior clareza do código
* Escreva docstrings para todas as funções e classes públicas

## 📜 Licença

Este projeto está licenciado sob a **Licença Pública Geral GNU v3.0**. Consulte o arquivo [LICENÇA](LICENÇA) para obter detalhes.

## 🙏 Apoio

Se você achar este projeto útil, considere apoiar seu desenvolvimento:

* ⭐ Dê uma estrela ao repositório
* 🐛 Relate problemas
* 💡 Sugira novos recursos
* 💰 [Apoie o projeto no GitHub](https://github.com/sponsors/Nsfr750)

## 📞 Contato

* GitHub: [@Nsfr750](https://github.com/Nsfr750)
* E-mail: nsfr750@yandex.com

---

### Apoie o Desenvolvedor

Se este aplicativo for útil para você, considere apoiar o desenvolvedor:

* **PayPal**: [https://paypal.me/3dmega](https://paypal.me/3dmega)
* **GitHub**: [https://github.com/Nsfr750](https://github.com/Nsfr750)
