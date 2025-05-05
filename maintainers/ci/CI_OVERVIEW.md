
# Visão Geral de CI/CD - AbacatePay SDKs

A automação é um pilar fundamental para garantir a qualidade, segurança e consistência dos SDKs open source da AbacatePay.  
Todos os repositórios devem possuir pipelines de **CI/CD** configurados desde o início do desenvolvimento.

---

## Boas Práticas com Tokens e Secrets no CI/CD

- Utilize **GitHub Secrets** para armazenar qualquer credencial sensível necessária nos workflows.
- **Nunca** exponha tokens ou chaves diretamente nos arquivos de configuração `.yml`.
- Habilite o **Secret Scanning** do GitHub para detectar exposições acidentais.
- Siga rigorosamente a [Política de Gerenciamento de Tokens](/policies/TOKEN_MANAGEMENT_POLICY.md) ao configurar seus pipelines.

## Ferramenta Oficial

- Utilizamos **GitHub Actions** como padrão para todos os SDKs.
- Workflows devem ser claros, objetivos e seguir os templates definidos neste repositório central.

---

## Etapas Obrigatórias no Pipeline

1. **Lint e Análise Estática**
   - Validação de estilo e padrões de código conforme a linguagem.

2. **Execução de Testes**
   - Testes unitários e de integração, com cobertura mínima definida em [QUALITY_GATES.md](/ci/QUALITY_GATES.md).

3. **Build**
   - Quando aplicável, garantir que o SDK seja compilado/empacotado corretamente.

4. **Validações de Segurança**
   - Integração com ferramentas como **Dependabot** e scanners de vulnerabilidades.

5. **Verificação de Versionamento**
   - Garantir conformidade com a [Política de Versionamento](/maintainers/VERSIONING.md).

---

## Política de PRs

- Nenhum Pull Request deve ser aprovado ou mergeado com falhas no pipeline de CI.
- Workflows devem ser acionados em:
  - Push nas branches principais.
  - Abertura e atualização de PRs.
  - Releases.

---

## Reuso de Workflows

- Sempre que possível, utilize os exemplos disponíveis em [GITHUB_WORKFLOW_TEMPLATES](/ci/GITHUB_WORKFLOW_TEMPLATES/).
- Adaptar os templates conforme a stack da linguagem, mantendo a base padronizada.

---

## Monitoramento e Manutenção

- Revise periodicamente os pipelines.
- Mantenha actions e dependências atualizadas para evitar vulnerabilidades.
- Integre o **Dependabot** para automação dessas atualizações.

---

## Referências

- [Quality Gates](/ci/QUALITY_GATES.md)
- [Processo de Release](/maintainers/RELEASE_PROCESS.md)
- [Política de Segurança](/policies/SECURITY_POLICY.md)
- [Política de Gerenciamento de Tokens](/policies/TOKEN_MANAGEMENT_POLICY.md)

---

> Um pipeline bem estruturado é a primeira linha de defesa para garantir a qualidade dos nossos SDKs open source.