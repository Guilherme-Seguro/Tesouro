Caça ao Tesouro

Jogo simples desenvolvido em HTML, CSS e JavaScript: o jogador precisa atravessar uma masmorra e alcançar o tesouro, desviando de paredes e armadilhas, com um sistema de vidas.

Objetivo:

O projeto foi criado como parte do meu portfólio de programação, com o objetivo de praticar lógica de jogos (movimentação em grade, detecção de colisão, estados de jogo), manipulação de <canvas> e organização de código em funções bem definidas.

Como jogar:
Mova-se com as setas do teclado ou W A S D;
Em telas pequenas, um controle direcional aparece na tela;
Chegue até o tesouro sem esbarrar nas paredes;
Evite as armadilhas (marcadas com ✕) — cada uma tirada custa 1 vida;
Se as vidas chegarem a zero, o jogo termina e é possível tentar novamente;
Ao alcançar o tesouro, a fase é concluída e o jogo avança para a próxima.

Funcionalidades:
3 fases com labirintos progressivamente mais complexos;
Sistema de vidas (3 corações), com feedback visual ao perder uma vida (tela pisca em vermelho e o coração perdido pulsa);
Paredes que bloqueiam a movimentação (com pequena animação de "esbarrão" ao tentar atravessar);
Armadilhas que consomem 1 vida ao serem pisadas (e desaparecem depois de acionadas);
Tesouro desenhado no destino de cada fase;
Telas de Fim de Jogo e Vitória, ambas com opção de reiniciar;
Controle por toque (D-pad) para uso em dispositivos móveis.

Tecnologias utilizadas:
HTML5 + Canvas API (renderização do labirinto);
CSS3 (interface, animações e responsividade);
JavaScript.

Como executar:

Basta abrir o arquivo index.html diretamente no navegador (duplo clique no arquivo). Não é necessário instalar nada nem rodar um servidor local.

Estrutura do código:

Cada fase é representada por uma matriz de caracteres, onde cada símbolo define o tipo de célula:

Símbolo	Significado:
.	Chão;
X	Armadilha;
S	Posição inicial do jogador;
T	Tesouro (objetivo da fase);

Principais funções:

carregarFase — lê a matriz da fase atual, define a posição inicial do jogador e do tesouro, e ajusta o tamanho do tabuleiro;
desenharTabuleiro / desenharCelula — renderizam o labirinto no <canvas> (paredes, chão, armadilhas e tesouro);
mover — processa o movimento do jogador, verificando colisão com paredes, armadilhas e o tesouro;
perderVida — atualiza o contador de vidas e dispara o efeito visual de dano;
concluirFase / proximaFase — controlam a transição entre fases;
reiniciarJogo — reseta vidas e fase atual para uma nova tentativa.
