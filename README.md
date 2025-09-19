# 🎬 Sistema Multi-Agente para Geração de Vídeos com Google Gemini & VEO 2.0

![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)
![Google Colab](https://img.shields.io/badge/Google%20Colab-Ready-orange.svg)
![Gemini API](https://img.shields.io/badge/Google%20AI-Gemini%201.5%20%7C%20VEO%202.0-green.svg)
![License: MIT](https://img.shields.io/badge/License-MIT-purple.svg)

Este repositório contém um notebook para Google Colab que implementa um sistema autônomo multi-agente para a criação de conteúdo em vídeo. A partir de um único tópico, o sistema orquestra uma equipe de agentes de IA para pesquisar, analisar, roteirizar e, finalmente, gerar um vídeo de alta qualidade usando o modelo **VEO 2.0** do Google.

## 📜 Descrição do Projeto

O objetivo deste projeto é demonstrar o poder de sistemas multi-agente na automação de tarefas criativas complexas. Em vez de um único prompt monolítico, o sistema divide o processo de criação de vídeo em quatro etapas distintas, cada uma executada por um agente especializado, garantindo um resultado final mais coeso, bem estruturado e visualmente atraente.

O projeto é executado inteiramente em um ambiente Google Colab e utiliza uma interface interativa criada com `ipywidgets` para facilitar a configuração e a execução.

## ✨ Funcionalidades Principais

- **Arquitetura Multi-Agente:** Utiliza quatro agentes distintos (Pesquisador, Analista, Roteirista e Visual) para um pipeline de produção robusto.
- **Geração de Conteúdo Automatizada:** Transforma um simples tópico em um roteiro completo, com pesquisa aprofundada e análise de storytelling.
- **Integração com VEO 2.0:** Conecta-se ao modelo de geração de vídeo mais avançado do Google para criar vídeos cinematográficos em 4K.
- **Interface Interativa no Colab:** Permite que o usuário insira o tópico, configure a pasta de saída e inicie o processo com um clique.
- **Organização de Artefatos:** Salva automaticamente todos os resultados intermediários (pesquisa, análise, roteiro, prompt visual) e o vídeo final em uma pasta organizada.

## 🤖 Como Funciona: O Pipeline dos Agentes

O sistema opera em um pipeline sequencial, onde a saída de um agente serve como entrada para o próximo.

1.  **Agente Pesquisador:**
    -   **Entrada:** Um tópico (ex: "Inteligência Artificial na Educação").
    -   **Tarefa:** Realiza uma pesquisa detalhada sobre o tópico, coletando informações sobre conceitos-chave, estado da arte, aplicações práticas e tendências futuras.
    -   **Saída:** Um documento de texto (.txt) com a pesquisa compilada.

2.  **Agente Analista:**
    -   **Entrada:** O texto gerado pelo Agente Pesquisador.
    -   **Tarefa:** Analisa o conteúdo bruto e o estrutura em uma narrativa lógica, identificando os conceitos-chave, um arco de storytelling e sugestões de elementos visuais.
    -   **Saída:** Um documento de análise (.txt) que servirá de base para o roteiro.

3.  **Agente Roteirista:**
    -   **Entrada:** A análise estruturada do Agente Analista.
    -   **Tarefa:** Cria um roteiro de vídeo detalhado, dividido em cenas, com marcações de tempo, narração, descrições visuais e transições.
    -   **Saída:** Um roteiro profissional (.txt) pronto para produção.

4.  **Agente Visual:**
    -   **Entrada:** O roteiro finalizado.
    -   **Tarefa:** Consolida todas as descrições visuais do roteiro em um único **prompt unificado e otimizado** para o modelo de geração de vídeo.
    -   **Saída:** Um prompt visual detalhado (.txt) que descreve o estilo, a paleta de cores, os movimentos de câmera e a narrativa visual do vídeo.

5.  **Geração do Vídeo (VEO 2.0):**
    -   **Entrada:** O prompt visual final.
    -   **Tarefa:** Envia o prompt para a API do Google GenAI, que utiliza o modelo VEO 2.0 para gerar um vídeo de alta qualidade.
    -   **Saída:** Um arquivo de vídeo (.mp4) salvo na pasta do projeto.

## 🛠️ Tecnologias Utilizadas

- **Linguagem:** Python
- **Ambiente:** Google Colab
- **IA Generativa:**
    -   Google Gemini 1.5 Flash (para os agentes de texto)
    -   Google VEO 2.0 (para geração de vídeo)
- **Bibliotecas Principais:**
    -   `google-generativeai`: Para interagir com a API do Gemini.
    -   `ipywidgets`: Para criar a interface interativa no notebook.

## 🚀 Como Usar

Este projeto foi projetado para ser executado com o mínimo de configuração no Google Colab.

1.  **Abra no Google Colab:**
    -   Clique no botão abaixo para abrir o notebook diretamente no Google Colab.
    -   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/seu-usuario/seu-repositorio/blob/main/nome_do_notebook.ipynb)
    -   *(**Atenção:** Substitua `seu-usuario/seu-repositorio` e `nome_do_notebook.ipynb` pelos seus dados reais)*

2.  **Configure a API Key:**
    -   No ambiente do Colab, clique no ícone de chave (🗝️) no menu lateral esquerdo.
    -   Adicione um novo "secret" com o nome `GEMINI_API_KEY`.
    -   Cole a sua chave de API do [Google AI Studio](https://aistudio.google.com/app/apikey) no campo de valor.

3.  **Execute o Notebook:**
    -   Execute a primeira célula para instalar as dependências.
    -   Execute a célula principal que contém a classe `InterfaceVideoIA`.
    -   Siga as instruções na interface interativa: escolha ou digite um tópico e clique em "CRIAR VÍDEO".

4.  **Acesse os Arquivos:**
    -   Após a execução, os arquivos gerados estarão disponíveis na pasta especificada (padrão: `/content/nome_do_projeto_...`).

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.
