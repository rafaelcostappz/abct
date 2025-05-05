
# Fluxo de Desenvolvimento - AbacatePay SDKs

> **Este documento define o fluxo oficial de desenvolvimento para todos os SDKs open source da AbacatePay.**

Seguir estas diretrizes garante consistência, qualidade e facilita a colaboração entre contribuidores e mantenedores.

---

## Estrutura de Branches

- `main`: Branch estável e protegida. Representa a última versão de produção.
- `develop`: Branch de integração contínua.
- `feat/*`: Novas funcionalidades.
- `fix/*`: Correções de bugs.
- `chore/*`: Manutenções e ajustes sem impacto direto em funcionalidades.

---

## Segurança no Desenvolvimento

- **Nunca** versionar tokens, chaves de API ou secrets em branches.
- Utilize variáveis de ambiente e **GitHub Secrets** para configurações sensíveis.
- Siga a [Política de Gerenciamento de Tokens](/policies/TOKEN_MANAGEMENT_POLICY.md) durante todo o ciclo de desenvolvimento.
- Caso identifique um vazamento acidental, interrompa o fluxo e acione imediatamente os procedimentos da [Política de Segurança](/policies/SECURITY_POLICY.md).

---

## Processo de Contribuição

1. Abra uma Issue antes de qualquer desenvolvimento.
2. Crie a branch adequada a partir de `develop`.
3. Certifique-se de que sua branch esteja **atualizada com a branch principal (`main` ou `develop`)**:
   ```
   git pull origin develop --rebase
   ```
4. Instale as dependências antes de começar:
   ```
   npm install
   ```
5. Siga o [Guia de Commits](/contributors/COMMIT_GUIDELINES.md).
6. Garanta que o código esteja:
   - Validado pelo lint.
   - Com testes atualizados e passando.
   - Em conformidade com os [Padrões de Código](/contributors/CODING_STANDARDS.md).
7. Abra o Pull Request para a branch `develop` utilizando o [Template de PR](/contributors/PULL_REQUEST_TEMPLATE.md).

> Pull Requests diretos para `main` não são permitidos.

---

## Revisão de Código

- Todo PR deve ser revisado por pelo menos **1 mantenedor**.
- Feedbacks devem ser tratados com profissionalismo.
- PRs não serão aprovados com falhas no pipeline de CI/CD.

Consulte as [Diretrizes de Code Review](/maintainers/CODE_REVIEW_GUIDELINES.md).

---

## Releases

- Versões são geradas a partir da branch `main`.
- Seguimos a [Política de Versionamento](/maintainers/VERSIONING.md).
- Detalhes completos em [RELEASE_PROCESS.md](/maintainers/RELEASE_PROCESS.md).

---

## Automação e Qualidade

- Commits e PRs disparam pipelines de CI.
- Testes, lint e validações de segurança são obrigatórios.

Consulte:
- [Visão Geral de CI/CD](/ci/CI_OVERVIEW.md)
- [Quality Gates](/ci/QUALITY_GATES.md)

---

> **Cumprir este fluxo garante a integridade e evolução dos SDKs AbacatePay.**
