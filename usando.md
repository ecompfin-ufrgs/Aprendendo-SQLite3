# Usando o cliente SHELL SQLite3

Referência: [link](https://www.sqlite.org/cli.html)

O SQLite shell executa três tipos de comandos, sendo a ordem de preferência
para o "parseamento" dos comandos colocada a seguir:

1. cláusulas SQL;

2. comandos especiais (dot-commands), e

3. comentários CLI.

O shell lê as cláusulas SQL e os comentários CLI os repassa para a biblioteca
SQLite 3 executar. Os comandos especiais e  do shell que são executados por ele
mesmo .


## Os comandos especiais

Referência: [link](https://www.sqlite.org/cli.html#special_commands_to_sqlite3_dot_commands_)


Os comandos especiais servem para mudar o formato de saída das consultas
("queries") e executar queries pré-definidas (pre-packaged).


Estes sempre se iniciam por ".", por isso são chamados de "dot-commands". São
contidos em apenas uma única linha e não podem aparecer no meio de uma cláusula
SQL.  Além disso, não existe a possibilidade de fazer comentários em
dot-commands.

Para saber a lista completa de comandos especiais, digite **.help** no shell do
SQLite 3.  

**Comandos especiais importantes**
 - .exit ou .quit - finalizam o shell do SQLite 3.  Isto também pode ser feito pressionando 
CTRL+ D.

- .open nome_do_banco.db -> abre um banco de dados quando se está dentro do shell.  Também serve para criar um novo banco de dados quando o banco não existe previamente. Ver mais [aqui](https://www.sqlite.org/cli.html#opening_database_files).



- .save nome_do_banco.db -> salva as cláusula sql realizdas no banco de dados temporário no arquivo nome_do_banco.db

- .mode -> altera o formato de exibição dos comandos na janela do shell do sqlite3. VEr detalhes em [link](https://www.sqlite.org/cli.html#changing_output_formats).

Para ver os esquema dos bancos de dados, tem-se estes comandos cuja referência está [aqui](https://www.sqlite.org/cli.html#querying_the_database_schema).

- .tables -> apresenta a lista de tabelas do banco de dados.

- .indexes -> lista os índices de tabelas.

- .schema -> mostra o esquema (isto é, a estrutura de tabelas) do banco de dados.  Use a opção --indent para facilitar a leitura.

- .databases -> lista todos os bancos de dados abertos na conexão atual à biblioteca SQLite3.





## A estrutura das cláusulas SQL

As cláusulas SQL podem ser escritas sem restrição de forma, isto é, podem conter
múltiplas linhas, espaços, comentários SQL.  Seu marco de terminação é o sinal
de ";" ou "/" ou comando "go".

### Comentários CLI

Iniciam-se por sinal # no início da linha sem nenhum caracter antes deles nem 
mesmo espaço em branco.

### Criação de um banco de dados



No terminal do sistema operacional, digite sqlite3 nome_do_banco.db

**Exemplo**: criação do banco de dados eletrotempo.db
```
sqlite3 eletrotempo.db
```

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








