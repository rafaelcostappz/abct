
<p align="center">
  <img src="https://github.com/rafaelcostappz/abacatepay-default-sdk/blob/main/assets/sdknodejs.png?raw=true" alt="AbacatePay SDK" width="250">
  <br>
</p>



<p align="center">
  <!-- Badges -->
  <a href="https://github.com/rafaelcostappz/abacatepay-default-sdk/actions">
    <img src="https://github.com/rafaelcostappz/abacatepay-default-sdk/actions/workflows/ci.yml/badge.svg" alt="Build Status"/>
  </a>
  <a href="https://github.com/rafaelcostappz/abacatepay-default-sdk/security/advisories">
    <img src="https://img.shields.io/badge/security-monitored-brightgreen.svg" alt="Security"/>
  </a>
  <a href="https://github.com/AbacatePay/sdk-standards/blob/main/contributors/TESTING_GUIDELINES.md">
    <img src="https://img.shields.io/badge/tests-passed-blue.svg" alt="Tests"/>
  </a>
</p>

<p align="center">
  <!-- Links Rápidos -->
  <a href="https://rafaelcostappz.github.io/abct/#/contributors/CONTRIBUTING">Contribuir</a> •
  <a href="https://rafaelcostappz.github.io/abct/#/policies/SECURITY_POLICY">Segurança</a> •
  <a href="https://rafaelcostappz.github.io/abct/#/contributors/CODE_OF_CONDUCT">Código de Conduta</a>
</p>

---

# AbacatePay Node.js SDK

> Este SDK permite que você integre facilmente os serviços de pagamento da AbacatePay com seu projeto Node.js, oferecendo uma interface simples e eficiente para interagir com nossa API.

## Instalação

Instale o SDK via **npm**:

```bash
npm install abacatepay-nodejs-sdk
```

## Como Usar

Após a instalação, basta configurar a chave de API e começar a fazer requisições.

### Exemplo de Uso

```javascript
const AbacatePay = require('abacatepay-nodejs-sdk');
const api = new AbacatePay({ apiKey: 'SUA_CHAVE_API_AQUI' });

api.processPayment({
  amount: 100,
  currency: 'USD',
  // Outros parâmetros
}).then(response => {
  console.log('Pagamento realizado:', response);
}).catch(error => {
  console.error('Erro ao realizar pagamento:', error);
});
```

## Links Importantes

Antes de contribuir, consulte os seguintes documentos para garantir que sua contribuição esteja alinhada com as práticas e políticas da AbacatePay:

- **[Guia Geral de Contribuição](https://github.com/AbacatePay/sdk-standards/blob/main/contributors/CONTRIBUTING.md)**
- **[Código de Conduta](https://github.com/AbacatePay/sdk-standards/blob/main/contributors/CODE_OF_CONDUCT.md)**
- **[Diretrizes de Commits](https://github.com/AbacatePay/sdk-standards/blob/main/contributors/COMMIT_GUIDELINES.md)**
- **[Política de Segurança](https://github.com/AbacatePay/sdk-standards/blob/main/policies/SECURITY_POLICY.md)**

> A AbacatePay mantém todos os SDKs em conformidade com as diretrizes open source e garante segurança, qualidade e transparência. python -m http.server 3000