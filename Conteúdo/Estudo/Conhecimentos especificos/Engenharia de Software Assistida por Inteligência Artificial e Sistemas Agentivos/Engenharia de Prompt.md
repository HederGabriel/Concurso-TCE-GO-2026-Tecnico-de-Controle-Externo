# Engenharia de Prompt

## 1. Persona, Tarefa e Contexto

### Persona
Define o papel ou a especialidade que a LLM deve assumir durante a execução da tarefa.

### Tarefa
Descreve claramente o que a LLM deve fazer, especificando a ação esperada.

### Contexto
Fornece informações relevantes para que a LLM compreenda o cenário, os objetivos e as condições da tarefa.

## 2. One-Shot e Multi-Shot

### One-Shot
Fornece um único exemplo de entrada e saída para orientar o modelo sobre como executar a tarefa.

### Multi-Shot
Fornece múltiplos exemplos de entrada e saída, permitindo que o modelo identifique padrões e siga melhor o formato e o comportamento esperados.

É especialmente útil para tarefas que exigem saídas estruturadas, como JSON, aumentando a consistência das respostas.

## 3. Cadeia de Pensamento (Chain of Thought)

Consiste em orientar a LLM a abordar um problema por etapas, dividindo tarefas complexas em etapas menores e organizadas.

**Exemplo:** Em um e-mail de suporte ao cliente, você pode instruir o modelo a:

1. Identificar a solicitação principal e o tom do cliente.
2. Identificar as informações necessárias para responder.
3. Determinar a ação mais adequada.
4. Verificar a clareza e a coerência da resposta final.

Essa abordagem pode melhorar o desempenho em tarefas que exigem múltiplas etapas de raciocínio. Entretanto, não é necessário solicitar que o modelo exponha todo o seu raciocínio interno: basta solicitar uma justificativa resumida ou os principais passos da solução.