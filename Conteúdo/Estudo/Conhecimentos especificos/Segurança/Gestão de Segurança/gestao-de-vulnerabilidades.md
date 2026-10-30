# Gestão de Vulnerabilidades
É um processo que envolve identificação, análise e mitigação de qualquer potencial ameaça que pode afetar sistemas, redes ou qualquer ativo de tecnologia
> Prática de encontrar e corrigir falhas de segurança antes que elas possam ser exploradas

## Objetivos
É **reduzir a exposição** da organização a ataques por meio da identificação e do tratamento das vulnerabilidades de forma contínua e baseada em riscos.
> Nem sempre será possível corrigir todas as vulnerabilidades imediatamente.

## Como avaliar e priozir os riscos?
Modelo conceitual simplificado, não uma fórmula universal para calcular o risco de todas as vulnerabilidades.

$$
\text{Risco} \approx
\text{Probabilidade} \times \text{Impacto}
$$

Probabilidade: possibilidade de ocorrer um evento prejudicial. <br>
Impacto: consequências que esse evento pode produzir.

### Comparação
| Recurso                                             | O que informa?                                  | Para que serve?                            |
| --------------------------------------------------- | ----------------------------------------------- | ------------------------------------------ |
| [CVE](#cve---common-vulnerabilities-and-exposures)  | Identificador de uma vulnerabilidade conhecida  | Referenciar e acompanhar a falha           |
| [CVSS](#cvss---common-vulnerability-scoring-system) | Gravidade técnica                               | Avaliar a severidade                       |
| [EPSS](#epss--exploit-prediction-scoring-system)    | Probabilidade estimada de exploração em 30 dias | Apoiar a priorização                       |
| [KEV](#kev--known-exploited-vulnerabilities)        | Evidência de exploração no mundo real           | Identificar vulnerabilidades já exploradas |

### CVE - Common Vulnerabilities and Exposures
CVE é um sistema de identificação de vulnerabilidades conhecidas publicamente.

Uma vulnerabilidade identificada pode receber um código como: CVE-2024-XXXX

O identificador permite que fabricantes, pesquisadores e equipes de segurança se refiram à mesma vulnerabilidade.

### CVSS - Common Vulnerability Scoring System
CVSS é um sistema utilizado para avaliar e comunicar a gravidade técnica de vulnerabilidades.

- **Base**: características fundamentais da vulnerabilidade.
- **Threat**: informações relacionadas à ameaça, como a situação de exploração.
- **Environmental**: características específicas do ambiente em que a vulnerabilidade existe.
- **Supplemental**: informações adicionais que ajudam a contextualizar a análise.

As pontuações CVSS podem variar de 0,0 a 10,0. A escala qualitativa do CVSS 4.0 é a seguinte: 

| Pontuação  | Classificação |
| ---------- | ------------- |
| 0,0        | Nenhuma       |
| 0,1 a 3,9  | Baixa         |
| 4,0 a 6,9  | Média         |
| 7,0 a 8,9  | Alta          |
| 9,0 a 10,0 | Crítica       |

> Uma vulnerabilidade com CVSS 9,8 é considerada crítica segundo essa escala.
> Entretanto, isso não significa automaticamente que ela seja a vulnerabilidade mais urgente em todos os ambientes.
>
> Por exemplo, uma vulnerabilidade crítica pode afetar um software que a organização nem sequer utiliza. Já uma falha classificada como alta pode estar presente em um serviço exposto que sustenta uma operação essencial.

### EPSS — Exploit Prediction Scoring System
EPSS é um modelo que estima a probabilidade de uma vulnerabilidade identificada por CVE ser explorada no mundo real nos próximos 30 dias.

Sua pontuação varia de 0 a 1. Por exemplo:
- EPSS = 0,05: probabilidade estimada de 5%.
- EPSS = 0,40: probabilidade estimada de 40%.
- EPSS = 0,90: probabilidade estimada de 90%.

> Esses valores representam estimativas para o conjunto de vulnerabilidades avaliadas pelo modelo, não garantias sobre o destino de uma vulnerabilidade individual.

### KEV — Known Exploited Vulnerabilities
O catálogo KEV é mantido pela CISA, agência norte-americana responsável por atividades relacionadas à segurança cibernética e à infraestrutura crítica.

A diferença fundamental é:
- CVSS: avalia a gravidade técnica.
- EPSS: estima a probabilidade de exploração nos próximos 30 dias.
- KEV: registra vulnerabilidades com evidências de exploração no mundo real.
