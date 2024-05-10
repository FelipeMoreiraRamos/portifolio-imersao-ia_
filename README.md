![Logo design for 'Viral Hit'](logo.png)

# Viral Hit
Criei clipes virais para os seus vídeos longos do Youtube! Este projeto tem como objetivo permitir que qualquer pessoa consiga encontrar os melhores momentos de seus vídeos longos para postar clipes em suas redes sociais. 

Não possui um vídeo para testar? Use esse [aqui](https://www.youtube.com/live/rP-zXlQYCKY)

Este é um projeto para a a 2a edição da Imersão IA_ da Alura + Google.

# Limitações
- No momento, o Viral Hit só aceita vídeos de **8,5 horas** no modo "áudio" ou vídeos menores que **50 minutos** no modo "vídeo" (1080p). Isso é por conta do limite de tokens do Gemini. Futuramente será adicionado para escolher um intervalo de tempo menor que 50 minutos para vídeos mais longos.
- O Viral Hit não cria vídeos e legendas para os clipes. A ideia é não fugir muito do escopo de ChatBot. Por isso o resultado é uma mensagem de texto.
- O Gemini 1.5 Pro gratuito tem um limite de 32.000 Tokens por minuto. Isso é um pouco menos que 2 minutos de vídeo (600 tokens). Então um vídeo de 1 hora demoraria certa de 33 minutos para ser analisado. 

# Como usar
1. Copie o arquivo viral_hit.ipynb para o seu PC
2. Vá para https://colab.research.google.com/
3. Clique em `Arquivo -> Abrir Notebook -> Upload -> Procurar` e selecione o arquivo
4. Adicione a sua chave de API ([Acesse aqui](https://aistudio.google.com/app/apikey?utm_source=website&utm_medium=referral&utm_campaign=Alura&utm_content=)) nos segredos do google colab (é a chave no menu lateral esquerdo). Clique em __Adicionar novo secret__, adicione o nome `GOOGLE_API_KEY` em em valor a sua chave. Não esqueça de ativar o secret!
5. Execute o programa. Você pode ir no menu `Ambiente de execução -> Executar tudo` ou apertar `Ctrl + F9`. Pode aparecer uma mensagem para confirmar o uso dos secrets.
6. A conversa acontecerá no final da página. Inicialmente você terá que adicionar a url do vídeo. Depois o chatbot irá pedir mais detalhes sobre o vídeo. Confirme os detalhes e aguarde.
7. O programa está no modo "áudio". Se quiser tentar o modo "vídeo", substitua **True** por **False** na última linha.

O programa possui várias etapas de processamento. Pode demorar até 2 hora para terminar no modo "vídeo". Fique de olho para que o colab não desconecte o notebook. Se você souber usar IDEs sugiro executar em sua própria máquina.

# Exemplo de Resultado
- Vídeo: https://www.youtube.com/live/rP-zXlQYCKY
- Descrição: É um vídeo de um vtuber jogando jogo de terror em primeira pessoa. Destaque reações do vtuber e momentos de sustos. O resumo deve ter no máximo 5 minutos.
- Resposta: 
```
[00:01:23, 00:01:55] VTuber comenta sobre a estratégia do jogo.
[03:13, 03:19] VTuber expressa nervosismo e ansiedade antes de iniciar o jogo.
[04:41, 04:45] VTuber explica sua condição de "enjoo de movimento" e as adaptações feitas no jogo para minimizar o desconforto.
[07:58, 08:00] VTuber faz uma expressão de tristeza em antecipação aos sustos do jogo.
[15:16, 15:21] Primeiro susto com som alto e figura repentina. A VTuber grita e demonstra surpresa.
[19:42, 19:47] Segundo susto com objeto caindo e som alto. A VTuber expressa mais medo e tensão.
[25:29, 25:35] Terceiro susto com efeito sonoro inesperado. A VTuber se assusta bastante e solta um grito.
[36:52, 36:58] Quarto susto com queda repentina de objetos. VTuber grita e demonstra frustração com a armadilha.
[39:26, 39:30] VTuber se surpreende com a beleza de um cenário inesperado dentro do jogo.
```
