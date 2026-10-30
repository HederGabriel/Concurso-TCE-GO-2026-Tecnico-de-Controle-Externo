# Seleção - σ
Seleciona Tuplas da  relação que satisfaçam a uma ou mais condições

Comparadores:
- =
- <
- >
- <=
- >=
- !=
- ∧ (and)
- v (or)
- ¬ (not)

## Sintaxe
σ condição_seleção (tabela)

### Ex:
| nro_cli | nome_cli | end_cli   | saldo  | cod_vend |
| ------- | -------- | --------- | ------ | -------- |
| 1       | Márcia   | Rua X     | 100,00 | 1        |
| 2       | Cristina | Avenida 1 | 10,00  | 1        |
| 3       | Manoel   | Avenida 3 | 234,00 | 1        |
| 4       | Rodrigo  | Rua X     | 137,00 | 2        |

> Listar toda informação do cliente número 4

`σ nro_cli = 4 (cliente)`

Saída:
| nro_cli | nome_cli | end_cli | saldo  | cod_vend |
| ------- | -------- | ------- | ------ | -------- |
| 4       | Rodrigo  | Rua X   | 137,00 | 2        |

> Liste as informações dos cliente que possuem saldo menor a R$200,00 e que morem na Rua X 

`σ saldo < 200 ∧ end_cli = "Rua X" (cliente)` 

Saída:
| nro_cli | nome_cli | end_cli | saldo  | cod_vend |
| ------- | -------- | ------- | ------ | -------- |
| 1       | Márcia   | Rua X   | 100,00 | 1        |
| 4       | Rodrigo  | Rua X   | 137,00 | 2        |