# Servelees (Sem Servidor)
Modelo de computação em nuvem que permite aos desenvolvedores criar e executar aplicativos e serviços sem se preucupar com o gerenciamento da infraestrutura subjacente.

## Características
### **Abstração de servidores:**
- O provedor de nuvem **gerencia automaticamente a infraestrutura**, incluindo servidores, SO e [escalabilidade](escalabilidade.md).
- Os DEVs se concentram apenas no código e na lógica do aplicativo.

### [**Escalabilidade automática:**](escalabilidade.md) 
- A insfraestrutura é gerenciada automaticamente para atender à demanda.

### **Pagamento por uso:**
- Os usuários pagam apenas pelos recursos computacionais que consomem.
- Isso pode resultar em economias de custos significativos para aplicativos com padrões de uso variáveis.

### **Eventos:**
- A computação serveless é geralmente orientada a eventos, o que significa que as funcões são executadas em resposta a eventos específicos (como uploads de arquivos, solicitações HTTP ou mensagens de fila).

## Benefícios
### **Redução da complexidade operacional:**
- Os DEVs **não precisam se preocupar com o gerenciamento de servidores**.

### **Maior agilidade:**
- [**Escalabidade automática**](escalabilidade.md) e o [**modelo de pagamento por uso**](#pagamento-por-uso) permitem que os DEVs implantem e dimensionem aplicativos rapidamente.

### **Redução de Custos:**
- O [**modelo de pagamento por uso**](#pagamento-por-uso) pode gerar uma economia de custos significativa

### **Escalabilidade Simplificada:**
- Sem preucupações com escalabilidade manual

## Casos de Uso comuns
- APIs e microsserviços
- Processamento de dados em tempo real
- Aplicativos da web e móveis
- Automação de tarefas
- Inteligência Artificial e aprendizado de máquina

## Ferramentas

1. AWS Lambda (Amazon Web Services)
   - É um serviço de computação serveless que permite **executar código sem provisionar ou gerenciar servidores**.
   - **Suporta várias linguagens de programação**, como Python, Java, Node.js e Go.
   - É ideal para criar microsserviços, processar dados em tempo real e automatizar tarefas.

2. Azure Functions (Microsoft Azure)
   - É um serviço de computação serveless semelhante ao AWS Lambda.
   - Permite **executar código em resposta a eventos**, como solicitações HTTP, mensagens de fila e alterações de banco de dados.
   - **Suporta várias linguagens de programaçãom**, incluindo C#, Java, Python e JavaScript.

3. Google Cloud Functions (Google Cloud Platform)
   - É um serviço de coputação serveless que permite criar funções que r**espondem a eventos do Google Cloud Platform**.
   - Suporta Node.js, Python, Go e outras linguagens.
   - É útil para criar APIs, processar dados e automatizar tarefas

4. Cloudflare Workers (Cloudflare)
   - É uma plataforma de computação serveless que permite **executar código na borda da rede Cloudflare**.
   - É ideal para criar aplicativos de **baixa latência e distribuir conteúdo globalmente**.
   - Suporta **JavaScript e WebAssembly**.

5. Backend as a Service (BaaS)
   - Serviços que fornecem funcionalidades de **backend pré-construídas**, como bancos de dados, autenticação e armazenamento de arquivos.
   - Exemplos incluem **Firebase**, **AWS Amplify** e **Supabase**
   - Simplificam o desenvolvimento de aplicativos móveis e da WEB.

6. Ferramentas de Orquestração
   - Ferramentas como Serveless Framework e AWS SAM (Serveless Application Model) facilitam a implantação e o gerenciamento de aplicativos serveless.
   - Permitem definir a infraestrutura como código e automatizar o processo de implantação.