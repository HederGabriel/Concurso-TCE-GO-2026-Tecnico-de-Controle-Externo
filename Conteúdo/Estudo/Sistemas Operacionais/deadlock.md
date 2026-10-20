# Deadlock (Impasse) — Revisão Rápida

## 1. O que é deadlock?

**Deadlock** é uma situação em que dois ou mais processos ficam bloqueados indefinidamente, esperando por recursos que estão sendo mantidos uns pelos outros.

### Exemplo

- **Processo A:** possui o recurso 1 e espera pelo recurso 2.
- **Processo B:** possui o recurso 2 e espera pelo recurso 1.

Nenhum dos processos consegue continuar, pois cada um aguarda um recurso mantido pelo outro.

## 2. As 4 condições do deadlock

Para ocorrer um deadlock, as quatro condições clássicas devem coexistir:

1. **Exclusão mútua:** um recurso só pode ser utilizado por um processo de cada vez.
2. **Posse e espera:** um processo mantém recursos enquanto espera por outros.
3. **Não preempção:** os recursos não podem ser retirados à força do processo; devem ser liberados por ele.
4. **Espera circular:** existe um ciclo de processos esperando por recursos mantidos uns pelos outros.

**Macete:** E-P-N-E — Exclusão mútua, Posse e espera, Não preempção e Espera circular.

## 3. Deadlock × Starvation

| Conceito | Significado |
|---|---|
| **Deadlock (impasse)** | Processos ficam presos em uma dependência circular. |
| **Starvation (inanição)** | Um processo espera indefinidamente por recursos ou pela CPU, enquanto outros continuam executando. |

**Para concurso:** no deadlock, os processos envolvidos ficam bloqueados pela dependência entre recursos. Na starvation, um processo pode continuar esperando enquanto os demais progridem.