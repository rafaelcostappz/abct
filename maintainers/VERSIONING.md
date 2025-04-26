
# Política de Versionamento - AbacatePay SDKs

> Todos os SDKs open source da AbacatePay seguem o padrão **Semantic Versioning 2.0.0 (SemVer)**.

O objetivo é garantir previsibilidade, compatibilidade e transparência para todos que utilizam ou contribuem com nossos SDKs.

---

## Formato das Versões

```
MAJOR.MINOR.PATCH
```

Exemplo: `2.3.1`

---

## Definições

- **MAJOR**: Mudanças incompatíveis com versões anteriores (breaking changes).
  - Exemplo: Remoção ou alteração de comportamento de uma função pública.
  - **Requer RFC aprovada** e comunicação clara.

- **MINOR**: Adição de novas funcionalidades de forma retrocompatível.
  - Exemplo: Novos métodos, parâmetros opcionais.

- **PATCH**: Correções de bugs ou ajustes internos que não afetam a interface pública.
  - Exemplo: Fixes, melhorias de performance sem alteração de contrato.

---

## Pre-Releases

Para versões ainda em estágio de teste ou validação:

- Formato:
  ```
  1.4.0-alpha.1
  2.0.0-beta.3
  3.1.0-rc.1
  ```

- Sufixos aceitos:
  - `alpha`: Versões iniciais, instáveis.
  - `beta`: Funcionalidades completas, mas sujeitas a ajustes.
  - `rc` (release candidate): Versão candidata à final.

---

## Regras Complementares

- Nunca publique mudanças que quebrem compatibilidade sem atualizar o **MAJOR**.
- Toda alteração relevante deve ser documentada no [CHANGELOG.md](../CHANGELOG.md).
- O versionamento deve estar sempre alinhado com o [Processo de Release](/maintainers/RELEASE_PROCESS.md).
- Evite lançamentos excessivos — agrupe alterações sempre que possível.

---

## Referências

- [Documentação Oficial do SemVer](https://semver.org/lang/pt-BR/)
- [Processo de Release](/maintainers/RELEASE_PROCESS.md)
- [Política de Mudanças Críticas](/policies/BREAKING_CHANGES_POLICY.md)

---

> O versionamento correto é essencial para manter a confiança e estabilidade do ecossistema AbacatePay.