# Log de Progresso - Projeto GRC Showcase

## Fase 1: Fundação e Segurança Local (Concluída ✅)

- [x] Criação da Organização `alaor-grc-showcase`.
- [x] Criação do Repositório `salesforce-governance` (Público, com Licença MIT).
- [x] Limpeza dos repositórios antigos do perfil.
- [x] Geração e configuração da Chave SSH (`Authentication Key`).
- [x] Geração e configuração da Chave GPG (`Signing Key`).
- [x] Teste final: Commit inicial com selo "Verified" enviado via SSH.

## Fase 2: Governança e Times (Concluída ✅)

- [x] Criação e descrição dos Times (`Developers`, `Approvers`, `Admin-PAM`, etc.).
- [x] Atribuição das permissões (`Roles`) dos Times ao repositório.
- [x] Criação das *Labels* personalizadas (Tipo, Status, Prioridade).
- [x] Configuração das Regras de Proteção da branch `main` (Ruleset).
- [x] Convidada conta secundária (`Developer`) para a organização.
- [x] **Teste de Validação:** Logado como `Developer`, o merge foi **bloqueado** (sucesso).
- [x] **Teste de Aprovação:** Logado como `Approver`, o PR foi revisado e mergeado.

## Fase 3: Integração de Identidade (Azure AD) (Pendente ⏸️)

> **Observação:** A implementação de SAML SSO depende de licenciamento GitHub Enterprise. A viabilidade técnica/financeira será analisada futuramente.

- [ ] Criar tenant no Microsoft Entra ID (Azure AD).
- [ ] Configurar SAML SSO na Organização GitHub.
- [ ] Vincular grupos do Azure AD aos times do GitHub (`Approvers`, `Developers`).
- [ ] Testar o fluxo de login via SSO.

## Fase 4: Automação e DevSecOps (Em Andamento ⏳)

- [ ] Ativar **Secret Scanning** e **Push Protection** (Segurança de Credenciais).
- [ ] Configurar **Code Scanning** com CodeQL (Análise Estática de Segurança).
- [ ] Criar pipeline de CI (`codeql.yml`) via Pull Request.
- [ ] **Teste de Segurança:** Verificar se o PR é escaneado automaticamente.
- [ ] Criar pipeline de CD (Simulação de Deploy) após merge na `main`.

## Fase 5: Documentação e Showcase (Pendente ⏸️)

- [ ] Criar pasta `docs/images` para evidências.
- [ ] Fazer upload dos prints de validação (Bloqueio, Aprovação, Scan).
- [ ] Escrever o `README.md` definitivo (Resumo, Fluxo, Tecnologias, Testes).
- [ ] Revisão final do Portfólio.