# Otimização de Consultas

É o conjunto de técnicas utilizadas para melhorar o desempenho das consultas SQL, reduzindo o tempo de execução e o consumo de recursos do banco de dados.

**Principais técnicas:**

- **Índices:** Criam estruturas auxiliares para localizar registros rapidamente, evitando varreduras completas (*Sequential Scan*).
- **Covering Index (Índice de Cobertura):** Índice que contém todas as colunas necessárias para atender a uma consulta, permitindo que o banco recupere os dados diretamente do índice (*Index Only Scan*), sem acessar a tabela original.
- **Índices Compostos:** Criados sobre múltiplas colunas, permitindo otimizar consultas que utilizam vários critérios de filtragem.
- **Otimizador de Consultas:** Analisa diferentes possibilidades e escolhe o plano de execução mais eficiente.

**Covering Index:**

Exemplo de consulta:

```sql
SELECT email
FROM usuarios
WHERE date_of_birth = '2000-01-01';
```

Criação de um índice de cobertura no PostgreSQL:

```sql
CREATE INDEX idx_usuario_nascimento
ON usuarios (date_of_birth)
INCLUDE (email);
```

- `date_of_birth`: Coluna utilizada na filtragem (`WHERE`).
- `email`: Coluna incluída para atender ao `SELECT`.

**Observação:** Índices melhoram a velocidade de leitura, mas ocupam espaço e aumentam o custo de operações de escrita (`INSERT`, `UPDATE` e `DELETE`). Devem ser utilizados conforme o padrão de consultas do sistema.