# db_roadmap
# Trilha para a impletação de bases de dados
Os dois pressupostos que apontam para a necessidade da criação de um banco de dados são:
  
* grande volume de dados;  
* necessidade de persistência dos dados;  
  
A persistência aponta para a comunicação de uma informação no futuro. 
  
A comunicação, por sua vez, necessita de um articulador, um intérprete, uma mensagem e um contexto base.
  
A seleção dos dados que serão armazenados devem responder às seguintes perguntas:
* O quê será comunicado? Qual informação será comunicada?
* Para quem?
* Em que contexto?
  
As respostas a essas perguntas são essenciais para definir a estrutura do projeto de um banco de dados.

## Elaboração do modelo conceitual
O modelo conceitual deve abordar todos os dados do banco.  
  
**MER** - Modelo de entidades e relacionamentos:  
  * **Entidades** são abstrações de seres do mundo real, representadas como tabelas;  
  * **Atributos** são características das entidades, representados como colunas;  
  * **Relacionamentos** entre entidades, pode ser representado como uma tabela com atributos próprios ou por meio de uma chave estrangeira em uma das tabelas (entidades) relacionadas.  

Então, selecionar as entidades e relacionamentos, especificando seus atributos.  
Atributos compostos (por dois ou mais atributos) são normalizados e trazidos como atributos da tabela. Cada atributo composto se torna uma coluna da tabela.  

**Chaves** - atributos identificadores (únicos) de entidades tornam-se chaves primárias da tabela respectiva.

**Representação de relacionamentos**  

O relacionamento pode ser representado por meio de uma tabela ou de uma chave estrangeira.  
Tabelas: relacionamentos NxN  
Chave estrangeira: relacionamento 1xN

