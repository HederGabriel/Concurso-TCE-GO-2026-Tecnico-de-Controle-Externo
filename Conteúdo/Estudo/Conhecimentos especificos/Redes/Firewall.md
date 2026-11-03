# Firewall

Recurso de segurança utilizado para **monitorar e controlar o tráfego de rede**, permitindo ou bloqueando conexões de acordo com regras de segurança predefinidas.

- **Implementação:** Software ou hardware.
- **Função:** filtrar pacotes e controlar o tráfego de entrada e saída.

> Atua como uma barreira de proteção entre redes ou dispositivos, impedindo comunicações não autorizadas.

## Stateless Firewall

Firewall que analisa cada pacote individualmente, **sem armazenar informações sobre conexões anteriores**.

- Não mantém o estado das conexões.
- Não possui contexto sobre pacotes anteriores.
- Analisa principalmente endereços IP, portas e protocolos.
- Menor consumo de recursos em comparação ao Stateful.

## Stateful Firewall

Firewall que **mantém informações sobre o estado das conexões**, analisando os pacotes considerando o contexto da comunicação.

- Armazena informações sobre as conexões.
- É sensível ao contexto.
- Identifica se os pacotes pertencem a conexões legítimas.
- Maior capacidade de análise em comparação ao Stateless.

> Pode bloquear pacotes que não correspondam a conexões previamente estabelecidas ou permitidas.