# Script backup PostGres

Como criar um Backup do PostGres utilizando a lingaguem SHELL

1° - Passo

Incluir as variáveis de ambiente "pg_dump" e "pg_restore" do postgres

2° - Passo

Realizar as mudanças de dados do arquivo tais como:

#!/bin/bash

export PGPASSWORD = "SENHA_DO_POSTEGRES"

pg_dump -U USUÁRIO_POSTGRES -h LOCAL_BANCO_DE_DADOS -O -o -b -F c NOME_BANCO_DADOS > NOME_DO_BACKUP.backup

pg_restore -U USUÁRIO_POSTGRES -h LOCAL_BANCO_DE_DADOS -d NOME_BANCO_DADOS NOME_DO_BACKUP.backup

3° - Passo

Realizar a execução do arquivo Shell.
