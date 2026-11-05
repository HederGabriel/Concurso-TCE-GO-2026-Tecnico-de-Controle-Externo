# Índices

São estruturas auxiliares que permitem localizar registros mais rapidamente, evitando a necessidade de percorrer toda a tabela (*Full Table Scan*).

**Funcionamento:**
- **Sem índice:** O banco realiza uma varredura completa na tabela para encontrar os registros.
- **Com índice:** O banco utiliza uma estrutura organizada para localizar os registros com maior eficiência, semelhante ao índice de um livro.

**Criação:**

Utiliza-se o comando `CREATE INDEX` para criar um índice em uma ou mais colunas.

```sql
CREATE INDEX idx_nome
ON clientes (nome);
```

**Tipos:**
- **Simples:** Criado sobre uma única coluna.
- **Composto:** Criado sobre duas ou mais colunas. A ordem das colunas influencia quais consultas podem aproveitar o índice.

**Otimizador de Consultas:**

O SGBD analisa as consultas e escolhe o melhor plano de execução, utilizando índices quando considerar vantajoso.

**Vantagens:**
- Acelera consultas e pesquisas.
- Melhora operações de filtragem (`WHERE`).
- Otimiza consultas com `JOIN` e ordenações (`ORDER BY`).

**Desvantagens:**
- Ocupa espaço de armazenamento.
- Aumenta o custo de operações `INSERT`, `UPDATE` e `DELETE`, pois os índices também precisam ser atualizados.

**Observação:** Índices devem ser utilizados estrategicamente. Nem toda coluna precisa de um índice, e sua criação deve considerar o padrão de consultas do banco de dados.