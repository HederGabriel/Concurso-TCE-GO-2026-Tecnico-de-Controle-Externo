# Transações
São blocos de intruções que devem ser executados pelo SGBD e que possui 4 características
> Comando de exemplo estão em postgreSQL

**ACID**:

- [Atomicidade](#atomicidade)
- [Consistência](#consistência)
- [Isolamento](#isolamento)
- [Durablidade](#durablidade)

## Atomicidade
implica que todos os comandos no bloco da transação precisam ser executados na lógica, tudo ou nada.
> Ou todos os comandos são executados ou nenhum deve ser executado

## Consistência
todas as restrições do BD precisam ser mantidas ou garantidas depois que a transação é efetivada

## Isolamento
significa que cada transação precisa ser executada de forma isolada 

## Durablidade
As transações devem ser salvas no banco de dados

## Exemplo
| nro_conta | nome_titular | saldo       |
|-----------|--------------|-------------|
| 1         | Marta        | 25.400,00   |
| 2         | Lucas        | 1.281,34    |
| 3         | Ana          | 85,12       |
| 4         | Fábio        | 172.191,23  |
| 5         | Bruna        | -125,00     |

Comando *sql*:
```sql
UPDATE conta SET saldo = saldo - 100
    WHERE nro_conta = 1;

UPDATE conta SET saldo = saldo + 100
    where nro_conta = 4;
```

Transação (BEGIN/COMMIT):
```sql
BEGIN;
    UPDATE conta SET saldo = saldo - 100 WHERE nro_conta = 1;
    UPDATE conta SET saldo = saldo + 100 WHERE nro_conta = 4;
COMMIT;
```
> Se o SGBD identificar algum problema ele automaticamente faz o *ROLLBACK*;

Savepoint
```sql
BEGIN;
    UPDATE conta SET saldo = saldo - 100 WHERE nro_conta = 1;

    SAVEPOINT debitoEmConta;
    
    -- Creditar na conta do Fábio
    UPDATE conta SET saldo = saldo + 100 WHERE nro_conta = 4;

    -- Ops, Não era pro Fábio, e sim pra Bruna
    ROLLBACK TO devitoEmConta;
    UPDATE conta SET saldo = saldo + 100 WHERE nro_conta = 5;
COMMIT;
```