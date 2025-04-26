
# Padrões de API - AbacatePay SDKs

Para garantir a consistência, segurança e previsibilidade no consumo das APIs da AbacatePay, todos os SDKs devem seguir os padrões descritos neste documento.

Essas diretrizes asseguram que integrações sejam robustas, fáceis de manter e alinhadas com as melhores práticas do mercado.

---

## Estrutura Geral

- **Formato de Dados**: Todas as APIs utilizam **JSON** como padrão de entrada e saída.
- **Endpoints**: Devem ser descritivos e utilizar convenções RESTful.
  - Exemplo:
    ```
    GET /v1/payments/{id}
    POST /v1/transactions
    ```

- **Versionamento de API**:
  - A versão da API deve ser explicitada na URL (`/v1/`).
  - Mudanças incompatíveis exigem incremento da versão MAJOR.

- **Métodos HTTP**:
  - `GET`: Consulta de dados.
  - `POST`: Criação de recursos.
  - `PUT` / `PATCH`: Atualização.
  - `DELETE`: Remoção.

---

## Tratamento de Erros

- Sempre retornar códigos HTTP adequados:
  - `200 OK`, `201 Created`, `400 Bad Request`, `401 Unauthorized`, `404 Not Found`, `500 Internal Server Error`, etc.
- Estrutura padrão para respostas de erro:
  ```json
  {
    "error": {
      "code": "INVALID_PARAMETER",
      "message": "O campo 'amount' é obrigatório."
    }
  }
  ```

---

## Autenticação e Segurança

- Uso obrigatório de **OAuth2** ou **API Tokens** conforme especificação da AbacatePay.
- Todas as requisições devem ser feitas via HTTPS.
- Tokens nunca devem ser expostos em logs ou mensagens de erro.

---

## Boas Práticas

- **Idempotência**: Garantir que operações como POST possam ser repetidas com segurança quando aplicável.
- **Paginação**: Para endpoints que retornam listas, utilizar padrões de paginação (`limit` / `offset`).
- **Timeouts e Retry**: Respeitar limites e implementar políticas de retentativa onde necessário.

---

## Documentação

- Toda API deve ser documentada utilizando **OpenAPI (Swagger)**.
- SDKs devem refletir fielmente a documentação oficial da API da AbacatePay.
- Manter exemplos atualizados e claros.

---

## Referências

- [Documentação Oficial da API AbacatePay](https://api.abacatepay.com/docs)
- [Política de Versionamento](/maintainers/VERSIONING.md)
- [Política de Breaking Changes](/policies/BREAKING_CHANGES_POLICY.md)
- [Guia de Contribuição](/contributors/CONTRIBUTING.md)

---

> APIs consistentes e bem documentadas são a base para integrações seguras e eficientes.