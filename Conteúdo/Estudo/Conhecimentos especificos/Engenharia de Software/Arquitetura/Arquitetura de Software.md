# Arquitetura de Software
De forma geral, ela define o comportamento e as características de uma aplicação
Arquitetura de Software não consiste em encontrar a estrutura perfeita, mas em tomar **decisões conscientes** diante de requisitos conflitantes.

> Tudo na arquitetura de software é um trade-off
>
> O "porque" é mais importante que o "como" 

## Características de um Sistema
- **Funcionais:** o que o sistema deve fazer, como funcionalidades e regras de negócio. 
- **Não funcionais:** como o sistema deve funcionar, considerando características como performance, segurança, confiabilidade e escalabilidade.

> Essas características influenciam diretamente as decisões de arquitetura.

## Constrains - Restrições
O que pode ou não pode ser feito em um sistema, e de que forma.

## Decisões e Trade-offs
Trade-off =  Decisão equilibrada, entre o que nós precisamos fazer com alguma tecnologia ou ferramenta, e o que ela pode fazer trazer de não tão bom.
> EX: Uma ferramenta **resolve** um problema de escalabilidade no sofware, **mas** ela tem um custo muito alto.
> **Qual é o trade-off?** Os custos para implementar essa ferramenta.

## Princípios de Design
- **Modularidade:** dividir o sistema em partes com responsabilidades bem definidas.
- **Baixo acoplamento:** reduzir as dependências entre os componentes.
- **Alta coesão:** manter relacionadas as responsabilidades de cada componente.
- **Abstração:** destacar o essencial e esconder detalhes desnecessários.
- **Simplicidade:** evitar complexidade desnecessária na solução.
- **Separação de responsabilidades:** organizar cada parte do sistema de acordo com sua função.

## O que é o Traballho?
Tomar todas as decisões de arquitetura, para um time ou vários times. ou um produto, ou uma empresa
- Bastante Conhecimento Técnico
- Conhecimento sólido sobre o negócio

### Quais são todas as decisões de arquitetura?
> Visão Macro (mais global)
- Como os dados vão ser armazenados
- Como o sistema vai se comunicar
- Como o sistema vai se estruturar
- Qual técnologia usar para resolver um problema
> Não existe uma bala de prata (Solução que serve para qualquer coisa) na arquitetura de software
> Leva-se em consideração muita coisa como:
- Situação Atual do Software
- Necessidades técnicas do *momento*
- Mudanças

### Análise de Trade-offs
Análisar todos os trade-off e ver se são realmente a melhor solução

### Times
*Garantir* que os times estejam seguindos as decisões de arquitetura e design, durante o desenvolvimento

## Padrões de Arquiteturas
- Arquitetura em camadas
- Arquitetura baseada em evento (***monólito***)
- Arquitetura Serveless
- Arquitetura baseada em nuvem
- Arquitetura de Micro-serviços
...

## TRADE-OFF (Características)
- Performance
- Usabilidade
- Confiabilidade
- Segurança
- Manutenabilidade
- Escalabilidade
...
