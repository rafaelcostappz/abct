
# Roadmap para Criação de Repositórios - SDKs Open Source AbacatePay

> Este guia orienta os mantenedores na criação e configuração de novos repositórios de SDKs open source da AbacatePay, garantindo alinhamento com as políticas, padrões e boas práticas definidas no repositório central [sdk-standards](https://github.com/AbacatePay/sdk-standards).

Todo novo repositório deve nascer já integrado ao ecossistema da AbacatePay, priorizando consistência, segurança e colaboração.

---

## 1. Criação do Repositório

- Nomeie o repositório seguindo o padrão: `abacatepay-[linguagem]-sdk`
- Aplique a licença MIT.
- Defina o repositório como público.
- Adicione uma descrição clara sobre o propósito do SDK.

---

## 2. Estrutura Inicial

- Utilize o [boilerplate oficial](https://github.com/AbacatePay/sdk-boilerplate) como base.
- Inclua:
  - `README.md` com links para o sdk-standards.
  - `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`, `SECURITY.md` referenciando o repositório central.
  - `CHANGELOG.md` baseado no template.
- Estruture o código conforme a linguagem definida em [Languages](https://github.com/AbacatePay/sdk-standards/tree/main/languages).

---

## 3. Configuração de CI/CD

- Copie o workflow correspondente de [GITHUB_WORKFLOW_TEMPLATES](https://github.com/AbacatePay/sdk-standards/tree/main/ci/GITHUB_WORKFLOW_TEMPLATES).
- Configure o pipeline para rodar lint, testes, build e validações de segurança.
- Assegure o cumprimento dos [Quality Gates](https://github.com/AbacatePay/sdk-standards/blob/main/ci/QUALITY_GATES.md).

---

## 4. Políticas de Branch e Proteções

### Automação da Proteção de Branches via GitHub CLI

Para garantir consistência, utilize o arquivo padrão [branch-protection.json](https://github.com/AbacatePay/sdk-standards/tree/main/templates/branch-protection.json) do repositório central.

**Passo a Passo:**

1. Certifique-se de ter o GitHub CLI (`gh`) instalado e autenticado.
2. Execute o comando:

```bash
gh api -X PUT repos/AbacatePay/NOME-DO-REPO/branches/main/protection --input path/to/branch-protection.json
```

Referência: [Branch Protection API - GitHub](https://docs.github.com/pt/rest/branches/branch-protection)

Regras aplicadas:
- Aprovação mínima de PR.
- CI obrigatório antes do merge.
- Bloqueio de force push e deleção.
- Aplicação para administradores.

---

## 5. Segurança e Monitoramento

### Configuração do Dependabot

1. Acesse Settings > Security & analysis.
2. Ative:
   - Dependabot alerts
   - Dependabot security updates
   - Dependabot version updates

3. Crie o `.github/dependabot.yml` conforme o template.

Referência: [Configuração do Dependabot](https://docs.github.com/en/code-security/dependabot/working-with-dependabot/configuration-options-for-dependency-updates)

---

## 6. Checklist Final

- Estrutura e documentação aplicadas.
- CI/CD funcionando.
- Branches protegidas.
- Dependabot configurado.
- Pronto para contribuições públicas.

---

Automatizar a segurança e padronizar a configuração inicial garante a robustez e a confiabilidade dos SDKs open source da AbacatePay.