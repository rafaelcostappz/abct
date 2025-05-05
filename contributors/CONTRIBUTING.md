# Guia Geral de Contribuição

Obrigado por querer contribuir com os SDKs **open source** da AbacatePay!  
Este guia explica como colaborar de forma eficiente e alinhada com nossos padrões.

---

## Antes de Começar

Os SDKs da AbacatePay são projetos **open source**, mantidos com rigor para garantir qualidade, segurança e consistência.

**É obrigatório abrir uma Issue antes de qualquer Pull Request**, salvo para correções extremamente simples (ex: erros de digitação).

- Utilize a Issue para descrever sua proposta e alinhar com os mantenedores.
- Não inicie o desenvolvimento antes da aprovação ou feedback da Issue aberta.
- Esse processo garante que sua contribuição esteja alinhada com o roadmap oficial e evita retrabalho.

Consulte também o nosso [Fluxo de Desenvolvimento](/contributors/DEVELOPMENT_WORKFLOW.md) para entender como organizamos branches, revisões e releases.

---

## Atenção: Segurança de Tokens e Credenciais

- **Nunca** inclua tokens, chaves de API, senhas ou qualquer credencial em commits, Pull Requests ou arquivos versionados.
- Utilize variáveis de ambiente e siga as orientações da nossa [Política de Gerenciamento de Tokens](/policies/TOKEN_MANAGEMENT_POLICY.md).
- Caso identifique exposição acidental, reporte imediatamente conforme nossa [Política de Segurança](/policies/SECURITY_POLICY.md).

---

## Como Contribuir

1. Realize o fork do repositório do SDK desejado.
2. **Abra uma Issue obrigatória** detalhando sua proposta ou correção.
3. Após validação da Issue, crie uma branch nomeada de forma descritiva:
   ```
   git checkout -b feat/nome-da-sua-feature
   ```
4. Siga rigorosamente:
   - [Guia de Commits](/contributors/COMMIT_GUIDELINES.md)
   - [Padrões de Código](/contributors/CODING_STANDARDS.md)
   - [Diretrizes de Documentação](/templates/DOCUMENTATION_STRUCTURE.md)
   - [Guia de Testes](/contributors/TESTING_GUIDELINES.md)
5. Antes de submeter o PR, siga as instruções do [Fluxo de Desenvolvimento](/contributors/DEVELOPMENT_WORKFLOW.md), incluindo:
   - Manter a branch atualizada com `develop` ou `main`
   - Executar `npm install` (ou equivalente) antes de qualquer desenvolvimento
6. Ao finalizar, abra o Pull Request utilizando o [Template de PR](/contributors/PULL_REQUEST_TEMPLATE.md) e seguindo o [Guia de Pull Request](/contributors/DEVELOPMENT_WORKFLOW.md), sempre referenciando a Issue correspondente.

---

## O que Esperamos

- Commits claros, objetivos e padronizados.
- Código limpo, validado por ferramentas de lint e com cobertura de testes adequada.
- Documentação atualizada sempre que necessário.
- Pull Requests bem descritos, organizados e vinculados à Issue.
- Respeito aos processos de revisão e ao feedback dos mantenedores.
- Conformidade com nossos [Quality Gates](/ci/QUALITY_GATES.md).

---

## O que Evitar

- Iniciar Pull Requests sem a devida Issue aprovada.
- Submeter PRs genéricos ou que envolvam múltiplas alterações sem relação direta.
- Utilizar mensagens de commit vagas como "ajustes", "update", "alterações".
- Ignorar falhas no pipeline de CI/CD.
- Desconsiderar padrões estabelecidos de código, testes e documentação.
- **Nunca expor tokens ou credenciais em commits!**

---

## Código de Conduta

Todos os colaboradores devem seguir o nosso [Código de Conduta](/contributors/CODE_OF_CONDUCT.md).  
Ambiente respeitoso e colaborativo é fundamental.

---

## Dúvidas ou Sugestões

Caso tenha dúvidas sobre o processo ou queira discutir uma ideia, abra uma Issue para alinhamento prévio.  
Os mantenedores estão disponíveis para orientar e garantir que sua contribuição agregue da melhor forma possível.

Agradecemos por colaborar com o ecossistema **open source** da AbacatePay.
