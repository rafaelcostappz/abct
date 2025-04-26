
# Quality Gates - AbacatePay SDKs

Os **Quality Gates** definem os critérios mínimos que todos os SDKs open source da AbacatePay devem cumprir para garantir a qualidade, segurança e consistência do código antes de qualquer merge ou release.

Esses requisitos são validados automaticamente nos pipelines de **CI/CD**.

---

## Requisitos Obrigatórios

### 1. Lint e Análise Estática
- O código deve passar por verificações de lint sem erros.
- Warnings devem ser minimizados e, quando existentes, devidamente justificados.

### 2. Testes Automatizados
- Execução obrigatória de testes unitários e de integração.
- **Cobertura mínima**: 80% para código novo.
- Testes devem ser determinísticos e rápidos.

### 3. Build (Quando Aplicável)
- O SDK deve ser compilado/empacotado com sucesso.
- Sem erros ou warnings críticos no processo de build.

### 4. Validações de Segurança
- Nenhuma dependência com vulnerabilidades conhecidas (nível alto/crítico).
- Integração com ferramentas como **Dependabot** e scanners de segurança.

### 5. Versionamento Correto
- Validação de que mudanças estão de acordo com a [Política de Versionamento](/maintainers/VERSIONING.md).
- PRs que introduzem breaking changes devem conter evidências de aprovação via RFC.

---

## Política de Bloqueio

- PRs com falha em qualquer Quality Gate serão automaticamente **bloqueados**.
- Não é permitido ignorar ou forçar merges bypassando o pipeline.

---

## Ferramentas Recomendadas por Linguagem

- **Node.js**: ESLint, Jest, npm audit
- **Python**: flake8, pytest, safety
- **Go**: golangci-lint, go test, govulncheck
- **Java**: Checkstyle, JUnit, OWASP Dependency-Check
- **PHP**: PHP_CodeSniffer, PHPUnit
- **Kotlin**: detekt, ktlint, JUnit
- **Ruby**: RuboCop, RSpec, bundler-audit

---

## Revisão dos Quality Gates

- Os critérios devem ser revisados trimestralmente pelos mantenedores para ajustes conforme evolução das práticas e ferramentas.

---

## Referências

- [Visão Geral de CI/CD](/ci/CI_OVERVIEW.md)
- [Diretrizes de Testes](/contributors/TESTING_GUIDELINES.md)
- [Política de Segurança](/policies/SECURITY_POLICY.md)

---

> Manter um padrão rigoroso de qualidade é essencial para a confiança e sustentabilidade dos SDKs da AbacatePay.