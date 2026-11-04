# OpenID Connect (OIDC)

Camada de identidade construída sobre o **OAuth 2.0**, utilizada para autenticar usuários e fornecer informações sobre sua identidade.

- **Função:** autenticação de usuários.
- **Base:** OAuth 2.0.
- **Identificação:** utiliza o ID Token.

> OAuth 2.0 autoriza o acesso a recursos; OpenID Connect permite verificar a identidade do usuário.

## ID Token (Token de Identidade)

Token utilizado para **comunicar informações sobre a identidade do usuário autenticado**.

- Formato: JWT.
- Identifica o usuário autenticado.
- Contém informações como identificador (`sub`), emissor (`iss`) e destinatário (`aud`).

> Responde à pergunta: Quem é você?

## Endpoints

Pontos de comunicação disponibilizados pelo servidor OpenID Connect.

- **Authorization Endpoint:** inicia o processo de autenticação e autorização.
- **Token Endpoint:** emite tokens após a validação da solicitação.
- **UserInfo Endpoint:** fornece informações adicionais sobre o usuário autenticado.
- **Logout Endpoint:** permite iniciar o encerramento da sessão, quando disponibilizado pelo provedor.

## Fluxos (Flows)

### Authentication Flow

Fluxo utilizado para autenticar o usuário e obter seu ID Token.

- Realiza a autenticação do usuário.
- Retorna um ID Token.
- Não exige necessariamente um Access Token.

### Hybrid Flow

Combina características dos fluxos Authorization Code e Implicit.

- Realiza a autenticação do usuário.
- Pode retornar um ID Token e um Access Token diretamente pelo Authorization Endpoint.
- Também pode retornar um Authorization Code para obtenção de tokens adicionais.

> Permite combinar autenticação e autorização em um mesmo fluxo.