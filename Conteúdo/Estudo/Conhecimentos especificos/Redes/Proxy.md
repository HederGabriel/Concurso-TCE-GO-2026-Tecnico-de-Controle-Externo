# Proxy - Servidor Proxy

Servidor intermediário que atua entre um cliente e outro servidor, **recebendo e encaminhando solicitações em nome do cliente**.

- **Função:** intermediar comunicações entre clientes e servidores.
- **Utilização:** controle de acesso, filtragem de conteúdo, anonimização e cache.

> Atua como intermediário entre o usuário e a Internet, podendo controlar e monitorar as solicitações realizadas.

## Tipos de Proxy

### Forward Proxy (Proxy Direto)

Atua em nome do cliente, intermediando suas solicitações para servidores externos.

- Oculta o endereço IP do cliente perante o servidor de destino.
- Pode controlar o acesso à Internet.
- Pode filtrar sites e conteúdos.
- Pode armazenar respostas em cache.

### Reverse Proxy (Proxy Reverso)

Atua em nome dos servidores, recebendo solicitações dos clientes e encaminhando-as aos servidores internos.

- Oculta a infraestrutura dos servidores internos.
- Pode distribuir requisições entre vários servidores (Load Balancing).
- Pode realizar cache.
- Pode auxiliar na segurança e no controle de acesso.