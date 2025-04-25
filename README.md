# Chatbot-FURIA
Código com descrição do trabalho
Documentação do Bot Telegram da FURIA
Visão Geral
Este projeto implementa um chatbot para Telegram em português dedicado à marca FURIA. O bot foi projetado para fornecer informações sobre produtos, prazos de entrega, agenda esportiva e escalações dos times da FURIA. Ele utiliza Python e a biblioteca python-telegram-bot para criar uma interface conversacional que atende às dúvidas dos fãs e clientes. as interfaces utlizadas foi o REPLIT e o METAAI, infelizmente não tenho como gravar a tela mas fiz uma gravação externa segue anexada o arquivo 

Estrutura do Projeto
├── main.py              # Ponto de entrada da aplicação
├── bot.py               # Configuração e inicialização do bot Telegram
├── handlers.py          # Manipuladores de mensagens e comandos
├── conversations.py     # Fluxos de conversação estruturados
├── utils.py             # Funções utilitárias gerais
├── responses.py         # Sistema de respostas gerais
├── weather.py           # Funcionalidades relacionadas ao clima (não utilizado na versão FURIA)
├── storage.py           # Sistema de armazenamento de dados dos usuários
├── furia_data.py        # Dados específicos da FURIA (produtos, agenda, escalações)
└── furia_responses.py   # Sistema de respostas específicas da FURIA
Módulos Principais
main.py
Arquivo principal que inicia o bot e configura o ambiente. Na versão atual, contém uma simulação de conversa para demonstração do bot.

# Principais funções:
# - Configuração de logging
# - Simulação de conversação para teste do bot
# - Ponto de entrada da aplicação
bot.py
Responsável pela inicialização e configuração do bot Telegram, incluindo registro de handlers e conexão com a API do Telegram.

# Principais funções:
# - Inicialização do bot com token
# - Configuração dos manipuladores de mensagens
# - Configuração do sistema de polling para receber atualizações
furia_data.py
Contém os dados específicos da FURIA, incluindo informações sobre produtos, coleções, prazos de entrega, agenda esportiva e escalações dos times.

# Principais estruturas de dados:
# - PRODUTOS: Dicionário com informações de produtos
# - COLECOES: Dicionário com informações de coleções especiais
# - ENTREGAS: Dicionário com prazos de entrega por região
# - AGENDA_ESPORTIVA: Dicionário com agenda por modalidade
# - ESCALACOES: Dicionário com escalações por modalidade
# Principais funções:
# - buscar_produto(): Encontra informações de um produto específico
# - buscar_colecao(): Encontra informações de uma coleção específica
# - buscar_prazo_entrega(): Encontra prazos de entrega para uma região
# - buscar_agenda(): Encontra agenda para uma modalidade
# - buscar_escalacao(): Encontra escalação para uma modalidade/campeonato
# - detectar_pergunta_*(): Funções para identificar o tipo de pergunta
furia_responses.py
Responsável pela geração de respostas específicas da FURIA, formatando as informações recuperadas de furia_data.py.

# Principais estruturas de dados:
# - RESPOSTAS: Dicionário com templates de respostas por tipo
# Principais funções:
# - get_random_response(): Obtém uma resposta aleatória de um conjunto
# - formatar_produto(): Formata resposta sobre um produto
# - formatar_colecao(): Formata resposta sobre uma coleção
# - formatar_entrega(): Formata resposta sobre prazos de entrega
# - formatar_agenda(): Formata resposta sobre agenda esportiva
# - formatar_escalacao(): Formata resposta sobre escalação
# - get_*_list(): Funções para listar itens (produtos, coleções, etc.)
# - get_response_furia(): Função principal para gerar respostas
handlers.py
Contém os manipuladores de mensagens e comandos do bot.

# Principais funções:
# - start(): Manipulador para comando /iniciar ou /start
# - help_command(): Manipulador para comando /ajuda ou /help
# - unknown_command(): Manipulador para comandos desconhecidos
# - handle_message(): Manipulador para mensagens de texto
# - handle_callback(): Manipulador para callbacks de botões
# - error_handler(): Manipulador de erros
conversations.py
Implementa fluxos de conversação estruturados, como pesquisas ou formulários.

# Principais constantes:
# - SURVEY_NAME, SURVEY_AGE: Estados da conversa
# Principais funções:
# - start_survey(): In Documentação do Bot Telegram da FURIA
## Visão Geral
Este projeto implementa um chatbot para Telegram em português dedicado à marca FURIA. O bot foi projetado para fornecer informações sobre produtos, prazos de entrega, agenda esportiva e escalações dos times da FURIA. Ele utiliza Python e a biblioteca python-telegram-bot para criar uma interface conversacional que atende às dúvidas dos fãs e clientes.
## Estrutura do Projeto
├── main.py # Ponto de entrada da aplicação
├── bot.py # Configuração e inicialização do bot Telegram
├── handlers.py # Manipuladores de mensagens e comandos
├── conversations.py # Fluxos de conversação estruturados
├── utils.py # Funções utilitárias gerais
├── responses.py # Sistema de respostas gerais
├── weather.py # Funcionalidades relacionadas ao clima (não utilizado na versão FURIA)
├── storage.py # Sistema de armazenamento de dados dos usuários
├── furia_data.py # Dados específicos da FURIA (produtos, agenda, escalações)
└── furia_responses.py # Sistema de respostas específicas da FURIA

## Módulos Principais
### main.py
Arquivo principal que inicia o bot e configura o ambiente. Na versão atual, contém uma simulação de conversa para demonstração do bot.
```python
# Principais funções:
# - Configuração de logging
# - Simulação de conversação para teste do bot
# - Ponto de entrada da aplicação
bot.py
Responsável pela inicialização e configuração do bot Telegram, incluindo registro de handlers e conexão com a API do Telegram.

# Principais funções:
# - Inicialização do bot com token
# - Configuração dos manipuladores de mensagens
# - Configuração do sistema de polling para receber atualizações
furia_data.py
Contém os dados específicos da FURIA, incluindo informações sobre produtos, coleções, prazos de entrega, agenda esportiva e escalações dos times.

# Principais estruturas de dados:
# - PRODUTOS: Dicionário com informações de produtos
# - COLECOES: Dicionário com informações de coleções especiais
# - ENTREGAS: Dicionário com prazos de entrega por região
# - AGENDA_ESPORTIVA: Dicionário com agenda por modalidade
# - ESCALACOES: Dicionário com escalações por modalidade
# Principais funções:
# - buscar_produto(): Encontra informações de um produto específico
# - buscar_colecao(): Encontra informações de uma coleção específica
# - buscar_prazo_entrega(): Encontra prazos de entrega para uma região
# - buscar_agenda(): Encontra agenda para uma modalidade
# - buscar_escalacao(): Encontra escalação para uma modalidade/campeonato
# - detectar_pergunta_*(): Funções para identificar o tipo de pergunta
furia_responses.py
Responsável pela geração de respostas específicas da FURIA, formatando as informações recuperadas de furia_data.py.

# Principais estruturas de dados:
# - RESPOSTAS: Dicionário com templates de respostas por tipo
# Principais funções:
# - get_random_response(): Obtém uma resposta aleatória de um conjunto
# - formatar_produto(): Formata resposta sobre um produto
# - formatar_colecao(): Formata resposta sobre uma coleção
# - formatar_entrega(): Formata resposta sobre prazos de entrega
# - formatar_agenda(): Formata resposta sobre agenda esportiva
# - formatar_escalacao(): Formata resposta sobre escalação
# - get_*_list(): Funções para listar itens (produtos, coleções, etc.)
# - get_response_furia(): Função principal para gerar respostas
handlers.py
Contém os manipuladores de mensagens e comandos do bot.

# Principais funções:
# - start(): Manipulador para comando /iniciar ou /start
# - help_command(): Manipulador para comando /ajuda ou /help
# - unknown_command(): Manipulador para comandos desconhecidos
# - handle_message(): Manipulador para mensagens de texto
# - handle_callback(): Manipulador para callbacks de botões
# - error_handler(): Manipulador de erros
conversations.py
Implementa fluxos de conversação estruturados, como pesquisas ou formulários.

# Principais constantes:
# - SURVEY_NAME, SURVEY_AGE: Estados da conversa
# Principais funções:
# - start_survey(): Inicia uma conversa de pesquisa idade
# - cancel_survey(): Cancela uma conversa em andamento
# - end_survey(): Finaliza uma conversa
storage.py
Implementa um sistema simples de armazenamento de dados dos usuários.

# Principais classes:
# - UserData: Classe para armazenamento e manipulação de dados de usuários
# Principais métodos:
# - get_user_data(): Obtém dados de um usuário específico
# - save_user_data(): Salva ou atualiza dados de um usuário
# - delete_user_data(): Remove dados de um usuário
# - get_all_users(): Obtém dados de todos os usuários
# - print_stats(): Exibe estatísticas de uso
# - export_data()/import_data(): Exporta/importa dados para/de arquivos
utils.py
Contém funções utilitárias usadas em vários módulos.

# Principais funções:
# - detect_language(): Detecta o idioma de um texto
# - is_about_language(): Verifica se texto é sobre preferência de idioma
# - extract_intent(): Extrai a intenção básica de uma mensagem
Fluxo de Funcionamento
O usuário inicia uma conversa com o bot enviando /iniciar ou /start
O bot responde com uma mensagem de boas-vindas e instruções
O usuário pode enviar comandos específicos ou fazer perguntas em linguagem natural
O sistema analisa a mensagem para identificar o tipo de pergunta:
Pergunta sobre produto
Pergunta sobre coleção
Pergunta sobre prazo de entrega
Pergunta sobre agenda esportiva
Pergunta sobre escalação
O bot busca as informações relevantes e formata uma resposta apropriada
A resposta é enviada ao usuário
O ciclo continua até que o usuário encerre a conversa
Funcionalidades Principais
Informações sobre Produtos

Preços, tamanhos, disponibilidade e descrições
Produtos individuais e coleções especiais
Comando /produtos para listar todos os produtos
Prazos de Entrega

Estimativas de tempo de entrega por região/estado
Informações sobre frete
Agenda Esportiva

Próximos jogos e eventos por modalidade
Datas, locais e adversários
Comando /agenda para ver toda a agenda
Escalações

Jogadores titulares por modalidade
Informações sobre próximos jogos
Comando /escalacoes para ver todas as equipes
Configuração e Execução
Para executar o bot em um ambiente de produção:

Configuração do Token

Obtenha um token de bot com o BotFather no Telegram
Configure o token como variável de ambiente: TELEGRAM_BOT_TOKEN
Instalação de Dependências

pip install python-telegram-bot==13.7
Execução do Bot

python main.py
Modo de Simulação

Para testar sem conexão ao Telegram, utilize o modo de simulação incluído
Notas de Desenvolvimento
O bot foi desenvolvido usando a versão 13.7 do python-telegram-bot
Todas as mensagens estão em português
Os dados (produtos, agenda, escalações) são exemplos para demonstração
Em um ambiente de produção, esses dados deveriam vir de uma API ou banco de dados
O sistema foi projetado de forma modular para facilitar atualizações e expansões
Possíveis Melhorias Futuras
Integração com sistema de e-commerce real
Adição de botões interativos e menus
Integração com API de pagamentos
Sistema de notificações para jogos ao vivo
Personalização baseada em preferências do usuário
Integração com sistema de CRM
