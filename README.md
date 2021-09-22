# MySql

Modelagem de dados é feita antes de começar a desenvolver o banco de dados em si, então pensamos no que importa para nossa resolução.

## Que tabelas preciso?

Vamos começar pelos tipos de modelagem que podemos seguir para construção do nosso modelo relacional, para facilitar o projeto de banco de dados. São representadas pelos seguintes modelos:
<div align="center"><img src="https://user-images.githubusercontent.com/57760132/134388472-3eb9821c-1f20-454f-b7ad-b288486a0a54.png" width="300" title="source: imgur.com" /></div>

> ## Modelagem conceitual
> Também chamado de Diagrama Entidade e Relacionamento (DER), nesse modelo identificaremos todas as entidades(tabelas) e relacionamento de uma forma mais global;
> 
> Esse modelo pode ser melhor compreendido por quem nunca praticou, pois facilita a compreensão semantica dos dados;
> 
> Aqui evitamos qualquer detalhamento mais especifico do modelo do banco de dados(abstração de mais alto nível);
> 
> Sua finalidade é caoturar os requisitos de informação e regras de negócio sob o ponto de vista do negocio.

### beleza camis, mas e aí, como eu posso criar o meu próprio DER definindo a regra de negocio que desejo para implementação do meu banco?
Os diagramas UML (do inglês, Linguagem de Modelagem Unificada) são uma verdadeira “mão na roda” para explicar itens abstratos, como um programa ou um sistema. Eles são muito utilizados porque criam uma espécie de “linguagem visual comum” dentro do complexo universo do desenvolvimento de softwares.

Abaixo alguns dos sites *gratuitos* para criação do **DER** 
1. [Edraw Max](https://www.edrawmax.com/)
2. [Lucidchart](https://www.lucidchart.com/pages/pt/exemplos/uml-online)
3. [Draw.io (...)](https://app.diagrams.net/)

Utilizei abaixo um modelo que construimos no Lucidchart como exemplo
<div align="center"><img src="https://user-images.githubusercontent.com/57760132/134390890-4a14246d-a8e5-4e93-841f-6a2dfae2c82c.png" width="400" title="source: imgur.com" /></div>

> Tabelas
> Atributos ( nome, email, senha, id)
> Cardinalidade : identificamos o tipo de relação entre tabelas à partir do valor que está depois da vírgula. no caso temos a cardinalidade de **1:N**
> Fazemos a seguinte pergunta para construir o relacionamento de acordo com a regra de negocio. Para tal modelo o cliente precisa fazer um registro para levar um livro, mas ele pode sair da livraria sem levar nenhum
> 1. Qual mínimo de livros que um cliente pode comprar? R: 0
> 2. Qual máximo de livros que um cliente pode comprar? R: N
> 3. Qual mínimo de clientes que pode comprar um livro? R: 1 
> 4. Qual máximo de clientes que podem comprar o mesmo livro? R:1












