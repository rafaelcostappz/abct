
# Diretrizes de Code Review - AbacatePay SDKs

> O processo de revisão de código é essencial para manter a qualidade, segurança e consistência dos SDKs da AbacatePay.

Estas diretrizes orientam os mantenedores sobre como conduzir revisões de forma eficiente, colaborativa e alinhada aos padrões da empresa.

---

## Objetivos da Revisão

- Garantir que o código esteja em conformidade com os [Padrões de Código](/contributors/CODING_STANDARDS.md) e boas práticas.
- Verificar a cobertura e qualidade dos testes.
- Identificar potenciais problemas de segurança ou performance.
- Assegurar que as mudanças estejam bem documentadas.
- Promover aprendizado e alinhamento entre contribuidores e mantenedores.

---

## Checklist de Revisão

- [ ] O título e a descrição do PR estão claros e seguem o [Template de PR](/contributors/PULL_REQUEST_TEMPLATE.md).
- [ ] A Issue está corretamente vinculada.
- [ ] O código segue os padrões definidos para a linguagem.
- [ ] Não há código duplicado ou desnecessário.
- [ ] Testes foram adicionados/atualizados conforme o [Guia de Testes](/contributors/TESTING_GUIDELINES.md).
- [ ] O pipeline de CI/CD passou sem erros.
- [ ] O [CHANGELOG.md](../CHANGELOG.md) foi atualizado, se aplicável.
- [ ] Não há impacto negativo em segurança ou performance.
- [ ] A documentação foi ajustada, se necessário.

---

## Boas Práticas ao Revisar

- Seja claro e objetivo no feedback.
- Prefira sugestões construtivas ao invés de críticas vagas.
- Explique o **motivo** da solicitação de mudança.
- Use comentários **respeitosos** e mantenha o tom colaborativo.
- Quando possível, sugira exemplos ou links para referência.

---

## Quando Solicitar Alterações

- Quebra de padrões ou boas práticas.
- Falta de testes adequados.
- Problemas de legibilidade ou complexidade desnecessária.
- Potenciais riscos de segurança.
- Qualquer inconsistência com o roadmap ou arquitetura definida.

---

## Quando Aprovar

- Todos os itens do checklist foram atendidos.
- O código está limpo, testado e bem documentado.
- O impacto da mudança foi devidamente analisado.
- Feedbacks anteriores foram aplicados.

---

## PRs Urgentes (Hotfixes)

- Em casos críticos, priorize a correção, mas **nunca ignore o processo**.
- Realize uma revisão pós-merge se necessário, para garantir que padrões foram mantidos.

---

## Referências

- [Guia de Contribuição](/contributors/CONTRIBUTING.md)
- [Guia de Commits](/contributors/COMMIT_GUIDELINES.md)
- [Processo de Release](/maintainers/RELEASE_PROCESS.md)
- [Protocolo de Segurança](/maintainers/SECURITY_HANDLING.md)

---

> Uma boa revisão não é apenas aprovar código, mas garantir que ele eleve o padrão do projeto.