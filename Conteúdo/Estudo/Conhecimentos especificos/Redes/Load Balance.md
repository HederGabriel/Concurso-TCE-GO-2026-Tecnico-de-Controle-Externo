# Load Balancing - Balanceamento de Carga

Técnica utilizada para **distribuir requisições e cargas de trabalho entre vários servidores**, evitando a sobrecarga de apenas um servidor.

- **Função:** distribuir o tráfego entre múltiplos servidores.
- **Objetivo:** melhorar o desempenho, a disponibilidade e a escalabilidade.

> Evita que um único servidor fique sobrecarregado, distribuindo as solicitações entre vários servidores.

## Funcionamento

1. O cliente realiza uma solicitação.
2. O Load Balancer recebe a requisição.
3. Analisa os servidores disponíveis.
4. Encaminha a requisição para um dos servidores.
5. O servidor processa a solicitação e retorna a resposta.

## Algoritmos de Balanceamento

- **Round Robin:** distribui as requisições sequencialmente entre os servidores.
- **Least Connections:** encaminha a requisição para o servidor com menos conexões ativas.
- **IP Hash:** utiliza o endereço IP do cliente para determinar o servidor de destino.
- **Weighted Round Robin:** distribui as requisições considerando pesos definidos para cada servidor.

## Benefícios

- **Alta disponibilidade:** mantém o serviço disponível mesmo quando um servidor falha, desde que existam outros servidores saudáveis.
- **Escalabilidade:** permite adicionar novos servidores conforme a demanda aumenta.
- **Desempenho:** distribui o processamento entre vários servidores.
- **Tolerância a falhas:** pode redirecionar requisições quando um servidor fica indisponível.