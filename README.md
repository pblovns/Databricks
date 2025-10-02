# Databricks



## Formas de Clonar tabelas:

Profunda:

CREATE OR REPLACE nome_da_tabela_clone
DEEP CLONE nome_da_tabela_existente;

Obs: Copia os dados e os metadados.

Superficial:

CREATE OR REPLACE nome_da_tabela_clone
SHALLOW CLONE nome_da_tabela_existente;

Obs: Copia APENAS os metadados.


## Se eu quiser saber quantos versionamentos que já fiz em uma tabela delta:

DESCRIBE HISTORY workspace.amb_teste.tabela_brasileirao;
SELECT * FROM workspace.amb_teste.tabela_brasileirao VERSION AS OF 119;
