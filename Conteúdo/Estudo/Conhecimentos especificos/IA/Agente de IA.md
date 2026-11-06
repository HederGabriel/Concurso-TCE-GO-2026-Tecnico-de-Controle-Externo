# Agentes de IA

Sistemas de inteligência artificial capazes de **perceber o ambiente, raciocinar, tomar decisões e executar ações** para alcançar determinados objetivos.

Podem utilizar ferramentas, APIs e bancos de dados para interagir com ambientes externos.

**Características:**
- Autonomia na execução de tarefas.
- Tomada de decisões orientada a objetivos.
- Capacidade de planejamento e execução de ações.
- Interação com o ambiente por meio de ferramentas.

**Observação:** nem todo agente utiliza LLM. Modelos de linguagem são utilizados principalmente em agentes modernos.

---

## **Diferença entre Agentes x Chatbots**

**Chatbot:** sistema focado na interação conversacional, respondendo a perguntas e solicitações dos usuários.

**Agente de IA:** sistema capaz de perceber informações, raciocinar, planejar e executar ações para alcançar objetivos.

| Chatbot | Agente de IA |
|---|---|
| Focado na conversação | Focado na execução de objetivos |
| Geralmente fornece respostas | Pode executar ações |
| Autonomia geralmente limitada | Pode possuir maior autonomia |
| Interação principalmente conversacional | Pode interagir com sistemas externos |

**Observação:** um agente pode possuir uma interface de chatbot. As categorias não são excludentes.

---

## **Componentes de um Agente de IA**

- **LLM:** interpreta solicitações, processa informações e auxilia na tomada de decisões.
- **Tools (Ferramentas):** permitem executar ações e interagir com sistemas externos.
- **Memory (Memória):** armazena informações relevantes para manter o contexto.
- **Instructions (Instruções):** definem objetivos, regras e limitações.
- **Environment (Ambiente):** contexto ou sistema com o qual o agente interage.

---

## **Funcionamento (Agent Loop)**

O agente opera por meio de um ciclo de percepção, decisão e ação.

1. **Percepção:** recebe informações do ambiente.
2. **Raciocínio:** interpreta as informações.
3. **Planejamento:** define as ações necessárias.
4. **Ação:** executa as tarefas utilizando ferramentas.
5. **Observação:** analisa os resultados e decide se precisa executar novas ações.

O ciclo pode se repetir até atingir o objetivo ou uma condição de parada.

---

## **Tipos de Agentes**

Na teoria clássica de Inteligência Artificial, os agentes podem ser classificados em:

- **Agente reflexo simples:** toma decisões com base na percepção atual, utilizando regras predefinidas.
- **Agente reflexo baseado em modelo:** considera também um modelo interno do ambiente.
- **Agente baseado em objetivos:** seleciona ações considerando os objetivos que deseja alcançar.
- **Agente baseado em utilidade:** escolhe ações buscando maximizar uma medida de utilidade ou benefício.
- **Agente de aprendizagem:** melhora seu desempenho por meio da experiência.

**Observação:** agentes baseados em objetivos e em utilidade consideram resultados futuros, diferentemente dos agentes reflexos simples.

---

## **Single-Agent x Multi-Agent**

- **Single-Agent:** um único agente executa as tarefas para alcançar o objetivo.
- **Multi-Agent:** múltiplos agentes trabalham em conjunto, podendo dividir responsabilidades e compartilhar informações.

---

## **Agentes de IA x Automação Tradicional**

| Automação tradicional | Agentes de IA |
|---|---|
| Segue regras e etapas predefinidas | Pode decidir dinamicamente quais ações executar |
| Fluxo geralmente determinístico | Comportamento geralmente mais flexível |
| Menor capacidade de adaptação | Pode adaptar suas ações conforme os resultados |

**Observação:** agentes também podem ser integrados a fluxos de automação tradicionais.

---

## **RAG x Agentes de IA**

- **RAG:** recupera informações externas para enriquecer o contexto de um LLM.
- **Agentes:** planejam e executam ações para alcançar objetivos.

**Observação:** um agente pode utilizar RAG como ferramenta para recuperar informações antes de tomar decisões.

---

## **Autonomia e Segurança**

A autonomia de um agente deve ser controlada por mecanismos de segurança.

- **Guardrails:** regras e restrições que limitam o comportamento do agente.
- **Human-in-the-loop:** participação humana na supervisão ou aprovação de decisões.
- **Controle de acesso:** limita as ferramentas e informações disponíveis ao agente.

---

## **Observações importantes para concursos**

- Agentes são orientados a objetivos, não apenas à conversação.
- Podem perceber, raciocinar, planejar e executar ações.
- Tools permitem a interação com sistemas externos.
- Memory permite armazenar e recuperar informações.
- O Agent Loop envolve percepção, decisão, ação e observação.
- Agentes podem trabalhar individualmente ou em sistemas multiagentes.
- A autonomia não significa ausência de supervisão humana.
- Nem todo agente utiliza LLM.
- RAG e agentes são conceitos diferentes, mas podem ser utilizados em conjunto.
- Na teoria clássica, existem agentes reflexos, baseados em modelos, objetivos, utilidade e aprendizagem.