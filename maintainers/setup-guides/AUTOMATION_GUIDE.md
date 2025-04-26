
# Guia de Automação - Configuração de Repositórios AbacatePay SDKs

> Este guia apresenta práticas recomendadas para automatizar a criação e configuração de novos repositórios de SDKs open source da AbacatePay, garantindo agilidade sem abrir mão da conformidade com nossos padrões.

Automatizar processos repetitivos reduz erros manuais e assegura que todos os repositórios sigam as diretrizes definidas no [sdk-standards](https://github.com/AbacatePay/sdk-standards).

---

## 1. Uso do Repositório Boilerplate

- Sempre que possível, inicie a partir do [sdk-boilerplate](https://github.com/AbacatePay/sdk-boilerplate).
- Clonagem rápida via GitHub:
  ```bash
  gh repo create abacatepay-novo-sdk --public --template AbacatePay/sdk-boilerplate
  ```
- O boilerplate já inclui:
  - Estrutura básica de pastas.
  - Arquivos padrão (`README.md`, `CONTRIBUTING.md`, etc.) com links para o repositório central.
  - Configuração inicial de CI/CD.

---

## 2. Reutilização de Workflows (GitHub Actions)

- Utilize workflows reutilizáveis definidos em [ci/GITHUB_WORKFLOW_TEMPLATES](https://github.com/AbacatePay/sdk-standards/tree/main/ci/GITHUB_WORKFLOW_TEMPLATES).
- Exemplo de chamada:

  ```yaml
  jobs:
    ci:
      uses: AbacatePay/sdk-standards/.github/workflows/ci-nodejs.yml@main
      with:
        node-version: '18'
  ```

- Certifique-se de que o workflow esteja em conformidade com os [Quality Gates](https://github.com/AbacatePay/sdk-standards/blob/main/ci/QUALITY_GATES.md).

---

## 3. Configuração Automática de Dependabot

- Copie o arquivo padrão:
  ```bash
  cp sdk-standards/templates/dependabot.yml .github/dependabot.yml
  ```

- Verifique se a configuração está alinhada com a [Política de Segurança](https://github.com/AbacatePay/sdk-standards/blob/main/policies/SECURITY_POLICY.md).

---

## 4. Proteção de Branch via GitHub CLI

- Aplique a proteção de branches utilizando o JSON padrão:
  ```bash
  gh api -X PUT repos/AbacatePay/abacatepay-novo-sdk/branches/main/protection --input templates/branch-protection.json
  ```

- Consulte a [Política de Gerenciamento de Tokens](https://github.com/AbacatePay/sdk-standards/blob/main/policies/TOKEN_MANAGEMENT_POLICY.md) para garantir práticas seguras.

---

## 5. Scripts de Automação

- Centralize scripts no diretório `/scripts` do boilerplate.
- Exemplo de execução:

  ```bash
  ./scripts/setup-repo.sh nodejs
  ```

- Scripts devem validar:
  - Proteção de branch aplicada.
  - Dependabot ativo.
  - Criação da branch `develop`.
  - Configuração inicial de GitHub Secrets (quando aplicável).

---

## Checklist de Automação Aplicada

- [ ] Boilerplate clonado e adaptado.
- [ ] Workflows reutilizáveis integrados.
- [ ] Dependabot configurado.
- [ ] Proteção de branch aplicada.
- [ ] Scripts de setup executados.
- [ ] Conformidade com políticas de segurança e tokens verificada.

---

## Referências

- [Boilerplate Oficial](https://github.com/AbacatePay/sdk-boilerplate)
- [Templates de CI/CD](https://github.com/AbacatePay/sdk-standards/tree/main/ci/GITHUB_WORKFLOW_TEMPLATES)
- [Quality Gates](https://github.com/AbacatePay/sdk-standards/blob/main/ci/QUALITY_GATES.md)
- [Política de Segurança](https://github.com/AbacatePay/sdk-standards/blob/main/policies/SECURITY_POLICY.md)
- [Política de Gerenciamento de Tokens](https://github.com/AbacatePay/sdk-standards/blob/main/policies/TOKEN_MANAGEMENT_POLICY.md)
- [Checklist de Configuração](./CONFIGURATION_CHECKLIST.md)

---

A automação é a chave para escalar com qualidade. Padronize, automatize e foque no que realmente importa: construir SDKs robustos e colaborativos.