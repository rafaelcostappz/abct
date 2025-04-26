
# Procedimentos de Segurança - AbacatePay SDKs

> Este documento orienta os mantenedores sobre como lidar com vulnerabilidades e incidentes de segurança nos SDKs open source da AbacatePay.

Garantir a segurança dos SDKs é uma responsabilidade contínua e crítica. Este guia descreve o processo oficial para identificação, tratamento e comunicação de falhas de segurança.

---

## Identificação e Report

- Vulnerabilidades podem ser identificadas por:
  - Contribuidores ou usuários (via canais privados de reporte).
  - Ferramentas automatizadas (ex: **Dependabot**, scanners de segurança).
  - Revisões internas de código.

- Todos os reports devem ser enviados para:  
  **security@abacatepay.com**

- Nunca discuta vulnerabilidades publicamente antes da correção e divulgação coordenada.

Consulte a [Política de Segurança](/policies/SECURITY_POLICY.md) para detalhes sobre o canal de reporte público.


---

## Vazamento de Tokens e Credenciais

Em caso de identificação de tokens, chaves de API ou secrets expostos:

1. **Revogação Imediata**
   - Revogue o token ou credencial comprometida assim que detectado.

2. **Triagem e Registro**
   - Classifique como incidente **crítico** e registre em ambiente privado.

3. **Histórico Git**
   - Caso o token tenha sido commitado, reescreva o histórico utilizando ferramentas como `git filter-repo` ou `bfg-repo-cleaner`.

4. **Rotação de Credenciais**
   - Gere novas credenciais e atualize os ambientes necessários.

5. **Comunicação**
   - Informe o time de segurança através do canal oficial.

6. **Revisão de Processo**
   - Avalie a causa raiz e reforce as práticas descritas na [Política de Gerenciamento de Tokens](/policies/TOKEN_MANAGEMENT_POLICY.md).

---

## Processo de Tratamento de Vulnerabilidades

1. **Triagem Inicial**
   - Avaliar a criticidade (Baixa, Média, Alta, Crítica).
   - Registrar o incidente em área privada (ex: GitHub Security Advisories).

2. **Designação**
   - Definir mantenedores responsáveis pela correção.

3. **Desenvolvimento do Patch**
   - Criar uma branch privada para o hotfix.
   - Garantir que todos os testes sejam executados.

4. **Revisão Interna**
   - Revisão obrigatória por, no mínimo, **2 mantenedores**.

5. **Release**
   - Seguir o fluxo de **patch release** descrito no [Processo de Release](/maintainers/RELEASE_PROCESS.md).
   - Utilizar o mecanismo de publicação segura no GitHub.

6. **Divulgação Coordenada**
   - Após a correção, publicar o aviso de segurança.
   - Atualizar o [CHANGELOG.md](../CHANGELOG.md) com a devida anotação.

---

## Boas Práticas

- Mantenha as dependências sempre atualizadas.
- Utilize ferramentas de análise estática e scanners de vulnerabilidades.
- Realize revisões periódicas de segurança.
- Evite exposição desnecessária de informações sensíveis no código.
- **Nunca exponha tokens ou informações sensíveis.**
- Consulte a [Política de Gerenciamento de Tokens](/policies/TOKEN_MANAGEMENT_POLICY.md).

---

## Comunicação

- **Incidentes críticos** devem ser comunicados imediatamente aos líderes técnicos da AbacatePay.
- Siga sempre uma postura de **responsible disclosure**.

---

## Referências

- [Política de Segurança](/policies/SECURITY_POLICY.md)
- [Política de Gerenciamento de Tokens](/policies/TOKEN_MANAGEMENT_POLICY.md)
- [Processo de Release](/maintainers/RELEASE_PROCESS.md)
- [Quality Gates de CI](/ci/QUALITY_GATES.md)
---

> A segurança é inegociável. Todo mantenedor deve estar atento e preparado para agir de forma rápida e responsável diante de qualquer incidente.