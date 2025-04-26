
# Padrões e Configurações - AbacatePay Java SDK

> Este documento centraliza os links e orientações específicas para contribuições no **abacatepay-java-sdk**.  
> As diretrizes gerais de contribuição estão no repositório central de padrões da AbacatePay.

Repositório oficial: [abacatepay-java-sdk](https://github.com/AbacatePay/abacatepay-java-sdk)

---

## Padrões de Código

- Consulte o arquivo [`CODING_STANDARDS.md`](https://github.com/AbacatePay/abacatepay-java-sdk/blob/main/CODING_STANDARDS.md) para regras específicas de estilo e organização em Java.
- Utilizamos:
  - **Google Java Style Guide** como base.
  - **Checkstyle** para análise estática.
  - Configurações no arquivo `checkstyle.xml`.

---

## Testes

- Framework oficial: **JUnit 5**
- Utilização de **Mockito** para mocks.
- Detalhes no [`TESTING_GUIDELINES.md`](https://github.com/AbacatePay/abacatepay-java-sdk/blob/main/TESTING_GUIDELINES.md)
- Cobertura mínima exigida: **80%**
- Integração com ferramentas como **JaCoCo** para análise de cobertura.

---

## CI/CD

- Pipeline configurado via **GitHub Actions**.
- Build e dependências gerenciadas com **Maven** (`pom.xml`).
- Workflow principal: [`.github/workflows/ci.yml`](https://github.com/AbacatePay/abacatepay-java-sdk/blob/main/.github/workflows/ci.yml)

---

## Dependências e Gerenciamento

- Projeto estruturado com **Maven**.
- Dependências definidas no `pom.xml`.
- Seguir práticas de versionamento semântico nas dependências.

---

## Referências

- [Guia Geral de Contribuição](/contributors/CONTRIBUTING.md)
- [Padrões Globais de Código](/contributors/CODING_STANDARDS.md)
- [Diretrizes de Commits](/contributors/COMMIT_GUIDELINES.md)
- [Fluxo de Desenvolvimento](/contributors/DEVELOPMENT_WORKFLOW.md)

---

> Mantenha o código Java limpo, bem estruturado e em conformidade com as diretrizes da AbacatePay.