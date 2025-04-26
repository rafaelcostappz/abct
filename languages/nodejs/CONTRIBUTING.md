
# Como Contribuir - AbacatePay Node.js SDK

Obrigado por querer contribuir com o **abacatepay-nodejs-sdk**!  
Este projeto segue as diretrizes centralizadas da AbacatePay para garantir qualidade, segurança e consistência em todos os nossos SDKs open source.

> Consulte o [Guia de Contribuição Central](https://github.com/AbacatePay/sdk-standards/blob/main/contributors/CONTRIBUTING.md) para regras gerais.

---

## Especificidades do SDK Node.js

### Ferramentas de Teste
- **Framework:** Utilizamos **Jest** para testes unitários e de integração.
- Para rodar os testes:
  ```bash
  npm test
  ```
- Cobertura mínima exigida: **80%**.

---

### Padrões de Código
- Utilizamos o **Biome** para lint e formatação unificada.
- Comandos úteis:
  ```bash
  npx biome lint .
  npx biome format . --write
  ```

Consulte os [Padrões Globais de Código](https://github.com/AbacatePay/sdk-standards/blob/main/contributors/CODING_STANDARDS.md).

---

### Fluxo de Pull Request (PR)
1. **Abra uma Issue** antes de qualquer PR.
2. Crie sua branch a partir da `develop`.
3. Adicione um Changeset:
   ```bash
   npx changeset
   ```
4. Garanta que o CI esteja passando.
5. Siga o [Guia de Commits](https://github.com/AbacatePay/sdk-standards/blob/main/contributors/COMMIT_GUIDELINES.md).

---

### Versionamento e Releases
- O versionamento é automatizado via **Changesets**.
- Após o merge na `main`, o processo de criação de tag e GitHub Release é automático.
- Consulte o [Fluxo de Release](https://github.com/AbacatePay/sdk-standards/blob/main/maintainers/RELEASE_PROCESS.md).

---

### Segurança e Dependências
- O **Dependabot** gerencia atualizações e segurança das dependências.
- Verifique manualmente com:
  ```bash
  npm audit
  ```

- Siga nossa [Política de Segurança](https://github.com/AbacatePay/sdk-standards/blob/main/policies/SECURITY_POLICY.md).

---

### Proteções e Qualidade
- Branch `main` é protegida.
- Commits diretos não são permitidos.
- PRs exigem aprovação e CI verde.