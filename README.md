# Modelagem de Banco de Dados

O projeto em parceria com a Dell tem como objetivo desenvolver uma aplicação web com o intuito de otimizar o gerenciamento de tarefas para os gerentes e montadores da fábrica. Levando em consideração a necessidade de armazenar e acessar dados importantes, como o desempenho de um funcionário ou seus dados de login, foi elaborado um banco de dados para garantir o completo desenvolvimento do projeto.

Para realizar a modelagem de um banco de dados, é necessário passar por um processo de três fases, que envolvem a construção conceitual, lógica/relacional e física do banco de dados. A modelagem lógica consiste em organizar as ideias sobre o fluxo e a importância dos dados que serão manipulados. 
Na fase relacional, ou também conhecida como lógica, essas ideias são aplicadas na forma de tabelas, com o uso de relacionamentos entre elas. O modelo físico se baseia na implementação em código, utilizando-se de ferramentas como o PostgreSQL para a sua construção.

O PostgreSQL é um sistema de gerenciamento de banco de dados relacional de código aberto e amplamente utilizado. Além de oferecer recursos avançados de modelagem e manipulação de dados, o PostgreSQL é altamente escalável e suporta a implementação de soluções complexas de bancos de dados.

Essas fases são essenciais para garantir que o banco de dados seja eficiente, seguro e atenda às necessidades do sistema que irá utilizá-lo.


![banco-de-dados (4)](https://github.com/Anacajp/Modelagem-de-Banco-de-Dados/assets/159061342/59cc9e87-f524-43bd-ba77-55d28f5f96f9)


A cardinalidade desempenha um papel crucial no entendimento do fluxo de dados, pois define a proporção ou relação entre conjuntos de dados. Ela indica quantos elementos de um conjunto estão associados a quantos elementos de outro conjunto em um relacionamento.




### Handbooks - Favorites


#### 1:1 


Isso ocorre poia um manual (handbook) pode ser favoridado **uma** única vez, e uma marcação de favorito pode ser distribuida para **um** único manual.


### Handbook - Additional Files


#### N:1 


Um manual pode receber **vários** conteúdos adicionais, como vídeos ou imagens. Por outro lado, um arquivo adicional só poderá ser adicionado em **um** único manual.


### Handbook - Product 


#### N:1 


Um manual pode ensinar sobre **um** produto, mas um produto pode ser ensinado em **vários** manuais.


### Product - Assemble Line 


#### 1:1


Um produto pode ser fabricado em **uma** única linha de montagem, enquanto uma linha de montagem pode fabricar **um** produto.


### User - Assemble Line 


#### 1:N


Um usuário pode trabalhar em **uma** única linha, enquanto uma linha pode conter **diversos** usuários. 


### User - Handbook


#### N:N


*Um usuário pode receber **vários** manuais, e um manual pode ser direcionado à **vários** usuários.
Quando um fluxo é dado por N:N, ou seja, vários para vários, deve haver a mediação de uma outra tabela intermediária. Essa, também conhecida como tabela de junção, é usada para registrar as associações entre os elementos das duas entidades. Para o desenvolvimento desse banco de dados, foi criado a tabela "Task", permitindo representar com mais eficiência esse tipo de relacionamento complexo.*


### User - Task


#### 1:N 


Um usuário pode receber **uma** tarefa, com permissão de editar ela. Por outro lado, a mesma tarefa pode ser distrubuida à **vários** usuários.


### Handbook - Task


#### 1:1


Um manual receberá **uma** única tarefa, enquanto uma tarefa será definida por **um** único manual.


### User - Favorites


#### 1:N


Um favoritado pode pertencer a **um único** usuário, enquanto um usuário pode ter **vários** favoritados.





