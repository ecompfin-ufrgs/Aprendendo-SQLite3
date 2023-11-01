# Tutorial TutorialsPoint

Referência

[link](https://www.tutorialspoint.com/sqlite/)


## Introdução

SQLite é uma biblioteca que implementa um banco de dados autocontido em arquivo, sem servidor ou configuração como um motor de banco de dados transacional SQL.

Há coisas importantes não suportadas pelo SQLite.  Confira [aqui](https://www.tutorialspoint.com/sqlite/sqlite_overview.htm)


## A SQL

**Data definition language (DDL)**

- create
- alter
- drop

**Data manipulation language**
- insert
- update
- delete

**Data query language**
- select

## Instalação

Confira [aqui](https://www.tutorialspoint.com/sqlite/sqlite_installation.htm)

## Commands

## Syntax

## Data Type

- NULL
- INTEGER
- REAL
- TEXT
- BLOB

## Create database

No terminal de comandos do sistema operacional, digite:

`sqlite3 DatabaseName.db`


**O comando dump**

Exporta um banco de dados para um arquivo no formato **.sql** que permite reconstruir o banco de dados em caso de corrupção do banco de dados original.  Veja os usos.

1. Salvando o banco de dados

No terminal do SO, digite

`sqlite3 databaseName.db .dump > databaseName.sql`

2. Para reconstruir o banco de dados, digite

`sqlite3 databaseName.db < databaseName.sql`



## Attach database

Este comando associa um banco de dados existente ao shell sqlite2 para ser manipulado.  Se o banco de dados não existe, o comando o cria.  Deste modo, este comando sql é análogo ao comando especial .open.

A sintaxe é a seguinte:

`attach database 'nome_do_banco.db' as 'nome_do_banco'; `

## Detach dabase

Referência: [link](https://www.tutorialspoint.com/sqlite/sqlite_detach_database.htm)

Serve para desfazer uma conexão realizada por attach.

Sintaxe:

`DETACH DATABASE "nome_do_banco";

## Create table

`CREATE TABLE database_name.table_name(
   column1 datatype PRIMARY KEY(one or more columns),
   column2 datatype,
   column3 datatype,
   .....
   columnN datatype
);`