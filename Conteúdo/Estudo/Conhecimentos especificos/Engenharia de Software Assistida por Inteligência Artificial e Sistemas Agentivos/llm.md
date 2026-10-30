# LLM - Large Language Models
Um LLM é uma função matemática que, a partir de um texto, atribui **probabilidades** para prever qual palavra deve vir a seguir, permitindo completar diálogos e criar interações naturais.

## Pré-Treinamento
Os modelos aprendem processando quantidades massivas de dados da internet. O comportamento do modelo é definido por bilhões de parâmetros (ou pesos), que começam aleatórios e são refinados via **backpropagation** (retro-propagação).

## Processos de Refinamento
etapa de aprendizado por reforço com feedback humano (RLHF), essencial para tornar os chatbots assistentes úteis e preferidos pelos usuários

## Arquitetura Transformer
revolucionou a área ao processar texto em paralelo, utilizando o mecanismo de atenção para entender o contexto e significados das  é a arquitetura que permite aos modelos de IA entenderem textos complexos rapidamente.

- **Processamento Paralelo**: Diferente de modelos antigos que liam palavra por palavra, o Transformer **"lê" o texto inteiro** de uma vez.
- **Codificação** (Embeddings): **Transforma palavras em listas de números** para que o computador as processe.
- **Mecanismo de Atenção**: É o coração do sistema; ele faz com que as palavras "conversem" entre si para entender o contexto real (ex: **distinguir "banco" de praça de "banco" de dinheiro**).
- **Redes Feedforward**: Camadas extras que refinam o aprendizado de padrões de linguagem (5:39-5:47).