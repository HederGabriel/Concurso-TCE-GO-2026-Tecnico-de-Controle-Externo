# DHCP - Dynamic Host Configuration Protocol

Protocolo responsável por **atribuir automaticamente configurações de rede** aos dispositivos conectados a uma rede.

- **Camada:** Aplicação.
- **Portas padrão:** 67 (servidor) e 68 (cliente).
- **Função:** atribuição automática de endereços IP e outras configurações de rede.
- **Atribuição:** dinâmica ou estática (reserva).

> Evita a necessidade de configurar manualmente o endereço IP de cada dispositivo.

## Funcionamento do DHCP (DORA)

O processo de atribuição de endereço IP utiliza quatro etapas:

1. **Discover:** o cliente procura servidores DHCP disponíveis na rede.
2. **Offer:** o servidor oferece um endereço IP ao cliente.
3. **Request:** o cliente solicita o endereço oferecido.
4. **Acknowledgment (ACK):** o servidor confirma a atribuição do endereço IP.

## Configurações fornecidas pelo DHCP

- **Endereço IP:** identifica o dispositivo na rede.
- **Máscara de Sub-rede:** identifica a parte da rede e a parte dos hosts.
- **Gateway padrão:** permite a comunicação com outras redes.
- **Servidor DNS:** realiza a resolução de nomes de domínio.