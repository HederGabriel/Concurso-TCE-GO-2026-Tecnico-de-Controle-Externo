## Alta Disponibilidade - HA (High Availability)

Capacidade de manter sistemas, serviços e aplicações operacionais e acessíveis, mesmo diante de falhas, minimizando o tempo de indisponibilidade (*downtime*).

> HA = manter o serviço disponível mesmo diante de falhas. <br>
> Failover = transferir o serviço. <br>
> Redundância = ter recursos alternativos.

**Principais características:**
- Busca garantir a continuidade dos serviços e reduzir interrupções.
- Utiliza redundância de recursos para evitar pontos únicos de falha (*SPOF — Single Point of Failure*).
- Não elimina falhas, mas permite que o sistema continue funcionando mesmo quando determinados componentes falham.

**Mecanismos de Alta Disponibilidade:**
- **Redundância:** duplicação de componentes, como servidores, redes, switches, bancos de dados, storages e fontes de energia.
- **Clusters:** conjunto de servidores que trabalham em conjunto para manter a disponibilidade de um serviço.
- **Balanceamento de carga (Load Balancing):** distribui as requisições entre diferentes servidores.
- **Monitoramento (Health Checks):** identifica falhas e verifica a disponibilidade dos componentes.
- **Failover:** transfere automaticamente ou manualmente a carga de um componente com falha para outro componente redundante.

**Tipos de Failover:**
- **Ativo-Passivo:** um servidor atende às requisições, enquanto outro permanece em espera para assumir em caso de falha.
- **Ativo-Ativo:** dois ou mais servidores operam simultaneamente, compartilhando a carga de trabalho.

**Níveis de Disponibilidade:**

A disponibilidade é expressa em percentual, indicando a proporção do tempo em que um serviço permanece operacional.

| Disponibilidade | Indisponibilidade máxima anual |
| --------------- | ------------------------------ |
| 99%             | 3,65 dias                      |
| 99,9%           | 8,76 horas                     |
| 99,99%          | 52,56 minutos                  |
| 99,999%         | 5,26 minutos                   |

- **Five Nines (99,999%):** representa um nível de disponibilidade com, aproximadamente, apenas 5 minutos e 15 segundos de indisponibilidade por ano.

**Arquitetura de Alta Disponibilidade:**
- **Multizona (Multi-AZ):** distribui os recursos entre diferentes zonas de disponibilidade dentro da mesma região geográfica.
- **Multirregião (Multi-Region):** distribui os recursos entre diferentes regiões geográficas, aumentando a proteção contra falhas regionais e desastres.

**Atenção para a prova:**
- Alta disponibilidade depende de redundância e mecanismos de recuperação de falhas.
- Redundância não se limita aos servidores: também envolve rede, energia, armazenamento e bancos de dados.
- *Failover* é a transferência do serviço para um componente redundante após uma falha.
- *Auto Scaling* ajusta automaticamente a quantidade de recursos conforme a demanda, mas não é, por si só, um mecanismo de failover.
- Quanto maior o percentual de disponibilidade, menor o tempo permitido de indisponibilidade.