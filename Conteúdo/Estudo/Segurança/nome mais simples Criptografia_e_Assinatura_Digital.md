# Criptografia Simétrica e Assimétrica, Certificados Digitais e Assinaturas Digitais

## 1. Criptografia

A criptografia transforma informações legíveis em dados protegidos, dificultando o acesso por pessoas não autorizadas.

Seus principais objetivos incluem proteger a confidencialidade das informações e, quando combinada com mecanismos apropriados, contribuir para a integridade e a autenticidade.

## 2. Criptografia Simétrica

Utiliza **a mesma chave secreta para cifrar e decifrar** uma mensagem.

### Funcionamento
1. O emissor cifra a mensagem usando uma chave secreta.
2. O destinatário utiliza a mesma chave para decifrar a mensagem.
3. A chave precisa ser compartilhada de maneira segura entre as partes.

### Vantagens
- Geralmente, é rápida e eficiente.
- É adequada para proteger grandes volumes de dados.

### Desvantagens
- Exige compartilhamento seguro da chave.
- Se a chave secreta for comprometida, as informações protegidas por ela poderão ficar expostas.

### Exemplo
- AES (*Advanced Encryption Standard*).

**Para memorizar:** criptografia simétrica = mesma chave.

## 3. Criptografia Assimétrica

Utiliza um par de chaves relacionadas matematicamente: **chave pública e chave privada**.

### Chave pública
- Pode ser compartilhada com outras pessoas.
- Pode ser usada para cifrar mensagens destinadas ao titular da chave privada.
- Pode ser usada para verificar assinaturas digitais.

### Chave privada
- Deve permanecer secreta.
- Pode ser usada para decifrar mensagens destinadas ao titular, conforme o esquema utilizado.
- Pode ser usada para gerar assinaturas digitais.

### Funcionamento para confidencialidade
1. O emissor utiliza a chave pública do destinatário para cifrar a mensagem.
2. O destinatário utiliza sua chave privada correspondente para decifrá-la.

### Funcionamento para assinatura digital
1. O signatário utiliza sua chave privada para gerar uma assinatura.
2. O destinatário utiliza a chave pública correspondente para verificar a assinatura.

### Características
- Resolve o problema de distribuir uma chave secreta compartilhada para cada comunicação.
- Geralmente, é mais custosa computacionalmente que a criptografia simétrica.
- Pode ser combinada com a criptografia simétrica em sistemas híbridos.

### Exemplo
- RSA, que pode ser empregado em esquemas de cifragem e de assinatura digital.

**Para memorizar:** criptografia assimétrica = par de chaves.

## 4. Certificados Digitais

Um certificado digital é um documento eletrônico que **associa a identidade de um titular à sua chave pública**.

Essa associação é atestada por uma autoridade certificadora, cuja assinatura digital permite verificar a autenticidade do certificado.

### Informações comuns em um certificado
- Identificação do titular.
- Chave pública do titular.
- Período de validade.
- Identificação da autoridade certificadora.
- Assinatura digital da autoridade certificadora.

### Finalidade
Permitir que terceiros verifiquem a associação entre uma identidade e uma chave pública, desde que confiem na cadeia de certificação e que o certificado seja válido para o uso pretendido.

### Atenção
- O certificado contém a chave pública, não a chave privada do titular.
- A chave privada deve permanecer secreta.
- A existência de um certificado não dispensa a verificação de sua validade, cadeia de certificação e situação de revogação.

**Para memorizar:** certificado digital = identidade associada à chave pública.

## 5. Assinaturas Digitais

A assinatura digital é um mecanismo criptográfico que utiliza a criptografia assimétrica e normalmente funções de resumo criptográfico (*hash*).

Permite verificar a integridade do conteúdo assinado e a autenticidade da assinatura em relação à chave pública correspondente.

### Funcionamento simplificado
1. O sistema calcula um resumo criptográfico (*hash*) do documento.
2. O signatário utiliza sua chave privada para gerar a assinatura conforme o algoritmo adotado.
3. O destinatário utiliza a chave pública correspondente para verificar a assinatura.
4. Se o documento for alterado, a verificação deverá detectar a alteração em um esquema seguro e corretamente implementado.

### Propriedades

**Integridade:** permite detectar alterações no conteúdo assinado.

**Autenticidade:** permite verificar se a assinatura corresponde à chave privada associada à chave pública utilizada na verificação.

**Não repúdio:** pode fornecer evidências que dificultem a negação de uma assinatura, mas depende do controle da chave privada, dos procedimentos de identificação e do contexto jurídico.

### O que a assinatura digital não garante sozinha?
**Confidencialidade.** A assinatura digital não impede, por si só, que outras pessoas leiam o conteúdo da mensagem.

Para manter o conteúdo secreto, é necessário utilizar um mecanismo de proteção de confidencialidade, como a criptografia.

**Para memorizar:** assinatura digital = integridade + autenticidade; não garante confidencialidade por si só.

## 6. Comparação entre os conceitos

| Conceito                 | Característica principal                      |
| ------------------------ | --------------------------------------------- |
| Criptografia simétrica   | Mesma chave para cifrar e decifrar            |
| Criptografia assimétrica | Par de chaves: pública e privada              |
| Certificado digital      | Associa uma identidade a uma chave pública    |
| Assinatura digital       | Permite verificar integridade e autenticidade |

## 7. Confidencialidade, Integridade e Autenticidade

| Propriedade       | Significado                                                 |
| ----------------- | ----------------------------------------------------------- |
| Confidencialidade | Impedir que pessoas não autorizadas leiam a informação      |
| Integridade       | Detectar alterações indevidas na informação                 |
| Autenticidade     | Verificar a origem ou a identidade associada a uma operação |

## 8. Pegadinhas de Concurso

- A criptografia simétrica utiliza a mesma chave para cifrar e decifrar.
- A criptografia assimétrica utiliza um par de chaves relacionadas.
- Para cifrar uma mensagem destinada a alguém, pode-se utilizar a chave pública do destinatário; a chave privada correspondente é utilizada para decifrá-la nos esquemas apropriados.
- Para verificar uma assinatura digital, utiliza-se a chave pública correspondente à chave privada do signatário.
- Certificados digitais associam identidades a chaves públicas, não divulgam chaves privadas.
- Assinaturas digitais não garantem confidencialidade por si sós.
- Cifrar uma mensagem e assinar uma mensagem são operações com objetivos diferentes.
- Criptografia, isoladamente, não garante todas as propriedades de segurança: é necessário considerar o algoritmo, o modo de operação e os mecanismos empregados.

## 9. Resumo para Revisão

- **Simétrica:** mesma chave.
- **Assimétrica:** chave pública + chave privada.
- **Certificado digital:** identidade + chave pública.
- **Assinatura digital:** integridade + autenticidade.
- **Confidencialidade:** exige proteção específica; uma assinatura digital, sozinha, não a garante.

## 10. Questões para Revisar

1. Qual é a principal diferença entre criptografia simétrica e assimétrica?
2. Por que o compartilhamento da chave é um desafio na criptografia simétrica?
3. Qual é a função de um certificado digital?
4. Qual chave é utilizada para gerar uma assinatura digital?
5. Qual chave é utilizada para verificar uma assinatura digital?
6. Por que uma assinatura digital não garante confidencialidade?
7. Qual é a diferença entre integridade, autenticidade e confidencialidade?