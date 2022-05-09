
# Projeto de 1ºano, Programação 1 e 2.
Projeto de 1ºano, do curso de Tecnologias de Informação <br>
Cadeira: Programação 1 e 2 

## Objetivo da Cadeira
Desenvolver a capacidade de resolver de problemas com recurso a algoritmos e métodos de programação através de uma linguagem de programação, ser capaz projetar, codificar, testar, visualizar, analisar e depurar funções e programas e também dominar um conjunto de ferramentas para ajudar na resolução de problemas. <br>
A linguagem veículo é Python 3.

#### Nota final: 17 valores.

## Enunciado
Esta versão contém apenas 250 linhas no ficheiro csv, por causa do limite de tamanho de ficheiros no GitHub <br>

O objetivo deste trabalho é desenvolver um analisador de jogos de xadrez. O ficheiro xadrez.csv contém informação sobre mais de 100 mil jogos de
xadrez jogados pelas melhores jogadoras do mundo. No final deste enunciado encontra uma descrição do conteúdo de cada coluna neste ficheiro.
O programa deve executar a partir da linha de comandos. Os argumentos passados na linha de comandos determinam a execução do programa. O
modo geral de interagir com o vosso trabalho é o seguinte:

$ python projeto.py ficheiro.csv comando opcoes 

onde ficheiro.csv é um ficheiro csv com a informação sobre jogos de xadrez (xadrez.csv por exemplo), comando é um dos seis comandos
descritos abaixo e opcoes descreve um conjunto de opções específicas para cada comando, descritas juntamente com cada comando.

#### Operação anos O comando
$ python projeto.py xadrez.csv anos

gera os dois gráficos na figura 1. Tratam-se de dois gráficos sobrepostos na esma figura, com um eixo das abcissas comum, e dois eixos distintos para as
ordenadas, um à esquerda (como habitualmente), e outro à direita, tal como escritos abaixo.

- Gáfico de barras onde as abcissas são os anos (2009, . . . , 2021) e as ordenadas são o número de jogos. Deve usar o eixo da esquerda para o valor das ordenadas.
- Curva em que as abcissas são as mesmas do gráfico anterior, isto é, o valor dos anos, e as ordenadas são o número de jogadoras. Deve usar o eixo do lado direito para as ordenadas.

![image](https://user-images.githubusercontent.com/105118849/167372906-b61b04f2-7742-43cb-91cb-63d0e0f679b0.png)

#### Operação classes O comando
$ python projeto.py xadrez.csv classes

![image](https://user-images.githubusercontent.com/105118849/167373135-6c90a914-9828-45ec-8417-b3f8202d88cc.png)

gera os cinco gráficos na figura 2. Trata-se de uma figura com os gráficos da distribuição de jogos por formato de jogo. Os jogos de xadrez online podem ser jogados com várias restrições de tempo de jogo; dividem-se em 4 classes: rapid, daily, bullet e blitz. Cada uma destas classes tem vários formatos,
representando o tempo para cada jogador, como por exemplo: 180 (cada jogador tem 180 segundos, ou seja, três minutos), 600+2 (cada jogador tem
600 segundos, ou seja, dez minutos, com incrementos de dois segundos a cada jogada), 1/259200 (cada jogador tem três dias para fazer o próximo lance).

A figura deve apresentar, por omissão, o top-5 dos formatos mais populares, isto é, dos formatos com maior número de jogos ao longo de todos os anos.
No entanto, caso a opção -c n esteja presente na linha de comandos, o gráfico deve apresentar as n classes mais populares, isto é, com maior número de
jogos. O exemplo na figura 3 pode ser gerado com o seguinte comando.

$ python projeto.py xadrez.csv classes -c 3

![image](https://user-images.githubusercontent.com/105118849/167373448-5d4639d8-a018-4d26-8acf-c35b2a00a778.png)

Em qualquer caso, o gráfico time_class deve apresentar sempre as 4 classes principais: rapid, daily, bullet e blitz

#### Operação vitorias O comando
$ python projeto.py xadrez.csv vitorias

gera o gráfico na figura 4. Trata-se de um gráfico de barras em que as abcissassão os nomes das jogadoras e as ordenadas são as percentagens de vitórias

![image](https://user-images.githubusercontent.com/105118849/167373663-31c269e5-f6a3-4bc1-9f8f-b4e14dcc27c9.png)

quando o jogo se inicia com as peças brancas e quando se inicia com as peças pretas. Este gráfico mostra, por omissão, dados referentes apenas às cinco
jogadoras com mais jogos jogados. A opção -c n controla o número de jogadoras a apresentar.

Em alternativa à opção -c, este comando aceita uma outra opção, -u u1 . . . un, que permite especificar os nomes das n jogadoras a comparar com nomes de
utilizador u1, . . . , un. Por exemplo, a figura 5 mostra o gráfico para as jogadoras com o nome de utilizadora budu44 e advantagelucy, obtido com o
seguinte comando.

$ python projeto.py xadrez.csv vitorias -u budu44 advantagelucy <br>
As opções -c e -u não podem ser utilizadas em conjunto.

#### Operação seguinte O comando
$ python projeto.py xadrez.csv seguinte

gera o gráfico na figura 6, um gráfico de barras das top-5 jogadas mais prováveis após uma dada jogada. A jogada por omissão é e4 (que corresponde
a avançar o peão de rei duas casas). Neste caso ficamos a saber que, após a jogada e4, as jogadas mais comuns são: c5 (avançar o peão da coluna c duas
casas; a chamada defesa siciliana), e5 (avançar o peão de rei duas casas), e6 (avançar o peão de rei uma casa), c6 (avançar o peão da coluna c uma casa) e
Nf6 (mover o cavalo de rei para f6). A jogada a considerar pode ser passada na linha de comandos, como opção. Por exemplo, -j e4 indica que o gráfico
deve apresentar as jogadas mais prováveis que sucedem à jogada e4. 

À semelhança do caso anterior, este comando deve também mostrar por omissão o top-5 das jogadas mais comuns e deve aceitar a opção -c n para
especificar o número de jogadas n a considerar.

![image](https://user-images.githubusercontent.com/105118849/167374290-30e60dd4-2537-4d5a-b32b-7c36b2b8d7de.png)

![image](https://user-images.githubusercontent.com/105118849/167374353-4dc199bc-83f3-432d-aaa9-9fe2a04b09bf.png)



















