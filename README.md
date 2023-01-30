# Introdução ao Sistema de Gerenciamento de Banco de Dados SQLite 3


## Introdução

Os usuários de computadores bem como suas aplicações armazenam e realizam
operações sobre dados.  Quando o volume destes dados é reduzido, eles podem ser
armazenados diretamente em arquivos contidos no disco rígido do sistema 
computacional, porém isto não é eficiente quando o volume de dados é elevado.
Isto porque se torna difícil a realização de todas as operações fundamentais 
sobre dados, quais seja, "CREATE, RETRIEVE, UPDATE and DELETE (CRUD).  Nestas
situações, necessita-se do emprego de um sistema gerenciador de bancos de dados.

O SQLite 3 é um sistema gerenciador de banco de dados que se caracteriza por
simplicidade, portabilidade e eficiência de operação.  Entre as suas mais
destacadas funcionalidades encontram-se a possibilidade de tratar arquivos CSV e 
ZIP como se fossem arquivos de bancos de dados! Por tudo isso, o SQLite 3
é adotado pelos principais sistemas operacionais para celular (Android e iOS),
sendo por isso o sistema gerenciador de banco de dados mais usado no mundo.

Vamos aprender as principais funcionalidades do SQLite 3.


## A arquitetura do SQLite 3

O SQLite 3 é um sistema gerenciador de banco de dados consiste em uma biblioteca
de código escrita em C que aceita cláusulas SQL para serem executadas sobre um
arquivo com extensão .db que armazena os dados propriamente ditos.

A biblioteca possui API para outras linguagens de programação e, em particular,
para a linguagem Python que a inclui como um pacote de sua biblioteca-padrão.
Além disso, o SQLite 3 oferece diversas ferramentas, sendo a mais importante o
aplicativo de linha de comando SHELL SQLite permite a manipulação das bases de
dados .db do SQLite 3 diretamente, isto é, sem a necessidade de emprego de uma
linguagem de programação.  Destaca-se também o SQLite Archiver que oferece a 
funcionalidade de leitura de arquivos ZIP para armazenamento de dados.


## Usando o cliente SHELL SQLite3

O SQLite shell executa três tipos de comandos, sendo a ordem de preferência
para o "parseamento" dos comandos colocada a seguir:

1. cláusulas SQL;

2. comandos especiais (dot-commands), e

3. comentários CLI.

O shell lê as cláusulas SQL e os comentários CLI os repassa para a biblioteca
SQLite 3 executar. Os comandos especiais e  do shell que são executados por ele
mesmo .

### Comandos do shell SQLite3

#### A estrutura das cláusulas SQL

As cláusulas SQL podem ser escritas sem restrição de forma, isto é, podem conter
múltiplas linhas, espaços, comentários SQL.  Seu marco de terminação é o sinal
de ";" ou "/" ou comando "go".

#### Os comandos especiais

Os comandos especiais servem para mudar o formato de saída das consultas
("queries") e executar queries pré-definidas (pre-packaged).


Estes sempre se iniciam por ".", por isso são chamados de "dot-commands". São
contidos em apenas uma única linha e não podem aparecer no meio de uma cláusula
SQL.  Além disso, não existe a possibilidade de fazer comentários em
dot-commands.

Para saber a lista completa de comandos especiais, digite **.help** no shell do
SQLite 3.  O .exit ou .quit são particularmente importantes, pois
finalizam o shell do SQLite 3.  Isto também pode ser feito pressionando 
CTRL+ D.



#### Comentários CLI

Iniciam-se por sinal # no início da linha sem nenhum caracter antes deles nem 
mesmo espaço em branco.


### Criação de um banco de dados



No terminal do sistema operacional, digite sqlite3 nome_do_banco.db

**Exemplo**: criação do banco de dados eletrotempo.db

sqlite3 eletrotempo.db


### Criando uma tabela

Digite:

CREATE TABLE nome_da_tabela(coluna1 tipoColuna1, ..., colunaN tipoColunaN);


**Exemplo**: criação da tabela estacaoMeteorologica no banco de dados
eletrotempo.db

CREATE TABLE estacaoMeteorologica (id_estacaometeo int, nomeEstacao text);



### Inserindo dados em uma tabela

Digite:

INSERT INTO nome_da_tabela VALUES (valor1, coluna1 ..., valorN);


**Exemplo**: inserindo dados tabela estacaoMeteorologica no banco de dados
eletrotempo.db

INSERT INTO estacaoMeteorologica (1, 'Maricá');








