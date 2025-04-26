
# Política de Deprecação - AbacatePay SDKs

A evolução constante dos SDKs da AbacatePay pode exigir, em determinados momentos, a descontinuação de funcionalidades, métodos ou versões. Esta política garante que o processo de deprecação seja realizado de forma **transparente, planejada e com mínimo impacto** para a comunidade.

---

## Quando Algo é Depreciado

- A funcionalidade se tornou obsoleta ou insegura.
- Existem alternativas mais eficientes ou alinhadas com novas práticas.
- Mudanças na API da AbacatePay que tornam o recurso inviável.
- Simplificação e manutenção do código a longo prazo.

---

## Processo de Deprecação

1. **Anúncio Formal**
   - A deprecação será comunicada via:
     - [CHANGELOG.md](../CHANGELOG.md)
     - Documentação oficial
     - Issues ou Discussions (quando aplicável)
   - Será informado o motivo e o prazo para remoção.

2. **Marcação no Código**
   - Inserção de anotação clara:
     ``` 
     @deprecated desde a versão X.Y.Z - Use XYZ como alternativa.
     ```

3. **Período de Suporte**
   - Funcionalidades depreciadas permanecerão ativas por pelo menos **1 versão MINOR** antes da remoção.

4. **Remoção Definitiva**
   - A exclusão ocorrerá apenas em uma **versão MAJOR**, conforme nossa [Política de Versionamento](/maintainers/VERSIONING.md).

---

## Comunicação com a Comunidade

- Sempre que possível, forneceremos alternativas e guias de migração.
- Deprecações relevantes serão destacadas nas notas de release.
- Discussões prévias podem ser abertas via RFCs para casos de grande impacto.

---

## Exemplo de Aviso de Deprecação

```markdown
[Deprecação] O método `processPaymentLegacy` será removido na versão 3.0.0.
Utilize `processPaymentV2` como substituto. Mais detalhes na documentação.
```

---

## Referências

- [Política de Versionamento](/maintainers/VERSIONING.md)
- [Política de Mudanças Críticas](/policies/BREAKING_CHANGES_POLICY.md)
- [Processo de Release](/maintainers/RELEASE_PROCESS.md)

---

> Deprecar com responsabilidade é garantir a evolução saudável dos SDKs sem comprometer a confiança da comunidade.