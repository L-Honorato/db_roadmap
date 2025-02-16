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
A tabela que representa um relacionamento é identificada pelas chaves primárias das tabelas relacionadas.  

## Criação do BD

Criam-se as tabelas e seus atributos com a fração DDL da linguagem SQL.  
Os atributos podem possuir **restrições de integridade**, que podem ser **estruturais** ou de **regras negócio**.  

As restrições estruturais levam em conta o modelo lógico escolhido. No modelo relacional, as restrições levam em conta a representação dos dados em tabelas, também chamadas de relações. Podem ser:  
* restrições de integridade de chave: controle de unicidade das tuplas (chaves primárias);  
* restrições de integridade referenciais: chaves estrangeiras;  
* restrições de entidade: valores nulos não podem ser considerados válidos em uma chave primária, pois não é possível diferenciar dois valores nulos;  
* restrições de domínio: regras de valores válidos para cada atributo.

As restrições relativas a regras de negócio impõe a validade ou não de determinados valores dos dados e são independentes do modelo lógico escolhido. Podem coincidir com as restrições de domínio.  

**DDL - Data Definition Language**  
Comandos SQL com finalidade estrutural. Definem a estrutura da base de dados.  
  
* CREATE TABLE - cria tabela
* ALTER TABLE - altera a estrutura da tabela
* DROP TABLE - exclui a tabela  

**Comandos de restrição de integridade**  
Comandos que dizem respeito a estrutura dos dados  
  
* PRIMARY KEY - chave primária
* FOREING KEY - chave estrangeira
* UNIQUE - restrição de unicidade
* NOT NULL - proibição de valores nulos
* CHECK - restrição de validação
* DEFAULT - definição de valor padrão
* ON DELETE/ON UPDATE - Controla o comportamento ao excluir ou atualizar registros referenciados por uma FOREING KEY
* DATA TYPE numéricos - NUMERIC (ou DECIMAL), INT (ou INTEGER), SMALLINT, BIGINT, FLOAT, REAL, DOUBLE PRECISION
* DATA TYPE texto - CHAR, VARCHAR, TEXT
* DATA TYPE data e hora - DATE, TIME, TIMESTAMP, DATETIME
* DATA TYPE booleanos - BOOLEAN
* DATA TYPE binários - BLOB, BYTEA
* DATA TYPE especiais - UUID, SERIAL, AUTO_INCREMENT

**DML - Data Manipulation Language**  
Comando utilizados para manuseio dos dados instanciados. Permitem a inserção, exclusão ou alteração dos dados. 

* INSERT - insere dados nas tabelas
* DELETE - exclui tuplas
* UPDATE - altera tuplas
* 
