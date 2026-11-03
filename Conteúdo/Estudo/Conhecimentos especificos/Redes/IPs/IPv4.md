# IPv4 - Internet Protocol Version 4

Protocolo responsável pelo **endereçamento e encaminhamento de pacotes** entre dispositivos em uma rede.

- **Tamanho:** 32 bits.
- **Formato:** 4 octetos de 8 bits.
- **Base:** Decimal (0 a 255 por octeto).
- **Separador:** ponto (`.`).
- **Exemplo:** `192.168.1.10`.
- **Quantidade:** aproximadamente 4,3 bilhões de endereços.

## Formação de um IPv4

Um endereço IPv4 é formado por **32 bits**, divididos em 4 octetos (8 bits cada).

Exemplo:

| Octeto | Binário | Decimal |
|---|---|---|
| 1º | 11000000 | 192 |
| 2º | 10101000 | 168 |
| 3º | 00000001 | 1 |
| 4º | 00001010 | 10 |

**Representação:**

- Binário: `11000000.10101000.00000001.00001010`
- Decimal: `192.168.1.10`

### Conversão Binário → Decimal

Cada bit representa uma potência de 2:

| Bit | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
|---|---|---|---|---|---|---|---|---|

Exemplo: `11000000`

128 + 64 = **192**

## Estrutura de um IPv4

Um endereço IPv4 possui duas partes:

- **Network ID:** identifica a rede.
- **Host ID:** identifica o dispositivo dentro da rede.

A divisão é determinada pela **máscara de sub-rede (Subnet Mask)** ou pelo prefixo CIDR.

### Máscara de Sub-rede

Define quais bits pertencem à rede e quais pertencem aos hosts.

Exemplo:

- IP: `192.168.1.10`
- Máscara: `255.255.255.0`
- CIDR: `/24`

Nesse caso:
- 24 bits identificam a rede.
- 8 bits identificam os hosts.

## Cálculos IPv4

### Quantidade de Endereços

Fórmula:

**2ⁿ**

Onde `n` representa a quantidade de bits disponíveis.

Exemplo:
- IPv4 possui 32 bits.
- 2³² = 4.294.967.296 endereços.

### Quantidade de Hosts

Fórmula:

**2ʰ - 2**

Onde `h` representa a quantidade de bits disponíveis para hosts.

Subtraímos 2 porque, em uma sub-rede IPv4 convencional:
- Um endereço identifica a rede.
- Um endereço é reservado para broadcast.

Exemplo: `/24`

- 32 - 24 = 8 bits para hosts.
- 2⁸ - 2 = **254 hosts utilizáveis**.

### Sub-redes (Subnetting)

Técnica utilizada para dividir uma rede maior em redes menores.

Exemplo:

`192.168.1.0/24`

Dividindo em `/26`:

- 32 - 26 = 6 bits para hosts.
- 2⁶ = 64 endereços por sub-rede.
- 2⁶ - 2 = 62 hosts utilizáveis por sub-rede.
- São formadas 4 sub-redes.

## Migração para IPv6

Devido ao esgotamento dos endereços IPv4, surgiu a necessidade de migrar gradualmente para o IPv6.

> Os dois protocolos continuam coexistindo.