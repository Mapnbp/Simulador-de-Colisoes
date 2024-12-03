# Jogo de Hóquei de Mesa (Air Hockey)

## Descrição Básica do Projeto

- **Objetivo e Tipo de Projeto**:
  O objetivo deste projeto era simular um jogo de hóquei de mesa em um ambiente bidimensional, onde dois jogadores controlam discos e tentam marcar gols no adversário. 
  O jogo iria incluir interações físicas realistas, baseadas na conservação do momento e em colisão elástica, com discos e jogadores se movendo dentro dos limites da tela,
  colidindo entre si e com as paredes, e alterando suas velocidades conforme as colisões.
  O sistema era projetado para ser simples, mas interativo, permitindo ajustes nas velocidades dos discos e dos jogadores diretamente durante o jogo. Também seria possivel
  alterar a massa do sistema, e durante o jogo seria apresentado o vetor direção sobre cada objeto, além da velocidade atual e aceleração do disco.
  As configurações podem ser modificadas através de um menu de opções.
  Infelizmente não conseguimos terminar de implementar, porém esse projeto será finalizado mais tarde, ainda que exclusivamente por experiência individual.
  Optamos por seguir com o outro projeto apresentado, mas que usa algumas das ideias que estariam presentes nesse código.

- Manual de Instruções para o Jogo: Ao executar o código, uma janela do Pygame será aberta com o menu principal, que contém as seguintes opções:
  - Iniciar:
  Inicia o jogo pressionando a tecla Enter. Se o usuário não alterar as configurações, o jogo começará com valores padrão para as massas, velocidades e o número de discos. O objetivo é marcar gols no adversário e evitar que o outro jogador faça o mesmo.
  
  - Configurar:
  Ao pressionar a tecla "C", o usuário pode acessar o menu de configurações, onde é possível:
  
  Ajustar a velocidade máxima do disco e dos jogadores.
  Definir as massas dos discos e dos jogadores.
  Alterar o número de discos no jogo.
  A navegação é feita com as teclas de seta. Pressionando "ESC", o usuário retorna ao menu principal.
  
  - Sair:
  Ao pressionar a tecla "ESC", o programa será fechado.
  
  - Observações:
  O jogo se adapta automaticamente caso a janela seja redimensionada, ajustando as dimensões das bordas para manter a área de jogo consistente.
  


## Conceitos de Física e Modelo Matemático
- Conceito Principal:
O jogo simula colisões elásticas entre discos e jogadores. Durante o impacto, a velocidade dos corpos muda, mas a energia e o momento linear total do sistema são conservados.

- Modelo Matemático:
O modelo é baseado nas leis de Newton para colisões elásticas, onde os corpos podem mudar sua direção e velocidade sem deformações permanentes. 
A colisão entre os discos e as paredes da tela redireciona os corpos sem alterar sua energia ou momento linear.

- Aplicabilidade:
Este projeto pode ser utilizado para entender as interações físicas básicas de colisões em um ambiente controlado, 
com a simplificação de não considerar forças como atrito ou resistência do ar.

- Implementação
Linguagens e Pacotes:
O jogo foi desenvolvido em Python utilizando os pacotes:
Pygame: Para a interface gráfica e controle do jogo.
math: Para cálculos e funções matemáticas relacionadas ao movimento dos objetos.
Como Usar
Instalação e Dependências:
Certifique-se de que o Python 3.6+ esteja instalado. Instale as dependências utilizando o comando:

Copiar código
pip install -r requirements.txt
Exemplos de Uso:
Para rodar o jogo, basta executar o arquivo principal:

Copiar código
python jogo_air_hockey.py
Informações sobre o Projeto
- **Informações sobre o projeto:**
  Este projeto foi desenvolvido por:
  
    Matheus Araujo Pinheiro (14676810): matheusaraujopinh@usp.br
  
    Bruno Gonçalves (14762111): brunogb728@usp.br

    Luis Henrique Ponciano (15577760): luishenriqueponciano@usp.br

    Gabriel Araujo Lima (14571376): gabriel.araujolima@usp.br

Como parte do processo avaliativo da disciplina 7600105 - Física Básica I (2024) da USP-São Carlos ministrada pela(o) Prof. Krissia de Zawadzki / Esmerindo de Sousa Bernardes.
