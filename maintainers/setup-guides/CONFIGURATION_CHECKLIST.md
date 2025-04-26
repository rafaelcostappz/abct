
# Checklist de Configuração - SDKs Open Source AbacatePay

> Este checklist garante que todo novo repositório de SDK da AbacatePay esteja em total conformidade com as diretrizes do repositório central [`sdk-standards`](https://github.com/AbacatePay/sdk-standards).

Antes de liberar o repositório para contribuições públicas, valide cada item abaixo.

---

## Estrutura e Documentação

- [ ] Nome do repositório no formato `abacatepay-[linguagem]-sdk`.
- [ ] Licença **MIT** aplicada.
- [ ] `README.md` com links para o [`sdk-standards`](https://github.com/AbacatePay/sdk-standards).
- [ ] `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md` e `SECURITY.md` **referenciando** o repositório central.
- [ ] `CHANGELOG.md` criado.
- [ ] Estrutura de pastas conforme as diretrizes da linguagem: [Languages](https://github.com/AbacatePay/sdk-standards/tree/main/languages).
- [ ] Templates de **Pull Request** aplicados conforme o padrão do [`sdk-standards`](https://github.com/AbacatePay/sdk-standards/tree/main/templates).
- [ ] Templates de **Issue** configurados em `.github/ISSUE_TEMPLATE/`.

---

## CI/CD e Qualidade

- [ ] Workflows do **GitHub Actions** aplicados a partir dos templates: [`ci/GITHUB_WORKFLOW_TEMPLATES`](https://github.com/AbacatePay/sdk-standards/tree/main/ci/GITHUB_WORKFLOW_TEMPLATES).
- [ ] [Quality Gates](https://github.com/AbacatePay/sdk-standards/blob/main/ci/QUALITY_GATES.md) implementados.
- [ ] Pipeline validando lint, testes e segurança.
- [ ] Configuração de release conforme o [Guia de Releases](https://github.com/AbacatePay/sdk-standards/blob/main/maintainers/RELEASE_PROCESS.md).

---

## Segurança e Governança

- [ ] **Dependabot** habilitado.
- [ ] **GitHub Security Advisories** ativo.
- [ ] **Secret Scanning** habilitado nas configurações do GitHub.
- [ ] Conformidade com a [Política de Gerenciamento de Tokens](https://github.com/AbacatePay/sdk-standards/blob/main/policies/TOKEN_MANAGEMENT_POLICY.md).
- [ ] Branches `main` e `develop` protegidas (manual ou via `branch-protection.json`).
- [ ] CI obrigatório para merge.
- [ ] Aprovação mínima de 1 mantenedor por PR.
- [ ] Proibição de commits diretos na `main`.

---

## Pronto para Open Source

- [ ] Referência clara ao [`sdk-standards`](https://github.com/AbacatePay/sdk-standards) no README.
- [ ] Validação completa deste checklist.
- [ ] Comunicação interna de que o repositório está pronto para contribuições públicas.

---

## Referências

- [Roadmap de Criação](./NEW_REPOSITORY_ROADMAP.md)
- [Repositório Central](https://github.com/AbacatePay/sdk-standards)
- [Guia de CI/CD](https://github.com/AbacatePay/sdk-standards/blob/main/ci/CI_OVERVIEW.md)
- [Política de Segurança](https://github.com/AbacatePay/sdk-standards/blob/main/policies/SECURITY_POLICY.md)
- [Política de Gerenciamento de Tokens](https://github.com/AbacatePay/sdk-standards/blob/main/policies/TOKEN_MANAGEMENT_POLICY.md)

---

> A padronização garante que todos os SDKs da AbacatePay mantenham a mesma excelência, desde o primeiro commit.