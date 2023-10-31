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
