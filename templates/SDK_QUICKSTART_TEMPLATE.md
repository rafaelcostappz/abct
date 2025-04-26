
# Guia de Início Rápido - AbacatePay SDK

> Este guia vai te ajudar a integrar rapidamente os serviços da AbacatePay com seu projeto. Ele abrange os passos iniciais para começar a usar o SDK da AbacatePay de maneira simples e rápida.

## Instalação

Para começar, primeiro instale o SDK. Dependendo da linguagem que você está utilizando, escolha a opção correspondente:

### Node.js
```bash
npm install abacatepay-[linguagem]
```

### Python
```bash
pip install abacatepay-[linguagem]
```

### Go
```bash
go get github.com/AbacatePay/abacatepay-[linguagem]
```

### Java
```bash
# Dependência Maven
<dependency>
    <groupId>com.abacatepay</groupId>
    <artifactId>abacatepay-[linguagem]</artifactId>
    <version>1.0.0</version>
</dependency>
```

---

## Configuração

Após a instalação, é necessário configurar o SDK com suas credenciais da AbacatePay.

### Exemplo de Configuração

### Node.js
```javascript
const AbacatePay = require('abacatepay-[linguagem]');
const api = new AbacatePay({
  apiKey: 'SUA_CHAVE_API_AQUI'
});
```

### Python
```python
from abacatepay import AbacatePay

api = AbacatePay(api_key='SUA_CHAVE_API_AQUI')
```

### Go
```go
package main

import "github.com/AbacatePay/abacatepay-[linguagem]"

func main() {
    api := abacatepay.NewClient("SUA_CHAVE_API_AQUI")
}
```

### Java
```java
import com.abacatepay.AbacatePay;

public class Main {
    public static void main(String[] args) {
        AbacatePay api = new AbacatePay("SUA_CHAVE_API_AQUI");
    }
}
```

---

## Realizando a Primeira Requisição

Agora que você configurou o SDK, vamos fazer a primeira requisição. Este exemplo mostra como realizar um pagamento:

### Exemplo de Pagamento

### Node.js
```javascript
api.processPayment({
  amount: 100,
  currency: 'USD',
  // Outros parâmetros necessários
}).then(response => {
  console.log('Pagamento realizado:', response);
}).catch(error => {
  console.error('Erro ao realizar pagamento:', error);
});
```

### Python
```python
response = api.process_payment(amount=100, currency='USD')
print('Pagamento realizado:', response)
```

### Go
```go
response, err := api.ProcessPayment(100, "USD")
if err != nil {
    fmt.Println("Erro:", err)
} else {
    fmt.Println("Pagamento realizado:", response)
}
```

### Java
```java
String response = api.processPayment(100, "USD");
System.out.println("Pagamento realizado: " + response);
```

---

## Próximos Passos

- Consulte a [documentação completa](https://github.com/AbacatePay/abacatepay-[linguagem]/docs) para mais detalhes e funcionalidades.
- Abra uma **Issue** ou envie um **Pull Request** se tiver sugestões ou melhorias para o SDK.

---

> Esse guia é um ponto de partida. A AbacatePay está sempre trabalhando para melhorar os SDKs, e a comunidade tem papel fundamental nesse processo!