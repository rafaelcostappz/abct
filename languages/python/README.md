
# Padrões e Configurações - AbacatePay Python SDK

> Este documento centraliza os links e orientações específicas para contribuições no **abacatepay-python-sdk**.  
> As diretrizes gerais de contribuição estão no repositório central de padrões da AbacatePay.

Repositório oficial: [abacatepay-python-sdk](https://github.com/AbacatePay/abacatepay-python-sdk)

---

## Padrões de Código

- Consulte o arquivo [`CODING_STANDARDS.md`](https://github.com/AbacatePay/abacatepay-python-sdk/blob/main/CODING_STANDARDS.md) para regras específicas de estilo e organização em Python.
- Utilizamos:
  - **flake8** para lint.
  - **black** para formatação automática.
  - Configurações padrão estão em:
    - `setup.cfg`
    - `pyproject.toml`

---

## Testes

- Framework oficial: **pytest**
- Detalhes no [`TESTING_GUIDELINES.md`](https://github.com/AbacatePay/abacatepay-python-sdk/blob/main/TESTING_GUIDELINES.md)
- Cobertura mínima exigida: **80%**
- Testes automatizados via CI.

---

## CI/CD

- Pipeline configurado via **GitHub Actions**.
- Workflow principal: [`.github/workflows/ci.yml`](https://github.com/AbacatePay/abacatepay-python-sdk/blob/main/.github/workflows/ci.yml)

---

## Dependências e Gerenciamento

- Gerenciador de pacotes: **pip** com uso de `requirements.txt`.
- Para ambientes virtuais, recomenda-se o uso de **venv** ou **pipenv**.
- Sempre manter as dependências atualizadas e documentadas.

---

## Referências

- [Guia Geral de Contribuição](/contributors/CONTRIBUTING.md)
- [Padrões Globais de Código](/contributors/CODING_STANDARDS.md)
- [Diretrizes de Commits](/contributors/COMMIT_GUIDELINES.md)
- [Fluxo de Desenvolvimento](/contributors/DEVELOPMENT_WORKFLOW.md)

---

> Mantenha-se alinhado com as boas práticas da comunidade Python e respeite sempre as diretrizes da AbacatePay.