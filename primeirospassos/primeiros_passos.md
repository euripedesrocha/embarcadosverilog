Nos últimos meses eu tenho observado um crescente interesse na comunidade maker
sobre o uso e aplicações de FPGAs em projetos. FPGAs possuem um fluxo de
trabalho diferente dos microcontroladores e por isso aquele que tenta dar os seu
primeiros passos acaba esbarrando em várias portas cujas chaves estão por aí
perdidas e a coisa toda parece mais complexa do que é  de fato.

# Motivações

Pra entregar as chaves que abrem essas portas e dar esperança ( Aviso: você
passou por uma piada ruim ) aos que desejam iniciar, resolvi escrever essa série
de textos que tentarão elucidar alguns problemas.

O leitor frequente do Embarcados atentará que diversos artigos já abordaram
aplicações com FPGA, citarei alguns deles durante a série, mas a ideia dessa
série é dar um passo a passo até a conclusão de um projeto que ainda
definiremos. Servirá como um guia introdutório.

# O que teremos nesse artigo?

* Um auxílio para entender o que são FPGAs
* Quais as linguagens e tecnologias envolvidas
* Algumas placas disponíveis no mercado

Resumindo, o que são, o que comem e onde vivem

# O que é um FPGA?

Os FPGA, descritos pelo André Prado [aqui](http://www.embarcados.com.br/fpga/),
são dispositivos eletrônicos que se reconfiguram para formar novos circuitos
digitais. Vamos tentar uma analogia para simplificar.

Imaginemos que você pretende montar um carrinho com blocos de montar. No seu
pequeno projeto de montagem você espera utilizar bloquinhos em forma de
paralelepípedo para construir o chassi, bloquinhos em paralelepípedo, só que
mais baixos para ligar e reforçar a estrutura e alguns bloquinhos que contenham
rodas. Observe que com os mesmos blocos é possível montar outros tipos de
veículos, ou mesmo descartar as rodas e fazer o muro de um pequeno forte. Ou
seja é possível fazer o que a sua imaginação mandar, desde que possua os blocos
necessários e na quantidade desejada.

Com os FPGA acontece exatamente o mesmo. Internamente o dispositivo possui
diversos blocos de circuitos que podem ser configurados e interligados no
intuito de construir e formar circuitos maiores. Com isso podemos construir
circuitos especializados e suprir demandas que ficariam complexas ou impossíveis
com um microcontrolador ou microprocessador.

# Linguagens

O processo de encaixar os blocos em um FPGA é um tanto mais complexo,
descreverei brevemente adiante, que encaixar os blocos de montar. Além disso
temos a necessidade de replicar, e no nosso caso compartilhar o código criado.
Para isso surgiram as linguagens de descrição de hardware. 

O papel dessas linguagens é descrever os circuitos digitais que serão montados
no FPGA em questão.

## VHDL

## Verilog

## MyHDL

# Ferramentas

## Estágios para a geração de  uma imagem

# Placas

