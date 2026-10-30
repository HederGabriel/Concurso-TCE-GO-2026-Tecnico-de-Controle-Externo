# Projeção - π
Produz uma nova relação (tabela) contendo um subconjunto de conlunas da relação argumento, sem duplicações

## Sintaxe
π lista_atributos (tabela)

## Ex:
> Liste os números e nomes de todos os clientes

`π nro_cli, nome_cli (cliente)`

Saída:
| nro_cli | nome_cli |
| ------- | -------- |
| 1       | Márcia   |
| 2       | Cristina |
| 3       | Manoel   |
| 4       | Rodrigo  |

> Liste o número e o nome dos clientes que possuem saldo inferior a R$200,00 e que morem na Rua X

1. Seleção <br>
`σ saldo < 200 ∧ end_cli = "Rua X" (cliente)`

2. Projeção <br>
`π nro_cli, nome_cli (primeiro passo)`

3. Resultado <br>
`π nro_cli, nome_cli(σ saldo <200 ∧ end_cli = "Rua X"(cliente))`

4. Resultado (Atribuição) <br>
`temp <-- σ saldo < 200 ∧ end_cli = "Rua X" (cliente) ` <br>
`π nro_cli, nome_cli (temp)`

Saída:
| nro_cli | nome_cli |
| ------- | -------- |
| 1       | Márcia   |
| 4       | Rodrigo  |