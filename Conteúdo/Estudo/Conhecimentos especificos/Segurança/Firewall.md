# Firewall

Conceitos e explicações básicas presentes em: [~Redes\Firewall.md](../Redes/Firewall.md).

## **Tipos de Firewall**

- **Firewall de Rede:** protege redes, controlando o tráfego entre diferentes segmentos ou redes externas.
- **Firewall de Host:** instalado em um dispositivo específico, controla as conexões de entrada e saída daquele equipamento.
- **NGFW (Next-Generation Firewall):** firewall de próxima geração que combina filtragem tradicional com recursos avançados, como inspeção profunda de pacotes (DPI), prevenção de intrusões (IPS) e identificação de aplicações.

## **Mecanismos de Filtragem**

- **Filtragem de Pacotes:** analisa informações como IP de origem e destino, portas e protocolos.
- **DPI (Deep Packet Inspection):** inspeciona o conteúdo dos pacotes, indo além dos cabeçalhos.
- **Regras de Firewall:** definem quais conexões são permitidas ou bloqueadas.
- **Política de Negação Padrão (Default Deny):** bloqueia todo tráfego que não esteja explicitamente autorizado.

## **DMZ (Zona Desmilitarizada)**

Segmento de rede isolado utilizado para hospedar serviços que precisam ser acessíveis externamente, como servidores Web e DNS.

- Separa os serviços públicos da rede interna.
- Reduz a exposição dos sistemas internos.
- Controla a comunicação entre redes externas, DMZ e rede interna.

## **Limitações do Firewall**

- Não impede ataques que não passam por ele.
- Não garante proteção contra ameaças internas.
- Não substitui antivírus, IDS/IPS ou outras medidas de segurança.
- Sua eficácia depende da configuração adequada das regras.