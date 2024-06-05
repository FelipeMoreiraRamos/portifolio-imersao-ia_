![Logo design for 'Viral Hit'](logo.png)

# Viral Hit
Crie clipes virais para os seus vídeos longos do Youtube! Este projeto tem como objetivo permitir que qualquer pessoa consiga encontrar os melhores momentos de seus vídeos longos para postar clipes em suas redes sociais. 

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
[03:13 - 03:23] A VTuber comenta sobre o desafio de jogar um jogo de terror devido a sua "motion sickness" e ambientes escuros. Ela expressa preocupação, mas se mostra determinada a jogar pelo bem das outras VTubers envolvidas no projeto.
[07:13 - 07:22] A VTuber revela que, diferentemente do web mangá, ela será o fantasma que assombra os jogadores. Ela demonstra animação com a ideia e curiosidade sobre as reações dos jogadores.
[09:53 - 10:03] A VTuber se confunde com a história do jogo, que difere do web mangá. Ela demonstra surpresa e tenta entender o novo contexto da narrativa.
[14:34 - 14:59] A VTuber ouve batidas na porta e sons estranhos, ficando visivelmente tensa e assustada. Ela questiona se há alguém ali e demonstra alívio quando percebe que não há ninguém.
[15:16 - 15:20] Um susto repentino com um barulho alto faz a VTuber gritar e se assustar. Ela demonstra frustração e comenta que odeia esse tipo de susto "armadilha".
[19:42 - 19:47] Outro susto repentino com um relógio caindo faz a VTuber gritar novamente. Ela ri do próprio susto e comenta que fará uma compilação desses momentos para um vídeo.
[25:29 - 25:35] A VTuber se assusta com um som alto e repentino vindo dos alto-falantes. Ela se encolhe na cadeira e demonstra medo.
[26:21 - 26:30] Uma porta se abre sozinha, assustando a VTuber. Ela se questiona se era a Tokino Sora (outra VTuber) e demonstra alívio ao perceber que não era.
[27:50 - 28:36] A VTuber se assusta com um terremoto e objetos caindo. Ela demonstra preocupação e observa os danos causados pelo tremor.
[36:52 - 36:58] Um susto repentino com um objeto caindo faz a VTuber gritar e se encolher. Ela ri do próprio susto e comenta que foi uma "armadilha".
[37:50 - 38:44] A VTuber se assusta com sons de passos e pingos, além de uma figura fantasmagórica que aparece brevemente. Ela demonstra medo e tensão, mas tenta se manter calma.
```

# Possíveis Temas
Aqui está uma lista detalhada de temas, eventos ou momentos que a IA deve procurar, bem como elementos visuais e pistas de áudio importantes para cada tipo de conteúdo:

### 1. **Comentário**

- **Temas**: Opiniões fortes, análises críticas, debates.
- **Elementos Visuais**: Expressões faciais intensas, uso de gráficos ou clipes para reforçar pontos.
- **Pistas de Áudio**: Mudanças no tom de voz para enfatizar pontos, música de fundo durante transições.

### 2. **Podcast**

- **Temas**: Tópicos controversos, histórias pessoais, entrevistas com convidados.
- **Elementos Visuais**: Reações dos participantes, interações com objetos ou tecnologia.
- **Pistas de Áudio**: Risadas, pausas significativas, efeitos sonoros especiais.

### 3. **Acadêmico**

- **Temas**: Explicações de conceitos complexos, demonstrações práticas, perguntas e respostas.
- **Elementos Visuais**: Slides, demonstrações experimentais, anotações manuscritas.
- **Pistas de Áudio**: Termos técnicos, citações de estudos, perguntas da audiência.

### 4. **How-to**

- **Temas**: Passo a passo crítico, dicas e truques, solução de problemas comuns.
- **Elementos Visuais**: Demonstração de técnicas, close-ups em ações específicas.
- **Pistas de Áudio**: Instruções claras e concisas, feedback sonoro de ferramentas ou materiais.

### 5. **Comédia**

- **Temas**: Piadas, sketches, reações a vídeos engraçados.
- **Elementos Visuais**: Expressões faciais cômicas, gestos exagerados.
- **Pistas de Áudio**: Risadas, timing de piadas, música alegre.

### 6. **Comentário de Esporte**

- **Temas**: Momentos decisivos do jogo, análise tática, reações pós-jogo.
- **Elementos Visuais**: Repetições de jogadas importantes, gráficos de estatísticas.
- **Pistas de Áudio**: Entusiasmo na narração, comentários de especialistas.

### 7. **Notícias**

- **Temas**: Notícias de última hora, atualizações de eventos em andamento, entrevistas.
- **Elementos Visuais**: Clipes de notícias, mapas e infográficos.
- **Pistas de Áudio**: Tons urgentes, mudanças na música de fundo.

### 8. **Vlog**

- **Temas**: Eventos diários, viagens, experiências pessoais.
- **Elementos Visuais**: Locais visitados, interações com pessoas.
- **Pistas de Áudio**: Música de fundo apropriada, diálogo pessoal.

### 9. **Gaming**

- **Temas**: Momentos emocionantes de jogo, tutoriais, reviews de jogos.
- **Elementos Visuais**: Gameplay destacado, reações do jogador.
- **Pistas de Áudio**: Comentários sobre estratégias, sons do jogo.
