
# Diretrizes de Testes - AbacatePay SDKs

> Testes bem estruturados são essenciais para garantir a qualidade, estabilidade e evolução sustentável dos SDKs da AbacatePay.

Estas diretrizes definem os princípios gerais que devem ser seguidos em todos os repositórios, independentemente da linguagem.

---

## Princípios Gerais

- **Cobertura Obrigatória**: 
  - Toda nova funcionalidade deve incluir testes automatizados.
  - Correções de bugs devem conter testes que validem o problema corrigido.
  - A cobertura mínima recomendada é de **80%** para código novo.

- **Tipos de Testes**:
  - **Testes Unitários**: Base da pirâmide. Devem ser rápidos e isolados.
  - **Testes de Integração**: Quando houver interação entre módulos ou serviços externos.
  - **Testes E2E**: Apenas quando aplicável, principalmente em SDKs que expõem interfaces mais complexas.

- **Requisitos**:
  - Testes devem ser **determinísticos** (mesmo resultado em todas as execuções).
  - Devem ser claros, com nomes descritivos.
  - Evitar dependência de ambiente externo sem mock/stub.

---

## Durante o Desenvolvimento

- Nenhum Pull Request será aceito sem a devida cobertura de testes.
- A execução dos testes é obrigatória no pipeline de CI/CD.
- Testes devem ser incluídos no checklist do [Template de PR](/contributors/PULL_REQUEST_TEMPLATE.md).

---

## Ferramentas

Cada SDK define as ferramentas de teste conforme sua stack.  
Exemplos:

- **Node.js**: Jest, Mocha
- **Python**: Pytest
- **Go**: Testing package nativo
- **Java**: JUnit

Consulte o repositório específico para detalhes de configuração.

---

## Boas Práticas

- Priorize a simplicidade e clareza nos testes.
- Utilize mocks e fakes sempre que necessário para isolar o comportamento.
- Testes lentos ou flakey não serão tolerados.
- Automatize sempre que possível.

---

> Garantir a qualidade do código é responsabilidade de todos. Testes são parte fundamental desse compromisso.