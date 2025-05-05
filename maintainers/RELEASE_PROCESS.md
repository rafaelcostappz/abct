# Processo de Release - AbacatePay SDKs

Este documento define o fluxo oficial para criação e publicação de novas versões dos SDKs open source da AbacatePay.

> Este processo é compartilhado entre todos os SDKs e ajustado para contemplar diferentes linguagens e ferramentas (Node.js, Go, Python etc.).

Seguir este fluxo garante que todas as releases sejam consistentes, auditáveis e alinhadas com as práticas modernas de versionamento.

---

## Pré-Requisitos para um Release

Antes de iniciar um ciclo de release, verifique se:

- Todos os Pull Requests relevantes foram revisados e aprovados.
- O pipeline de CI/CD na branch `develop` está 100% verde.
- O `CHANGELOG.md` foi atualizado (automaticamente via Changesets ou manualmente, dependendo do SDK).
- A versão segue a [Política de Versionamento](/maintainers/VERSIONING.md).
- Não há Issues críticas abertas relacionadas à release.

---

## Tipos de Releases

- **Patch (x.y.Z):** Correções de bugs sem alteração de comportamento.
- **Minor (x.Y.z):** Novas funcionalidades compatíveis com versões anteriores.
- **Major (X.y.z):** Mudanças que quebram compatibilidade. Exigem aprovação de RFC e comunicação prévia.

> Hotfixes devem seguir o fluxo de release de patch, priorizando a correção imediata.

---

## Fluxo de Release

1. Garanta que `develop` esteja atualizado com os PRs finalizados.
2. Faça o merge de `develop` na branch `main`.
3. O pipeline de release será automaticamente disparado pelo GitHub Actions.
4. A publicação será feita no registro apropriado (npm, PyPI, etc.).
5. A tag semântica (`vX.Y.Z`) será criada automaticamente (quando configurado).
6. Finalize o preenchimento da aba **Releases** no GitHub com o changelog da versão.

---

## Automação

O processo de release pode variar entre SDKs. Verifique os arquivos de configuração no repositório.

- **Node.js**: Utiliza [Changesets](https://github.com/changesets/changesets) para versionamento e changelog automático. O release ocorre após o merge na `main`.
- **Go / Python / Outros**: Utilizam tags manuais ou scripts no CI. Consulte `Makefile`, `setup.py`, ou `.github/workflows/release.yml` conforme o caso.

---

## Protocolo de Rollback

Em caso de incidente grave ou liberação incorreta de versão, siga o protocolo de rollback:

1. **Interrompa o pipeline de publicação imediatamente**, se estiver em execução.
2. **Remova ou desative a release** no registro (npm, PyPI, etc.), quando possível.
3. **Crie uma nova tag de correção** (`vX.Y.Z+rollback`) para registrar a reversão.
4. **Abra uma Issue interna de segurança** documentando o ocorrido e ações tomadas.
5. **Atualize o changelog e comunique a comunidade**, caso o release tenha sido público.
6. **Reforce a revisão de PRs e processos de CI**, se a causa for humana ou automatizada.

Este protocolo segue boas práticas comuns em projetos open source para manter a estabilidade e confiança no ecossistema.

---

> Um processo de release bem definido garante confiança, estabilidade e previsibilidade para todos os usuários dos SDKs AbacatePay.
