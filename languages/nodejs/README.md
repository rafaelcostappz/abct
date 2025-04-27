<p align="center">
  <img src="https://github.com/rafaelcostappz/abacatepay-default/blob/main/assets/banner.png?raw=true" alt="AbacatePay Banner" width="100%">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/CI-passing-4CAF50?style=for-the-badge&logo=githubactions&logoColor=white&labelColor=2E7D32" alt="CI Status"/>
  <img src="https://img.shields.io/badge/Security-monitored-2196F3?style=for-the-badge&logo=shield&logoColor=white&labelColor=1565C0" alt="Security"/>
  <img src="https://img.shields.io/badge/Tests-passed-9C27B0?style=for-the-badge&logo=jest&logoColor=white&labelColor=6A1B9A" alt="Tests"/>
</p>

<p align="center">
  <a href="https://rafaelcostappz.github.io/abct/#/contributors/CONTRIBUTING">
     Contribuir
  </a> •
  <a href="https://rafaelcostappz.github.io/abct/#/policies/SECURITY_POLICY">
     Segurança
  </a> •
  <a href="https://rafaelcostappz.github.io/abct/#/contributors/CODE_OF_CONDUCT">
    Código de Conduta
  </a>
</p>



## AbacatePay Nodejs SDK

Official NodeJS SDK for AbacatePay - Accept payments in seconds with a simple integration.

### <img src="https://github.com/rafaelcostappz/abacatepay-default/blob/main/assets/processor-svgrepo-com.svg?raw=true" height="22" valign="middle"/> Installation

```bash
npm install abacatepay-nodejs-sdk
```

### <img src="https://github.com/rafaelcostappz/abacatepay-default/blob/main/assets/browser-svgrepo-com.svg?raw=true" height="22" valign="middle"/>  Quick Start

```js
import AbacatePay from 'abacatepay-nodejs-sdk';

// Initialize the SDK with your API key
const abacate = AbacatePay('your_api_key');
```

## <img src="https://raw.githubusercontent.com/rafaelcostappz/abacatepay-default/45d0daa990361db6360a1a274544e86f4c4057d3/assets/go-svgrepo-com%20(1).svg" height="20" valign="middle"/> Usage



> Creating a Payment

```js
const billing = await abacate.billing.create({
  frequency: "ONE_TIME",
  methods: ["PIX"],
  products: [
    {
      externalId: "PRO-PLAN",
      name: "Pro plan",
      quantity: 1,
      price: 1000 // Amount in cents
    }
  ],
  returnUrl: "https://yoursite.com/app",
  completionUrl: "https://yoursite.com/pagamento/sucesso",
  customer: {
    email: 'customer@example.com'
  }
});
```

> Response

```js
{
  _id: 'bill_12345667',
  url: 'https://abacatepay.com/pay/bill_12345667',
  amount: 1000,
  status: 'PENDING',
  devMode: true,
  methods: ['PIX'],
  frequency: 'ONE_TIME',
  nextBilling: null,
  customer: {
    id: 'cust_12345',
    metadata: {
      email: 'customer@example.com'
    }
  },
  createdAt: '2024-11-04T18:38:28.573',
  updatedAt: '2024-11-04T18:38:28.573',
}
```

### <img src="https://raw.githubusercontent.com/rafaelcostappz/abacatepay-default/45d0daa990361db6360a1a274544e86f4c4057d3/assets/creditcard-svgrepo-com.svg" height="20" valign="middle"> Payment Methods

Currently supported payment methods:
- PIX (Instant Brazilian payment system)

### <img src="https://raw.githubusercontent.com/rafaelcostappz/abacatepay-default/642b0ba3cda42f3289435bb58fafd14f0cfc3d1a/assets/document-svgrepo-com.svg" height="20" valign="middle"> License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.