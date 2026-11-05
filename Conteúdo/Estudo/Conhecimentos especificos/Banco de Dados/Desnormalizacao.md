# Desnormalização

É o processo de introduzir redundância em um banco de dados, contrariando algumas regras de normalização, com o objetivo de simplificar consultas, melhorar a flexibilidade ou atender a necessidades específicas.

**Quando utilizar:**

- **Fatores externos:** Quando é necessário integrar dados provenientes de sistemas que já possuem estruturas não normalizadas.
- **Flexibilidade:** Quando mudanças nas regras de negócio podem exigir estruturas mais flexíveis.
- **Performance:** Para reduzir operações de `JOIN` e acelerar consultas, quando outras otimizações não forem suficientes.
- **Data Marts:** Em bancos voltados para consultas analíticas e leitura (*read-only*), facilitando o acesso aos dados.

**Desvantagens:**
- Maior redundância de dados.
- Risco de inconsistências.
- Maior complexidade nas operações de atualização.

**Observação:** Antes de desnormalizar, deve-se priorizar otimizações na camada de processamento, como índices e particionamento, preservando a integridade lógica do banco de dados.