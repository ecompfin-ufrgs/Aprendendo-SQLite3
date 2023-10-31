# A linguagem Pragma

Referência: [link](https://www.sqlite.org/pragma.html)

A linguagem Pragma é composta por comandos diretos à biblioteca SQLite3 tendo as seguintes características:

1. Não existe garantia de manutenção dos comandos em versões futuras do SQLite3.

2. Não se gera mensagens de erros.  Comandos não compreendidos são simplesmente ignorados.

3. Existem comandos pragma que rodam na compilação da biblioteca, sendo importantes apenas para aqueles que compilarem o SQLite3 nos seus programas.

4. Pragmas são uma extensão do SQL específica do SQLite3.


A sintaxe básico dos comandos pragma é a seguinte:

PRAGMA nome_do_esquema.nome_do_pragma = valor_do_prama

ou

PRAGMA  nome_do_esquema.nome_do_pragma(valor_do_prama)

Veja mais [aqui](https://www.sqlite.org/syntax/pragma-stmt.html)


Os valores dos pragmas podem ser números, nomes ou booleanos (true ou false)
