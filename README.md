# GameMaster AI 🎮

**GameMaster AI** é um assistente virtual inteligente, construído com Python, Langchain e a API Groq (utilizando o modelo Llama 3), projetado para ajudar usuários a descobrir novos videogames. Ele se engaja em uma conversa proativa e amigável para entender suas preferências e recomendar os títulos mais adequados.

![Exemplo de Interação](link_para_uma_imagem_ou_gif_da_interacao_no_terminal_se_voce_tiver)
*(Opcional: Se você puder capturar uma imagem ou GIF da interação no terminal, adicione aqui)*

## ✨ Funcionalidades Principais

* **Recomendações Personalizadas:** Receba sugestões de jogos baseadas em seus gostos.
* **Interface Conversacional:** Interaja com o AI através de um chat no terminal.
* **Amplo Conhecimento:** O AI possui informações sobre jogos de diversas épocas e plataformas.
* **Exploração Detalhada:** O assistente faz perguntas para refinar a busca, cobrindo:
    * Gêneros (RPG, Ação, Estratégia, etc.)
    * Modos de jogo (Single-player, Multiplayer, Co-op)
    * Plataformas (PC, PlayStation, Xbox, Switch, Mobile)
    * Temas e Atmosferas
    * Jogos de referência (títulos que você amou ou odiou)
* **Informações Concisas:** Para cada sugestão, obtenha nome, breve descrição, gênero, modos de jogo, plataformas e o motivo da recomendação.
* **Memória de Conversa:** O AI lembra o contexto da conversa para fornecer recomendações mais relevantes ao longo do tempo (por sessão).
* **Saída Formatada:** Interação no terminal clara e fácil de ler.

## ⚙️ Como Funciona

Este projeto utiliza:

* **Python:** Linguagem principal de desenvolvimento.
* **Langchain:** Framework para desenvolvimento de aplicações com Modelos de Linguagem (LLMs). Ele orquestra o prompt, o modelo de linguagem e o gerenciamento do histórico da conversa.
* **Langchain-Groq:** Integração específica para utilizar os modelos de linguagem ultrarrápidos da Groq.
* **Groq API (Llama 3):** Fornece o poder do modelo de linguagem Llama 3 para entender as entradas do usuário e gerar respostas e recomendações coerentes.
* **`python-dotenv`:** Para gerenciar chaves de API e outras configurações de ambiente de forma segura.

O fluxo básico é:
1.  O usuário envia uma mensagem.
2.  A mensagem é combinada com o prompt do sistema (que define o comportamento do GameMaster AI) e o histórico da conversa.
3.  Essa informação é enviada para o modelo Llama 3 através da API Groq.
4.  O modelo gera uma resposta.
5.  A resposta é exibida ao usuário no terminal e o histórico da conversa é atualizado.

## 🚀 Configuração e Instalação

1.  **Clone o Repositório:**
    ```bash
    git clone [https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git](https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git)
    cd SEU_REPOSITORIO
    ```

2.  **Crie um Ambiente Virtual (Recomendado):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # No Windows: venv\Scripts\activate
    ```

3.  **Instale as Dependências:**
    ```bash
    pip install -r requirements.txt
    ```
    *(Certifique-se de criar um arquivo `requirements.txt` com as bibliotecas necessárias. Você pode gerar um com `pip freeze > requirements.txt` após instalar tudo listado abaixo).*

    Dependências principais a serem incluídas no seu `requirements.txt`:
    ```
    langchain
    langchain-groq
    python-dotenv
    # Adicione outras dependências se houver
    ```

4.  **Configure as Variáveis de Ambiente:**
    * Crie um arquivo chamado `.env` na raiz do projeto.
    * Adicione sua chave da API Groq ao arquivo `.env`:
        ```env
        GROQ_API_KEY="sua_chave_api_da_groq_aqui"
        ```
    * Você pode obter uma chave da API Groq em [console.groq.com](https://console.groq.com/).

## ▶️ Como Usar

Após a configuração, execute o script Python principal:

```bash
python nome_do_seu_arquivo.py
```
*(Substitua `nome_do_seu_arquivo.py` pelo nome real do seu arquivo Python, por exemplo, `main.py` ou `app.py`)*

Siga as instruções no terminal para interagir com o GameMaster AI. Digite "sair" para encerrar a conversa.

### Exemplo de Interação no Terminal:

```
Bem-vindo ao Assistente de Jogos GameMaster AI!
Digite 'sair' a qualquer momento para encerrar a conversa.
============================================================

GameMaster AI:
Olá! Eu sou o GameMaster AI, pronto para te ajudar a encontrar seu próximo jogo favorito! 🚀 Que tipo de aventura você está buscando hoje?
------------------------------------------------------------

Você: Estou procurando um RPG de fantasia com um bom mundo aberto.

GameMaster AI:
Ótima escolha! RPGs de fantasia com mundo aberto podem ser incrivelmente imersivos. 🤩 Para me ajudar a refinar, você tem alguma preferência em relação ao combate? Por exemplo, prefere em tempo real, por turnos, ou algo mais tático? E alguma plataforma específica em mente (PC, PlayStation, Xbox, etc.)?
------------------------------------------------------------

Você: Combate em tempo real e jogo no PC.

GameMaster AI:
Entendido! Combate em tempo real no PC para um RPG de fantasia de mundo aberto. Tenho algumas sugestões excelentes que podem te interessar:

1.  **Nome do Jogo:** The Witcher 3: Wild Hunt
    * **Breve descrição:** Um RPG de ação aclamado pela crítica, onde você joga como Geralt de Rivia, um caçador de monstros profissional, em busca de sua filha adotiva em um vasto mundo aberto rico em histórias.
    * **Gênero(s) principal(is):** RPG de Ação, Mundo Aberto
    * **Modo(s) de jogo:** Single-player
    * **Plataformas disponíveis:** PC, PlayStation 4/5, Xbox One/Series X/S, Nintendo Switch
    * **Principal motivo:** É um dos jogos de RPG de mundo aberto mais aclamados, com combate em tempo real fluido, uma história envolvente e um mundo incrivelmente detalhado para PC.

2.  **Nome do Jogo:** Elden Ring
    * **Breve descrição:** Dos criadores de Dark Souls, Elden Ring oferece um imenso reino de fantasia para explorar, com combate desafiador em tempo real e uma liberdade sem precedentes.
    * **Gênero(s) principal(is):** RPG de Ação, Soulslike, Mundo Aberto
    * **Modo(s) de jogo:** Single-player, Multiplayer Co-op e PvP
    * **Plataformas disponíveis:** PC, PlayStation 4/5, Xbox One/Series X/S
    * **Principal motivo:** Se você gosta de um desafio e um mundo vasto com muita exploração e combate em tempo real, Elden Ring no PC é uma experiência fantástica.

O que você acha dessas opções? Alguma delas te chama a atenção? 🤔
------------------------------------------------------------

Você: sair

GameMaster AI: Até logo! Espero que encontre jogos incríveis! 🎮
============================================================
```

## 💡 Possíveis Melhorias Futuras

* Integração com APIs de bancos de dados de jogos (como IGDB) para obter informações ainda mais detalhadas e atualizadas.
* Interface gráfica de usuário (GUI) usando bibliotecas como Tkinter, PyQt, ou uma interface web com Flask/Django.
* Suporte a múltiplos idiomas.
* Opção para salvar e carregar históricos de conversas entre sessões.
* Habilidade de buscar trailers ou gameplays dos jogos sugeridos.

## 🤝 Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir uma *issue* ou enviar um *pull request*.

## 📄 Licença

Este projeto é distribuído sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes.
*(Considere adicionar um arquivo LICENSE ao seu repositório. Você pode facilmente gerar um arquivo de licença MIT no GitHub ao criar o repositório ou adicioná-lo depois).*
