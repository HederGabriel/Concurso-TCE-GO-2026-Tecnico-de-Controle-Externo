# **Padrões de Segurança de API**

## **Gatekeeper Pattern**

Utiliza um componente intermediário para controlar e filtrar as requisições externas antes que cheguem aos serviços internos.

- Reduz a superfície de ataque.
- Centraliza autenticação, autorização e controle de requisições.
- **Exemplos:** API Gateway e BFF (Backend for Frontend).

### **WAF (Web Application Firewall)**

Firewall que inspeciona e bloqueia tráfego HTTP/HTTPS malicioso antes que chegue à aplicação.

- Protege contra SQL Injection, XSS e outros ataques.
- Atua como camada complementar de segurança.
- **Exemplos:** Cloudflare WAF, AWS WAF e Azure WAF.

## **Valet Key Pattern**

Fornece uma chave ou token temporário com permissões restritas para acessar diretamente determinado recurso.

- Limita o acesso por tempo, recurso e permissão.
- **Exemplos:** SAS Token (Azure) e Pre-signed URL (AWS S3).

## **Token Relay Pattern**

Encaminha o token de autenticação do usuário entre serviços, preservando sua identidade e contexto de autorização.

- Permite que diferentes APIs identifiquem o usuário que originou a requisição.
- **Exemplo:** encaminhamento de um Access Token (JWT) entre microsserviços.