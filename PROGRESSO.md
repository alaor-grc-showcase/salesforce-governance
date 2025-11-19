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