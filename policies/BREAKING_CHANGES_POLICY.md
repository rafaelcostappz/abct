
# Política de Breaking Changes - AbacatePay SDKs

Mudanças que quebram compatibilidade (**breaking changes**) são, por vezes, necessárias para a evolução dos SDKs. No entanto, devem ser tratadas com extremo cuidado, transparência e planejamento.

Esta política define quando e como aplicar mudanças críticas, garantindo previsibilidade para todos os usuários.

---

## O Que é uma Breaking Change

Qualquer alteração que:

- Modifique ou remova a interface pública existente.
- Altere o comportamento esperado de métodos ou funções.
- Introduza requisitos incompatíveis com versões anteriores.
- Afete contratos de API consumidos pelos SDKs.

---

## Quando São Permitidas

- Apenas quando não houver alternativa viável mantendo compatibilidade.
- Necessidade justificada por:
  - Segurança
  - Correção de design crítico
  - Alinhamento com atualizações da API da AbacatePay
- **Obrigatoriamente precedida por uma RFC aprovada**.

---

## Processo para Implementação

1. **Discussão e Aprovação**
   - Formalizar a proposta via [RFCs](https://rafaelcostappz.github.io/abacatepay-rfcs/).

2. **Anúncio Antecipado**
   - Comunicar a comunidade com antecedência mínima de **1 ciclo de release**.

3. **Versão MAJOR**
   - Aplicar somente em releases que seguem a [Política de Versionamento](/maintainers/VERSIONING.md) para mudanças MAJOR.

4. **Documentação**
   - Registrar detalhadamente no [CHANGELOG.md](../CHANGELOG.md).
   - Fornecer guia de migração sempre que possível.

5. **Validação**
   - Garantir que o pipeline de CI/CD detecte usos obsoletos ou incompatíveis, quando aplicável.

---

## Boas Práticas

- Agrupar breaking changes para evitar múltiplas quebras em curto prazo.
- Evitar surpresas: comunique sempre e com clareza.
- Oferecer deprecated warnings antes da remoção, sempre que viável.

---

## Referências

- [Política de Versionamento](/maintainers/VERSIONING.md)
- [Processo de Release](/maintainers/RELEASE_PROCESS.md)
- [Política de Deprecação](/policies/DEPRECATION_POLICY.md)

---

> Transparência e planejamento são essenciais para que mudanças críticas não comprometam a confiança da comunidade.