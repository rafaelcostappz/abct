
# Padrões e Configurações - AbacatePay Rails SDK

> Este documento centraliza os links e orientações específicas para contribuições no **abacatepay-rails-sdk**.  
> As diretrizes gerais de contribuição estão no repositório central de padrões da AbacatePay.

Repositório oficial: [abacatepay-rails-sdk](https://github.com/AbacatePay/abacatepay-rails-sdk)

---

## Padrões de Código

- Baseado no **Ruby Style Guide**.
- Utilizamos:
  - **RuboCop** para lint e formatação automática.
  - Configurações no `.rubocop.yml`.

---

## Testes

- Framework oficial: **RSpec**
- Cobertura mínima: **80%**
- Detalhes no [`TESTING_GUIDELINES.md`](https://github.com/AbacatePay/abacatepay-rails-sdk/blob/main/TESTING_GUIDELINES.md)

---

## CI/CD

- Pipeline via **GitHub Actions**.
- Workflow principal: [`.github/workflows/ci.yml`](https://github.com/AbacatePay/abacatepay-rails-sdk/blob/main/.github/workflows/ci.yml)

---

## Dependências

- Gerenciadas via `Gemfile` e `Bundler`.

---

## Referências

- [Guia Geral de Contribuição](/contributors/CONTRIBUTING.md)