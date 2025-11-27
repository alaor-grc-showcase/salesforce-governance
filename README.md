# Salesforce Governance & DevSecOps Showcase

Este repositório demonstra a implementação de um fluxo de trabalho **DevSecOps** completo para o ecossistema Salesforce, focado em **Governança, Risco e Conformidade (GRC)**.

O projeto sai do tradicional deploy manual e estabelece uma esteira de automação segura, auditável e escalável, aplicando o **Princípio do Mínimo Privilégio**.

---

## 🚀 Funcionalidades e Governança

### 1. Governança e Controle de Acesso (GRC)
- **Segregação de Funções:** Papéis claros definidos via Times do GitHub (`Developers` vs `Approvers`).
- **Proteção de Branch (Rulesets):** A branch `main` é bloqueada para commits diretos.
- **Code Review Obrigatório:** Nenhum código sobe para produção sem a aprovação de um `Approver` (que não pode ser o autor do código).
- **Autenticação Forte:** Uso obrigatório de chaves **GPG** para assinatura de commits (Verificação de Autoria).

### 2. Segurança Automatizada (DevSecOps)
- **Secret Scanning:** Bloqueio automático de commits contendo senhas ou tokens expostos.
- **CodeQL (SAST):** Análise estática de código automática em cada Pull Request para detectar vulnerabilidades de segurança antes do merge.

### 3. Automação de Deploy (CI/CD)
- **Integração Contínua (CI):** Validação automática de PRs.
- **Entrega Contínua (CD):** Pipeline automatizado via **GitHub Actions** que realiza o deploy na Org Salesforce após o merge.
- **Autenticação JWT:** Conexão segura *Server-to-Server* usando Certificados Digitais (OpenSSL) e Connected App, eliminando o uso de senhas fixas no script.

---

## 🛠️ Arquitetura do Fluxo

```mermaid
graph TD;
    A["Developer"] -->|Commit Assinado GPG| B["Branch de Feature"];
    B -->|Pull Request| C{"Governança"};
    C -->|CodeQL Scan| D["Análise de Segurança"];
    C -->|Code Review| E["Aprovação Humana"];
    D -- Passou --> F;
    E -- Aprovou --> F["Merge na Main"];
    F -->|Dispara Action| G["GitHub Runner"];
    G -->|Autenticação JWT| H["Salesforce Org"];
    H -->|Deploy| I["Produção"];
'''

⚙️ Stack Tecnológica
Controle de Versão: Git & GitHub

Orquestração: GitHub Actions

Salesforce: Salesforce CLI (sf), Apex, Connected App

Segurança: OpenSSL (Certificados), GnuPG (Assinatura)

📜 Como foi construído (Log de Progresso)
Para ver o passo a passo detalhado da implementação deste projeto, consulte o arquivo PROGRESSO.md.
