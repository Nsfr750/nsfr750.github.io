---
lang: pt
lang-niv: fonto
lang-ref: 018-jbk
layout: doc
order: 9
title: 'OpenPGP'
---

# Documentação do Aplicativo OpenPGP GUI

Bem-vindo à documentação oficial do **Aplicativo OpenPGP GUI**.

## Visão Geral
Este aplicativo fornece uma interface moderna e amigável para gerenciamento de chaves OpenPGP, criptografia, descriptografia, assinatura de mensagens, verificação e geração de certificados SSL. Todas as operações criptográficas são realizadas localmente para máxima privacidade.

# Recursos

- Interface de usuário moderna com ttkbootstrap (tema Superhero)
- Gerar, carregar e exportar pares de chaves OpenPGP
- Definir nome da chave, e-mail, senha e visualizar impressão digital
- Criptografar e descriptografar mensagens
- Assinar e verificar mensagens (assinaturas destacadas)
- Exportar chave pública em formato ASCII (.asc)
- Visualizar impressão digital para verificação de segurança
- Gerar certificados SSL com CN personalizado
- Limpar/redefinir todos os campos com um clique
- **Sistema de registro centralizado** (informação, avisos, erros, exceções não capturadas)
- **Visualizador de logs com filtragem em tempo real** (TUDO, INFORMAÇÃO, AVISO, ERRO)
- Use `log_info`, `log_warning`, `log_error` para entradas de log personalizadas
- Captura e exibição automática de rastreamento no visualizador de logs
- Barra de menu dinâmica com diálogos Sobre, Ajuda, Visualizador de Logs, Patrocinador, Versão
- Versionamento semântico e informações de versão
- Estrutura modular (`struttura`, `gui`, etc.)
- Fácil extensibilidade e personalização de temas (através do ttkbootstrap)

# Começando

## Requisitos
- Python 3.9 ou superior
- PySide6 (incluído nos requisitos)
- pgpy (incluído nos requisitos)
- cryptography (incluído nos requisitos)
- pyperclip (incluído nos requisitos)

> **Nota**: O aplicativo foi migrado de Tkinter/ttkbootstrap para PySide6 para uma interface de usuário mais moderna e sustentável.

## Instalação
1. Clone ou baixe este repositório.
2. (Opcional) Crie um ambiente virtual:
   ```
   python -m venv venv
   venv\Scripts\activate
   ```
3. Instale as dependências:
   ```
   pip install -r requirements.txt
   ```

## Executando o Aplicativo
Execute a partir da raiz do projeto:
```
python main.py
```

Se encontrar erros de importação, certifique-se de estar executando a partir da raiz e não de uma subpasta.

# Guia do Usuário

## Visão Geral da Janela Principal
- Insira seu nome, e-mail e senha para geração de chaves.
- Selecione o algoritmo (atualmente RSA; mais em breve).
- Use os botões para gerar, carregar ou exportar chaves.
- A impressão digital da chave carregada/gerada é exibida para verificação.
- Use a área de texto para inserir mensagens para criptografar, descriptografar, assinar ou verificar.
- Exporte sua chave pública para compartilhá-la com segurança.
- Gere certificados SSL a partir da interface gráfica.
- Use o botão 'Limpar' para redefinir todos os campos.

## Barra de Menu
- **Arquivo**: Exportar chave pública, Sair
- **Log**: Visualizar log (com filtros para TUDO, INFORMAÇÃO, AVISO, ERRO)
- **Ajuda**: Ajuda, Sobre, Patrocinador

## Registro e Visualizador de Logs
- Todas as informações, avisos, erros e exceções não capturadas são registradas automaticamente.
- Use `log_info(msg)`, `log_warning(msg)`, `log_error(msg)` em seus scripts para entradas de log personalizadas.
- O Visualizador de Logs (Log > Visualizar Log) permite filtrar e visualizar logs por nível.
- Se o arquivo de log estiver ausente, o último rastreamento de execução será exibido, se disponível.

## Dicas
- Todas as operações criptográficas são locais (sem nuvem).
- Para melhores resultados, use senhas fortes.
- A janela de log fornece feedback e detalhes de erros.

# Uso Avançado

## Exportando Chaves Públicas
- Use o botão 'Exportar Chave Pública' ou o item do menu para salvar sua chave pública em formato ASCII (.asc).

## Verificação de Impressão Digital
- Sempre verifique a impressão digital antes de compartilhar sua chave pública para maior segurança.

## Geração de Certificados SSL
- Insira o Nome Comum (CN) desejado no campo de nome.
- Clique no botão 'Gerar Certificado SSL' para criar um certificado autoassinado.

## Estendendo o Aplicativo
- Você pode adicionar suporte a mais algoritmos (ECC, Ed25519) estendendo a lógica de geração de chaves em `main_window.py`.
- A interface gráfica usa ttkbootstrap para personalização fácil de temas.

## Registro e Depuração
- Todas as ações, avisos, erros e exceções não capturadas são registradas em `traceback.log`.
- Use `log_info`, `log_warning`, `log_error` para entradas de log personalizadas em seu código.
- O Visualizador de Logs suporta filtragem por TUDO, INFORMAÇÃO, AVISO, ERRO.
- Exceções não capturadas são registradas automaticamente e exibidas no Visualizador de Logs (com rastreamento).

## Solução de Problemas
- Se encontrar erros de importação, verifique se está executando a partir da raiz do projeto.
- Para problemas com dependências, verifique `requirements.txt` ou reinstale os pacotes necessários.

# Guia do Desenvolvedor

Bem-vindo, desenvolvedor! Este guia fornece o essencial para contribuir e estender o Aplicativo OpenPGP GUI.

---

## Estrutura do Projeto
- `main.py` — Ponto de entrada, inicia a janela principal.
- `gui/` — Todos os componentes da interface gráfica (janela principal, widgets, diálogos).
- `struttura/` — Lógica principal, diálogos, utilitários, controle de versão, ajuda/sobre, etc.
- `docs/` — Documentação.
- `requirements.txt` — Dependências do Python.

## Tecnologias Principais
- **Python 3.x**
- **Tkinter** — Framework de interface gráfica (com ttkbootstrap para temas)
- **pgpy** — Criptografia OpenPGP
- **cryptography** — Geração de certificados SSL
- **Pillow** — (opcional) para ícones

## Como Contribuir
1. Faça um fork e clone o repositório.
2. Crie um ambiente virtual e instale as dependências.
3. Siga o PEP8 e mantenha o código modular.
4. Documente novos recursos e atualize o `CHANGELOG.md`.
5. Adicione ou atualize testes, se possível.
6. Abra um pull request com uma descrição clara.

## Adicionando Recursos
- Para adicionar novos algoritmos (ex: ECC), estenda a lógica de geração de chaves em `main_window.py`.
- Para novos componentes de interface, adicione widgets em `gui/` e mantenha a lógica separada da interface.
- Use estilos `ttkbootstrap` para uma aparência consistente.

## Testes
- Adicione testes para novos recursos e correções de bugs.
- Testes manuais: execute `python main.py` e use todas as funções da interface gráfica.
- (Opcional) Integre com CI/CD para testes automatizados.

## Estilo de Código
- Siga o PEP8.
- Use docstrings para funções/classes públicas.
- Mantenha a interface do usuário e a lógica o mais separadas possível.

## Registro e Depuração
- Use `log_info(msg)`, `log_warning(msg)`, `log_error(msg)` em qualquer lugar do código para entradas de log personalizadas.
- Todos os logs são salvos em `traceback.log` e exibidos no Visualizador de Logs.
- O Visualizador de Logs suporta filtragem por TUDO, INFORMAÇÃO, AVISO, ERRO.
- Exceções não capturadas são registradas automaticamente e exibidas no Visualizador de Logs (com rastreamento).

## Suporte e Dúvidas
- Abra issues no GitHub para relatar bugs ou solicitar recursos.
- Consulte `README.md` para informações de contato e contribuição.

---

## Tópicos Avançados

### Referência da API

O aplicativo é modular: a lógica principal está em `struttura/`, a interface gráfica em `gui/`.

**Classes e funções principais:**
- `MainWindow` (`gui/main_window.py`): Lógica principal da interface gráfica e manipulação de eventos.
- `gen_key`, `export_pubkey`, `clear_fields`, etc.: Métodos para operações criptográficas.
- `Help`, `About`, `LogViewer`, etc.: Diálogos e utilitários em `struttura/`.
- `get_version()` (`struttura/version.py`): Retorna a string da versão atual.

Para mais informações, leia os docstrings no código e consulte `docs/user_guide.md` para o fluxo de uso.

### Exemplos de Extensão

#### Adicionando um Novo Algoritmo de Chave
1. Em `gui/main_window.py`, localize o menu suspenso de seleção de algoritmo.
2. Adicione seu novo algoritmo (ex: ECC, Ed25519) às opções do menu.
3. Na lógica de geração de chaves, implemente o tratamento para o novo algoritmo usando `pgpy`.
4. Teste completamente e atualize a documentação.

#### Adicionando um Widget Personalizado
1. Crie seu widget em `gui/widgets.py` ou em um novo arquivo.
2. Importe e use-o em `main_window.py` onde necessário.
3. Siga as convenções de estilo do ttkbootstrap para manter a consistência.

### Diagrama de Arquitetura

Abaixo está uma visão geral da arquitetura em texto simples:

```
Aplicativo OpenPGP GUI
│
├── main.py (ponto de entrada)
│
├── gui/
│   ├── main_window.py (classe MainWindow, lógica de eventos)
│   ├── widgets.py (widgets personalizados)
│   └── ...
│
├── struttura/
│   ├── help.py, about.py, version.py (diálogos, controle de versão)
│   ├── menu.py (lógica da barra de menu)
│   └── ...
│
├── docs/ (documentação)
├── requirements.txt
└── ...
```

Para um diagrama visual, consulte [docs/architecture.png](architecture.png) (adicione seu próprio PNG para mais detalhes).

# Perguntas Frequentes

**P: Posso usar este aplicativo sem conexão com a internet?**  
R: Sim! Todas as operações criptográficas são realizadas localmente para garantir a privacidade.

**P: Como exporto minha chave pública?**  
R: Use o botão 'Exportar Chave Pública' ou a opção no menu Arquivo.

**P: Quais algoritmos são suportados?**  
R: Atualmente RSA; mais algoritmos (ECC, Ed25519) estão planejados.

**P: Onde minhas chaves são armazenadas?**  
R: As chaves são salvas apenas onde você escolher. Não há uploads automáticos nem armazenamento em nuvem.

**P: Como obtenho ajuda?**  
R: Use o menu Ajuda ou leia a documentação na pasta docs/.
