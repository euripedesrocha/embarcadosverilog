# Uma introdução a descrição de Hardware

Quando Gordon Moore fez a sua previsão que culminou em sua famosa
[lei](https://pt.wikipedia.org/wiki/Lei_de_Moore), ele
talvez não tivesse a noção de como as ferramentas de desenvolvimento teriam de
evoluir para auxiliar os projetistas em suas tarefas. Ao longo dos anos foram
surgindo as linguagens de descrição de hardware para nos auxiliar a cumprir
parte das tarefas do desenvolvimento de um novo sistema digital.

A wikipedia nos dá uma boa
[definição](https://pt.wikipedia.org/wiki/Linguagem_de_descri%C3%A7%C3%A3o_de_hardware):

```
Em eletrônica, uma linguagem de descrição de hardware ou LDH é qualquer
linguagem de uma classe de linguagens de computador, linguagem de especificação
ou linguagem de modelagem para uma descrição formal e design de circuitos
eletrônicos, e mais comumente, a lógica digital.
```

O Thiago Lima tem seguido com uma série de posts sobre a linguagem Verilog e
tentarei complementar o que ele está escrevendo. Vamos discutir o projeto de
sistemas usando LDH de uma perspectiva mais alto nível e integrando o
conhecimento produzido gerando alguns projetos.

## Pensando em hardware

Embora guardem características com as linguagens de programação voltadas a
processadores as LDH apresetam diferenças fundamentais. Vamos discutir algumas
delas.

# Paralelismo
O primeiro ponto é o paralelismo. Vamos observar que nosso código será dividido
em blocos. Cada um desses trechos é a descrição de um circuito digital. Com isso
cada um desses elementos irá operar ao mesmo tempo e independente da ordem em
que apareçam esses blocos irão executar paralelamente. Um trecho VHDL abaixo
ilustra

``` vhdl
with entrada select
saida1 <=

saida2 <= when
```

# Comunicação entre os blocos

Os equivalentes as variáveis, em uma analogia para facilitar a compreensão, que
são passados entre os blocos do circuito quando chegarem ao dispositivo serão
caminhos físicos. Cada um deles se converterá em um "fio" dentro do dispositivo.
Com isso devemos ter cuidado em não escrever em mais de um momento.

# É HARDWARE!

A despeito de suas similaridades linguagens de descrição de hardware, como o
próprio nome diz, descrevem hardware. Ao escrever o código precisamos ter em
mente qual será o hardware gerado por aquela descrição. Ainda que o façamos em
mais alto nível.

# Eventos

Já estabelecemos que os blocos acontecem em paralelo, mas como podemos entender
a operação do circuito? Simples. As linguagens de decrição de hardware descrevem
o circuito com a ideia de eventos. Os blocos são executados a partir de
gatilhos. Vamos exemplificar para facilitar a compreensão com exemplos, novamente
em VHDL.


``` vhdl
with entrada select
saida1 <=

saida2 <= when
```

Observamos na primeira linha a presença da variável entrada, aos iniciados em
vhdl é um signal, a cada "ciclo de execução" o valor de entrada será avaliado e
saida1 será alterada. Do mesmo modo saida2 sofre alterações conforme xxxxx é
modificado.

Ao falar em ciclos de execução é preciso destacar que a analogia é somente no
intuito de facilitar a compreensão por parte do leitor. No processo de teste e
verificação o simulador utiliza passos de tempo para realizar a simulação. Há
outro tipo de simulador mas vamos nos ater a esse.

Quando o projeto é levado ao dispositivo, em nossa discussão um FPGA, ocorre o
que chamamos de síntese. A descrição de hardware é convertida em circuito
propriamente ocupando parte dosdispositivos digitais que se encontram dentro do
FPGA. No exemplo acima temos um multiplexador.


