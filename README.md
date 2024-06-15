Modelo de Objetos    BingoGame:
        Representa uma instância do jogo Bingo.
        Propriedades:
            BallsInstance: Um objeto BallsCounter que gerencia as bolas do Bingo (letras e números).
            RoundRules: Um objeto InstanceConfig que armazena as regras do jogo (número de bolas, bolas sorteadas, linhas por cartela).
        Construtor:
            Inicializa as regras do jogo.
            Cria a instância BallsCounter para gerar as bolas do Bingo.
    InstanceConfig:
        Armazena as configurações para uma instância específica do jogo.
        Propriedades:
            BallsCount: Número total de bolas no jogo.
            BallsDrawn: Número de bolas a serem sorteadas.
            RowsPerTicket: Número de linhas em cada cartela.
    BallsCounter:
        Gerencia a criação e organização das bolas do Bingo.
        Propriedade:
            GameBalls: Um objeto BingoBalls que contém as bolas organizadas por letra (B-I-N-G-O).
        Construtor:
            Recebe o número total de bolas e cria as bolas do Bingo de acordo com as regras (distribuição de números por letra).
    BingoBalls:
        Representa todas as bolas do jogo, organizadas em colunas por letra.
        Propriedade:
            Balls: Uma lista de objetos LetterBalls, onde cada objeto representa uma coluna de bolas com a mesma letra.
    LetterBalls:
        Representa uma coluna de bolas do Bingo com a mesma letra.
        Propriedades:
            Letter: A letra que identifica a coluna (B, I, N, G, O).
            Balls: Uma lista de números que correspondem às bolas daquela letra.

    GameTicket:
        Representa uma cartela de Bingo.
        Propriedades:
            TicketNumbers: Um objeto BingoBalls que contém os números da cartela, organizados por coluna.
            TicketRows: Uma lista de arrays de inteiros, onde cada array representa uma linha da cartela.
        Construtor:
            Cria uma cartela aleatória com base nas bolas disponíveis no jogo e no número de linhas por cartela.
    DrawBalls:
        Simula o sorteio das bolas do Bingo.
        Propriedades:
            BallsContainer: Uma lista que inicialmente contém todas as bolas do jogo.
            BallsDrawn: Uma lista que armazena as bolas sorteadas.
Funcionamento Geral
    Configuração: O jogo é configurado com o número de bolas, bolas sorteadas e linhas por cartela.
    Criação das Bolas: As bolas do Bingo são criadas e organizadas por letra.
    Geração da Cartela: Uma cartela aleatória é gerada com base nas bolas disponíveis.
    Sorteio: As bolas são sorteadas aleatoriamente.
    Verificação da Cartela: A cartela é verificada em relação às bolas sorteadas para determinar a pontuação */   
