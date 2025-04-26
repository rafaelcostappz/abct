
# Política de Gerenciamento de Tokens e Credenciais - AbacatePay SDKs

> Esta política define as diretrizes para o uso, armazenamento e proteção de **tokens**, **chaves de API**, **secrets** e demais credenciais sensíveis nos repositórios **open source** da AbacatePay.

Manter a segurança dessas informações é essencial para proteger nossa infraestrutura, nossos usuários e a integridade dos SDKs.

---

## Proibições

- **Nunca** commitar tokens, chaves de API, senhas ou qualquer credencial sensível em repositórios, mesmo que privados.
- É estritamente proibido:
  - Hardcode de secrets no código-fonte.
  - Exposição de tokens em logs, mensagens de commit ou issues.
  - Compartilhamento de tokens em canais públicos ou não seguros.

---

## Boas Práticas de Gestão de Tokens

1. **Uso de Variáveis de Ambiente (`.env`)**
   - Armazene credenciais localmente em arquivos `.env` e adicione-os ao `.gitignore`.

2. **GitHub Secrets**
   - Utilize o recurso de **[GitHub Secrets](https://docs.github.com/pt/actions/security-guides/encrypted-secrets)** para armazenar tokens em workflows de CI/CD.

3. **Rotação de Tokens**
   - Realize a troca periódica de tokens e chaves de API conforme as políticas internas.

4. **Criptografia**
   - Quando necessário armazenar informações sensíveis, utilize métodos de criptografia adequados.

5. **Acesso Mínimo**
   - Siga o princípio de **least privilege**: conceda apenas as permissões estritamente necessárias para cada token.

---

## Ferramentas de Suporte

- **GitHub Secret Scanning**
  - Está habilitado para detectar automaticamente vazamentos de secrets em pushs.
  - Caso detectado, ações imediatas devem ser tomadas.

- **Dependabot Secrets**
  - Mantenha suas dependências seguras e integre variáveis sensíveis de forma segura nos pipelines.

- **Ferramentas Recomendadas**:
  - [Doppler](https://www.doppler.com/)
  - [HashiCorp Vault](https://www.vaultproject.io/)
  - [GitGuardian](https://www.gitguardian.com/)

---

## Procedimentos em Caso de Vazamento

1. **Revogue imediatamente** o token comprometido.
2. Atualize as credenciais e realize a **rotatividade**.
3. Comunique o incidente para o time de segurança:  
   📧 **security@abacatepay.com**
4. Caso o vazamento esteja em histórico Git, siga procedimentos de **git history rewrite**.
5. Registre o incidente conforme os [Procedimentos Internos de Segurança](/maintainers/SECURITY_HANDLING.md).

---

## Referências

- [GitHub Secrets Documentation](https://docs.github.com/pt/actions/security-guides/encrypted-secrets)
- [GitHub Secret Scanning](https://docs.github.com/pt/code-security/secret-scanning)
- [Política de Segurança da AbacatePay](/policies/SECURITY_POLICY.md)
- [Procedimentos Internos de Segurança](/maintainers/SECURITY_HANDLING.md)

---

> A segurança dos tokens e credenciais é responsabilidade de todos. Pequenas falhas podem gerar grandes riscos — siga esta política rigorosamente.