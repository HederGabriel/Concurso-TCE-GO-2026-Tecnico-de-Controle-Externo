# IPv6 - Internet Protocol Version 6

Versão mais recente do protocolo IP, desenvolvida para **ampliar a quantidade de endereços disponíveis** e substituir gradualmente o IPv4.

- **Tamanho:** 128 bits.
- **Formato:** 8 grupos de números hexadecimais.
- **Separador:** dois-pontos (`:`).
- **Exemplo:** `2001:0db8:85a3:0000:0000:8a2e:0370:7334`.
- **Quantidade:** aproximadamente 3,4 × 10³⁸ endereços.

> Possui um espaço de endereçamento muito maior que o IPv4 e suporte nativo a IPsec.

## Migração do IPv4 para IPv6

A migração ocorre gradualmente, pois os dois protocolos não são diretamente compatíveis.

Principais mecanismos de transição:

- **Dual Stack:** dispositivos utilizam IPv4 e IPv6 simultaneamente.
- **Tunneling (Tunelamento):** encapsula pacotes de um protocolo dentro de outro para permitir a comunicação.
- **Translation (Tradução):** converte pacotes entre IPv4 e IPv6.

> O IPv6 foi desenvolvido para substituir gradualmente o IPv4, principalmente devido à limitação de endereços deste último.