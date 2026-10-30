# TCP/IP
O ***modelo TCP/IP*** (Transmission Control Protocol/Internet Protocol) é o modelo de **arquitetura real utilizado na Internet**.
Possui **4 camadas** e leva esse nome pela relevância dos dois protocolos mais importantes da arquitetura, que são o **TCP** e o **IP**
- É um modelo prático, baseado em protocolos reais com TCP, IP, HTTP, FTP, SMTP, DNS, entre outros. 
- Ele é mais simplificado e direto que o modelo OSI.

## Fluxo
```
Aplicação -> Transporte -> Rede -> Física
Aplicação <- Transporte <- Rede <- Física
```

## Camadas

### 4 - Aplicação
Mais alto nível, comunicação entre programas, como <u>HTTP</u>, <u>FTP</u>, <u>SMTP</u>, <u>POP</u>, <u>DNS</u>...

### 3 - Transporte
Garante que os pacotes não se percam no caminho.
- <u>**TCP**</u> (Entrega confiável)
- <u>**UDP**</u> (Entrega não confiável)

### 2 - Rede/Internet
É responsável pelo **endereçamento** e **roteamento** dos pacotes de dados entre os dispositivos na rede.
- <u>**IP**</u> - Endereço na rede
- <u>**ICMP**</u> - Verifica status da rede

### 1 - Física
Inclui protocos de acesso à rede (meio físico), como <u>**Ethernet**</u> e o <u>**Wi-Fi **</u>

> <u>**Roteador**</u> atua na <u>camada de rede</u>
> <u>**Switch**</u> atua na <u>camada de enlace</u>
> <u>**Hub**</u> atua na <u>camada física</u>