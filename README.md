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

Segue alguns dos sites *gratuitos* para criação do **DER** 
1. [Edraw Max](https://www.edrawmax.com/)
2. [Lucidchart](https://www.lucidchart.com/pages/pt/exemplos/uml-online)
3. [Draw.io (...)](https://app.diagrams.net/)

Utilizei abaixo um modelo que construimos no Lucidchart como exemplo
<div align="center"><img src="https://user-images.githubusercontent.com/57760132/134390890-4a14246d-a8e5-4e93-841f-6a2dfae2c82c.png" width="400" title="source: imgur.com" /></div>

> Tabelas
> Atributos ( nome, email, senha, id)
> 
> [Cardinalidade](https://www.devmedia.com.br/modelagem-1-n-ou-n-n/38894) : identificamos o tipo de relação entre tabelas à partir do valor que está depois da vírgula nas duas tabelas. No caso, temos a cardinalidade de **1:N**
> 
> Fazemos a seguinte pergunta para construir o relacionamento de acordo com a regra de negocio. Para tal modelo o cliente precisa fazer um registro para levar um livro, mas ele pode sair da livraria sem levar nenhum
> 
> 1. Qual mínimo de livros que um cliente pode comprar? R: 0
> 2. Qual máximo de livros que um cliente pode comprar? R: N
> 3. Qual mínimo de clientes que pode comprar um livro? R: 1 
> 4. Qual máximo de clientes que podem comprar o mesmo livro? R:1

Temos também as cardinalidades **1:1** *(one to one)* e **N:N** *(many to many)* que seguem a mesma lógica de construção no DER.

> ## Modelagem lógica

A grande máxima é que no conceitual não temos a chave estrangeira, conforme seguimos para modelagem lógica é acrescentado a [*chave estrangeira*](https://www.devmedia.com.br/sql-aprenda-a-utilizar-a-chave-primaria-e-a-chave-estrangeira/37636) no nosso Diagramas ER(entidade relacional).

Para trabalhar com modelo lógico podemos utilizar agumas ferramentas gratuitas, ou o próprio MySql.
1. [MySql workbench](https://www.mysql.com/products/workbench/)
2. [Astah Professional](https://astah.net/)
3. [DBdesigner](https://www.dbdesigner.net/)

Utilizei abaixo um modelo que construimos no Dbdesigner como exemplo:
<div align="center"><img src="https://user-images.githubusercontent.com/57760132/134400874-b37bf7b3-dd20-4e5d-9d71-01ef697ef17e.png" width="400" title="source: imgur.com" /></div>

> Vale salientar que a *chave estrangeira* sempre vai ficar no lado que tem o N como cardinalidade, olhando a cima percebemos que na relação cliente livros **(1:N)** a chave estrangeira nomeada de *fk_id_livro* origina-se na entidade *tb_livros* e relaciona com *id_cliente*;
> 
> Importante a chave estrangeira ter o mesmo tipo da primária em, não esqueçam!
> 
> No próprio DBdesigner podemos gerar os comandos ( query ) para chegar a o ultimo nível de modelagem física.
> 
> Após concluir o Diagrama, salve o projeto através do menu **Esquema -> Salvar**
> 
> Exporte o Diagrama no formato PDF através do menu **Exportar -> PDF** e faça o download do arquivo
> 
> Gere o código SQL através do  menu **Exportar => SQL**
> 
> Na janela abaixo, clique em **Gerar SQL** e baixe o arquivo no formato SQL
> 

<div align="center"><img src="https://user-images.githubusercontent.com/57760132/134402467-26c10354-ff99-450e-92a1-6e7fe559c324.png" title="source: imgur.com" /></div>








