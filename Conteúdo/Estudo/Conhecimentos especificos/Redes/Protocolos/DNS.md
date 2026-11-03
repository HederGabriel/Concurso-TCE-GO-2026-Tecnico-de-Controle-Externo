# DNS - Domain Name System

Sistema responsável por **traduzir nomes de domínio em endereços IP**, permitindo que dispositivos encontrem servidores na rede.

- **Camada:** Aplicação.
- **Porta padrão:** 53 (UDP e TCP).
- **Função:** resolução de nomes de domínio.
- **Exemplo:** `google.com` → endereço IP correspondente.

> Permite acessar sites utilizando nomes de domínio, sem precisar memorizar seus endereços IP.

## Funcionamento do DNS

1. O usuário digita um domínio no navegador (ex.: `google.com`).
2. O dispositivo consulta um servidor DNS.
3. O servidor DNS procura o endereço IP correspondente.
4. O endereço IP é retornado ao dispositivo.
5. O navegador utiliza o IP para estabelecer a comunicação com o servidor.

## Tipos de Registros DNS

- **A:** associa um domínio a um endereço IPv4.
- **AAAA:** associa um domínio a um endereço IPv6.
- **CNAME:** cria um alias (apelido) para outro domínio.
- **MX:** identifica os servidores responsáveis pelo recebimento de e-mails.
- **NS:** identifica os servidores DNS responsáveis por um domínio.
- **TXT:** armazena informações textuais, frequentemente utilizadas para verificações e autenticação.

## Tipos de Consulta DNS

- **Recursiva:** o servidor DNS consultado fica responsável por encontrar a resposta.
- **Iterativa:** o servidor retorna a melhor resposta disponível ou indica outro servidor que pode fornecer a informação.