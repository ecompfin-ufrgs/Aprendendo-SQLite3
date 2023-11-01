
# A estrutura das cláusulas SQL

As cláusulas SQL podem ser escritas sem restrição de forma, isto é, podem conter
múltiplas linhas, espaços, comentários SQL.  Seu marco de terminação é o sinal
de ";" ou "/" ou comando "go".



## Criação de um banco de dados



No terminal do sistema operacional, digite sqlite3 nome_do_banco.db

**Exemplo**: criação do banco de dados eletrotempo.db
```
sqlite3 eletrotempo.db
```

## Criando uma tabela

Digite:

CREATE TABLE nome_da_tabela(coluna1 tipoColuna1, ..., colunaN tipoColunaN);


**Exemplo**: criação da tabela estacaoMeteorologica no banco de dados
eletrotempo.db

CREATE TABLE estacaoMeteorologica (id_estacaometeo int, nomeEstacao text);



## Inserindo dados em uma tabela

Digite:

INSERT INTO nome_da_tabela VALUES (valor1, coluna1 ..., valorN);


**Exemplo**: inserindo dados tabela estacaoMeteorologica no banco de dados
eletrotempo.db

INSERT INTO estacaoMeteorologica (1, 'Maricá');








