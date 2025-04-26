
# Padrões de Código - AbacatePay SDKs

> Este documento define diretrizes **gerais** de codificação aplicáveis a todos os SDKs open source da AbacatePay.  
> As regras específicas para cada linguagem estarão detalhadas em seus respectivos repositórios.

---

## Princípios Fundamentais

- **Clareza acima de tudo**: Código deve ser fácil de ler e entender.
- **Simplicidade**: Evite complexidade desnecessária.
- **Consistência**: Siga o padrão estabelecido no projeto.
- **Documentação**: Sempre que necessário, comente o "porquê", não o "como".
- **Evite código morto**: Remova trechos não utilizados.
- **Modularidade**: Prefira funções e métodos pequenos, com responsabilidades bem definidas.

---

## Convenções Gerais

- **Nomenclatura**:
  - Variáveis, funções e classes devem ter nomes descritivos.
  - Utilize o padrão de case adequado à linguagem (camelCase, snake_case, PascalCase).
  
- **Organização**:
  - Mantenha a estrutura de pastas conforme definido no SDK.
  - Agrupe arquivos relacionados de forma lógica.

- **Comentários**:
  - Evite comentários redundantes.
  - Utilize para explicar decisões importantes ou trechos complexos inevitáveis.
  - Priorize a autoexplicação pelo próprio código.

---

## Padrões Específicos por Linguagem

Cada SDK possui um documento próprio detalhando o padrão de codificação específico, localizado no repositório correspondente.

Exemplos:

- **Node.js SDK**: `CODING_STANDARDS.md` dentro do repositório [abacatepay-nodejs-sdk](https://github.com/AbacatePay/abacatepay-nodejs-sdk)
- **Go SDK**: idem para [abacatepay-go-sdk](https://github.com/AbacatePay/abacatepay-go-sdk)

Consulte sempre o guia da linguagem antes de iniciar qualquer contribuição.

---

## Referências

- Utilize o [Template de Estrutura de Documentação](/templates/DOCUMENTATION_STRUCTURE.md) para manter a padronização da documentação técnica.

---

> Seguir estas diretrizes garante um código mais sustentável, colaborativo e fácil de evoluir.