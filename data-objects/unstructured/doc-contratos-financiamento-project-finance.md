---
id: DO-221
name: "Contratos de Financiamento (Project Finance)"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Confidencial"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Não Estruturado"
  - "LeanIX-v4"
---

# Contratos de Financiamento (Project Finance) (DO-221)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança da base de conhecimento não estruturada **Contratos de Financiamento (Project Finance)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Contratos financeiros complexos celebrados por Sociedades de Propósito Específico (SPE) para captação de recursos de grandes projetos de usinas ou linhas de transmissão.

Este objeto de dados não estruturado é de extrema importância para as regras de conformidade regulatória (conforme as diretrizes de regulação tarifária, fiscalização ou as instruções operacionais do SIN). Sua correta catalogação impede silos de conhecimento e vazamentos de informações classificadas.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade, linhagem e governança de dados no repositório corporativo da PowerUp, este Data Object mantém as seguintes conexões estáveis:

*   **Subdomínio de Dados (Nível 1):** Jurídico e Contratual / Contratos Estratégicos
*   **Sistemas e Aplicações Relacionadas (Applications):** SAP CLM, Tesouraria, Controladoria, PMO (Projetos)
*   **Repositório/Sistema de Registro Canônico (System of Truth):** Arquivo Contratual do Sindicato de Bancos / SAP CLM
*   **Capacidade de Negócio Relacionada:** Gestão de Tesouraria, Execução de Projetos de Capital, Risco e Captação
*   **Documento de Referência (Mestre):** nao

## # Schema

Este ativo de dados não estruturados de referência é composto e regido pelos seguintes temas críticos e tipos de informações:

*   **Informações Críticas e Conteúdo Típico:** Condições precedentes (Conditions Precedent) para desembolsos, covenants financeiros (como DSCR mínimo), garantias fiduciárias (cessão de receitas do PPA, penhor de ações), step-in rights.
*   **Classificação de Privacidade e Sensibilidade (Compliance/LGPD):** Confidencial

## # Examples

Abaixo está exemplificado um rascunho de metadados em formato estruturado representando o objeto documental, indicando as variáveis comumente contidas em seu fluxo de indexação:

```json
{"project_finance_uhe": {"spe_nome": "PowerUp Rio Grande S.A.", "credor_lider": "BNDES", "covenant_dscr": "Debt Service Coverage Ratio mínimo de 1.25x", "contas_reserva": ["Conta Reserva do Serviço da Dívida", "Conta de Centralização de Receitas"]}}
```

## # Citations

1. [Manual de Governança de Informações Não Estruturadas PowerupOKC] - Rege os padrões de indexação, controle e privacidade das bases de conhecimento setoriais.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
