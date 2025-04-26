
# Guia de Commits - AbacatePay SDKs

> A padronização das mensagens de commit é fundamental para garantir um histórico claro, facilitando revisões, automações e o entendimento da evolução do projeto.

Seguimos o padrão **Conventional Commits** em todos os repositórios de SDKs da AbacatePay.

---

## Formato da Mensagem

```
tipo: descrição breve no imperativo
```

### Exemplos

```
feat: adiciona suporte a webhook de estorno
fix: corrige erro na autenticação OAuth2
chore: atualiza dependências do projeto
docs: melhora instruções de instalação no README
```

---

## Tipos Permitidos

- **feat**: Nova funcionalidade.
- **fix**: Correção de bug.
- **docs**: Alterações na documentação.
- **chore**: Manutenções e tarefas internas (sem impacto no código de produção).
- **refactor**: Refatorações que não alteram comportamento externo.
- **test**: Inclusão ou ajuste de testes.
- **build**: Alterações que afetam o processo de build.
- **ci**: Configurações de integração contínua.
- **perf**: Melhorias de performance.
- **style**: Ajustes de formatação, lint, etc. (sem alteração de lógica).
- **release**: Commits relacionados a versionamento e publicações.

---

## Regras Gerais

- Use frases curtas e objetivas na descrição.
- Sempre no **imperativo** (ex: "adiciona", "corrige", "atualiza").
- Não use letras maiúsculas no tipo.
- Não termine a descrição com ponto final.
- Evite commits agrupando múltiplas alterações sem relação direta.

---

## O que Evitar

- Mensagens genéricas como:
  ```
  update
  ajustes
  mudanças
  ```
- Commits sem contexto claro.
- Commits em outros idiomas que não o português.

---

## Ferramentas Recomendadas

Considere o uso do [Commitizen](https://commitizen-tools.github.io/commitizen/) para auxiliar na padronização automática das mensagens de commit.

---

> Um histórico bem escrito é um legado para todos que colaboram com o projeto.