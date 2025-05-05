
# Processo de Release - AbacatePay SDKs

> Este documento define o fluxo oficial para criação e publicação de novas versões dos SDKs open source da AbacatePay.

Seguir este processo garante que todas as releases sejam consistentes, auditáveis e alinhadas com as práticas de versionamento adotadas.

---

## Pré-Requisitos para um Release

Antes de gerar uma nova versão, assegure-se de que:

- Todos os Pull Requests relacionados foram revisados e aprovados.
- O pipeline de **CI/CD** está 100% verde.
- O [CHANGELOG.md](../CHANGELOG.md) foi atualizado com as mudanças relevantes.
- A versão está de acordo com a [Política de Versionamento](/maintainers/VERSIONING.md).
- Não há Issues críticas abertas relacionadas à release.

---

## Tipos de Releases

- **Patch** (`x.y.Z`): Correções de bugs sem alteração de comportamento.
- **Minor** (`x.Y.z`): Novas funcionalidades compatíveis com versões anteriores.
- **Major** (`X.y.z`): Mudanças que quebram compatibilidade. Exigem RFC aprovada e comunicação ampla.

Hotfixes devem seguir o fluxo de **patch release**, priorizando a correção imediata.

---

## Fluxo de Release

1. **Branch de Release**  
   Crie uma branch a partir da `main`:
   ```
   git checkout -b release/x.y.z
   ```

2. **Atualize o Changelog e a Versão**  
   Ajuste o `CHANGELOG.md` e arquivos de versionamento conforme o SDK.

3. **Crie a Tag**  
   Após merge na `main`, crie a tag semântica:
   ```
   git tag -a vX.Y.Z -m "Release vX.Y.Z"
   git push origin vX.Y.Z
   ```

4. **Disparo do Pipeline de Release**  
   A publicação será feita automaticamente via **GitHub Actions**.

5. **Confirmação e Comunicação**  
   - Verifique a publicação (ex: NPM, PyPI, etc.).
   - Documente a release na aba de **Releases** do GitHub.
   - Caso aplicável, comunique a comunidade sobre mudanças importantes.

---

## Automação

- Sempre que possível, utilize ferramentas como:
  - **Changesets** (para SDKs que suportam)
  - Scripts de release integrados no pipeline.

Consulte a configuração específica no repositório de cada SDK.

---

## Considerações Finais

- Releases devem ser realizadas por mantenedores autorizados.
- Evite lançamentos fora do fluxo descrito.
- Em caso de erro crítico, siga o protocolo de **rollback** documentado no CI.

---

> Um processo de release bem definido garante confiança, estabilidade e previsibilidade para todos os usuários dos SDKs AbacatePay.
