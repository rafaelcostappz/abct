
# Padrões e Configurações - AbacatePay Go SDK

> Este documento centraliza os links e orientações específicas para contribuições no **abacatepay-go-sdk**.  
> As diretrizes gerais de contribuição estão no repositório central de padrões da AbacatePay.

Repositório oficial: [abacatepay-go-sdk](https://github.com/AbacatePay/abacatepay-go-sdk)

---

## Padrões de Código

- Consulte o arquivo [`CODING_STANDARDS.md`](https://github.com/AbacatePay/abacatepay-go-sdk/blob/main/CODING_STANDARDS.md) para regras específicas de estilo e organização em Go.
- Utilizamos:
  - **gofmt** e **goimports** para formatação.
  - **golangci-lint** para análise estática.
  - Configurações estão no `.golangci.yml`.

---

## Testes

- Framework nativo: `testing`
- Utilização de **testify** para asserts e mocks.
- Detalhes no [`TESTING_GUIDELINES.md`](https://github.com/AbacatePay/abacatepay-go-sdk/blob/main/TESTING_GUIDELINES.md)
- Cobertura mínima exigida: **80%**
- Execução automatizada via CI.

---

## CI/CD

- Pipeline via **GitHub Actions**.
- Workflow principal: [`.github/workflows/ci.yml`](https://github.com/AbacatePay/abacatepay-go-sdk/blob/main/.github/workflows/ci.yml)

---

## Dependências e Gerenciamento

- Gerenciamento via `go.mod` e `go.sum`.
- Utilizamos Go Modules.
- Evite dependências desnecessárias e mantenha o código idiomático.

---

## Referências

- [Guia Geral de Contribuição](/contributors/CONTRIBUTING.md)
- [Padrões Globais de Código](/contributors/CODING_STANDARDS.md)
- [Diretrizes de Commits](/contributors/COMMIT_GUIDELINES.md)
- [Fluxo de Desenvolvimento](/contributors/DEVELOPMENT_WORKFLOW.md)

---

> Escreva código Go limpo, idiomático e alinhado com as práticas da AbacatePay.