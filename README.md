# Trabalho de Colisão Elástica

## Descrição Básica do Projeto

- **Objetivo e Tipo de Projeto**:
  Criamos um jogo simulação bidimensional onde é possivel visualizar corpos, representados por bolas, se colidindo de forma elástica,
  onde a energia cinética e o momento linear total do sistema se conservam e os corpos envolvidos não sofrem deformações permanentes 
  durante o impacto. Ou seja, após o encontro entre os corpos, a direção, o sentido e o módulo da velocidade é afetado, porém a massa não se altera.
  OBSERVAÇÃO: A parede, ou seja, as bordas da tela, não são consideradas para a colisão e servem apenas para redirecionar o vetor do corpo
  - Manual de Instruções para o Jogo:
    Após executar o código, será aberto uma janela pygame onde o usuário se deparará com um menu contendo 3 opções:
    ```
    ![Imagem do menu incial](images/Imagem do WhatsApp de 2024-12-02 à(s) 20.50.02_1f62514c.jpg)
    ```
    - Iniciar:
    Inicia o jogo pressionando a tecla enter, caso o usuário não mexa em nenhuma configuração, o jogo iniciará com o número
    de corpos e suas respectivas massas e velocidades geradas aleatoriamente.
    (imagem contendo o jogo rodando)
    - Configurar:
    Abre o menu de configurações pressionando a tecla C. navegando por ele através das teclas direcionais (arrow keys) é possivel:
    determinar o intervalo de massa mínima (1) e máxima (2) dos corpos no jogo; Determinar o intervalo de velocidade mínima (3) e máxima (4) dos corpos, e o número de corpos (5). 
    (imagem contendo as configurações)
    Pressionando ESC, o usuário retorna ao menu inicial.
    - Sair:
    pressiona a tecla ESC para fechar o programa.
    - OBSERVAÇÃO:
    Conforme o usuário expande e contrai a janela do jogo, as paredes que fecham a área do jogo seguem o padrão e adaptam seu comprimento. 
    (colocar duas imagens de tamanho diferente para exemplificar essa parte visual do jogo)

## Conceitos de Física e Modelo Matemático

- **Conceito Principal:** Colisão Elástica

  A colisão elástica é um tipo de colisão onde, após o impacto, a energia cinética total e o momento linear total do sistema são conservados. Isso significa que a direção, o sentido e o módulo da velocidade dos corpos são alterados, mas a energia cinética e o momento linear não se perdem, assumindo que não há perdas para outras formas de energia, como calor ou deformação permanente.

## Conceitos de Física e Modelo Matemático

- **Conceito Principal:** Colisão Elástica

  A colisão elástica é um tipo de colisão onde, após o impacto, a energia cinética total e o momento linear total do sistema são conservados. Isso significa que a direção, o sentido e o módulo da velocidade dos corpos são alterados, mas a energia cinética e o momento linear não se perdem, assumindo que não há perdas para outras formas de energia, como calor ou deformação permanente.

- **Modelo Matemático:**  

  O modelo matemático utilizado no jogo é baseado nas **Leis de Newton** e nas **Leis da Conservação da Energia Mecânica**. Durante as colisões elásticas, temos as seguintes equações importantes:

  1. **Conservação do Momento Linear**:

     O momento linear total do sistema (no eixo x e y) é conservado durante a colisão. A fórmula para a conservação do momento linear é dada por:

     ```
     m1 * v1i + m2 * v2i = m1 * v1f + m2 * v2f
     ```

     Onde:
     - `m1` e `m2` são as massas dos corpos 1 e 2, respectivamente.
     - `v1i` e `v2i` são as velocidades iniciais dos corpos 1 e 2, respectivamente.
     - `v1f` e `v2f` são as velocidades finais dos corpos 1 e 2, respectivamente.

  2. **Conservação da Energia Cinética**:

     A energia cinética total do sistema também é conservada durante a colisão elástica, e a fórmula para a conservação da energia cinética é:

     ```
     (1/2) * m1 * v1i^2 + (1/2) * m2 * v2i^2 = (1/2) * m1 * v1f^2 + (1/2) * m2 * v2f^2
     ```

     Onde:
     - `m1` e `m2` são as massas dos corpos.
     - `v1i` e `v2i` são as velocidades iniciais dos corpos.
     - `v1f` e `v2f` são as velocidades finais dos corpos.

  3. **Cálculo das Velocidades Finais**:

     Em uma colisão elástica entre dois corpos, as velocidades finais dos corpos podem ser calculadas usando as fórmulas específicas que derivam da conservação do momento linear e da energia cinética:

     ```
     v1f = [(m1 - m2) * v1i + 2 * m2 * v2i] / (m1 + m2)
     ```

     ```
     v2f = [(m2 - m1) * v2i + 2 * m1 * v1i] / (m1 + m2)
     ```

     Onde:
     - `m1` e `m2` são as massas dos corpos.
     - `v1i` e `v2i` são as velocidades iniciais dos corpos.
     - `v1f` e `v2f` são as velocidades finais dos corpos.

- **Aplicabilidade:**

  O jogo simula como corpos de diferentes massas e velocidades reagem a colisões elásticas entre si, levando em consideração as leis da física mencionadas. No código implementado, as colisões são tratadas de forma a conservar tanto o momento linear quanto a energia cinética dos corpos, aplicando as fórmulas mencionadas para calcular as novas velocidades após cada colisão. Como forças externas como atrito, resistência do ar e gravidade não são consideradas, a simulação é uma idealização simplificada das colisões, sendo útil para a visualização de interações entre corpos em um sistema fechado e para a compreensão básica da física de colisões elásticas.

  ## Implementação

  - **Linguagens e Pacotes:**  
  O projeto foi implementado em Python utilizando os pacotes pygame, sys, random e math. Cada um desses pacotes oferece ferramentas específicas para lidar com visualização, computação científica, interações físicas,         aleatoriedade, permitindo que a simulação seja interativa e visualmente intuitiva.
  
## Como Usar
- **Instalação e Dependências:**  
  -Certifique-se de que o Python 3.6+ (ou outra versão de linguagem) está instalado.
  -Dependências incluem: Math, PyGame, Random.
  -Instale os pacotes necessários executando:
  
  ```
  pip install (coloque a qui o nome da biblioteca que lhe falta)
  ```

- **Exemplos de Uso:** 
  -Para rodar a simulação básica, utilize o código:
  lançamento.py e execute o terminal.

- **Informações sobre o projeto:**
  Este projeto foi desenvolvido por:
  
    Matheus Araujo Pinheiro (14676810): matheusaraujopinh@usp.br
  
    Bruno Gonçalves (14762111): brunogb728@usp.br

    Luis Henrique Ponciano (15577760): luishenriqueponciano@usp.br

    Gabriel Araujo Lima (14571376): gabriel.araujolima@usp.br

Como parte do processo avaliativo da disciplina 7600105 - Física Básica I (2024) da USP-São Carlos ministrada pela(o) [Prof. Krissia de Zawadzki/Esmerindo de Sousa Bernardes]
