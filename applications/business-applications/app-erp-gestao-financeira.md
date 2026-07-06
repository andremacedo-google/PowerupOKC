---
id: AP-001
name: "ERP - Gestão Financeira, Contábil e Controladoria"
type: "Application"
subtype: "Business Application"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
businessCriticality: "Mission Critical"
functionalSuitability: "Excellent"
technicalSuitability: "Excellent"
tags:
  - "Setor Elétrico"
  - "Corporativo"
  - "Finanças"
  - "S4HANA"
  - "LeanIX-v4"
---

# ERP - Gestão Financeira, Contábil e Controladoria (ID: AP-001)

Este Fact Sheet descreve a aplicação de **Enterprise Resource Planning (ERP)** focada em processos contábeis, tributários e de controladoria aplicados ao setor elétrico. Ele atua como o sistema de registro central unificado das transações financeiras corporativas.

## 1. Escopo Técnico e de Negócio
No contexto do setor de energia, o ERP gerencia a contabilidade societária, a apuração tributária (ICMS, PIS/COFINS sob as regras tarifárias), a contabilidade de custos por centro de responsabilidade e o controle de investimentos de capital (CAPEX). Ele suporta a apropriação de despesas, fechamentos contábeis mensais e consolidação de relatórios financeiros exigidos pela ANEEL.

## 2. Integrações e Fluxo de Dados (Data Objects)
Como sistema central de registro corporativo, o ERP realiza o seguinte mapeamento do barramento de dados:

*   **Inputs (Dados de Entrada):**
    *   `DO-010 Fatura de Energia (CIS)`: Para reconciliação de contas a receber e faturamentos consolidados de clientes livres e cativos.
    *   `DO-012 Lançamentos Contábeis`: Origem de notas fiscais de fornecedores de MRO e materiais de campo via contas a pagar.
*   **Outputs (Dados de Saída):**
    *   `DO-012 Lançamentos Contábeis (ACDOCA)`: Balancetes de verificação, fluxo de caixa realizado e razão contábil consolidado enviado para a diretoria.

## 3. Capacidades de Negócio Suportadas
Este sistema é o principal habilitador tecnológico das seguintes capacidades de Nível 3:
*   `cap-l3-contabilidade-e-fechamento-financeiro` [338]
*   `cap-l3-planejamento-do-ciclo-de-vida-dos-ativos` [338]

## 4. Exemplos de Soluções e Tecnologias de Mercado
*   **SAP S/4HANA (FI/CO/PPM)**: Padrão líder no setor elétrico nacional para o fechamento contábil e controladoria [338].
*   **Oracle ERP Cloud (Financials)**: Solução corporativa alternativa de alta adoção.

## 5. Práticas de Governança e FinOps
*   **Controle de Licenças:** O licenciamento é baseado em usuários nomeados ativos e volume de transações financeiras.
*   **FinOps:** O monitoramento de custos de infraestrutura contábil deve separar as transações de alto volume (como conciliação de faturamento) das transações administrativas comuns para otimização de consultas de banco de dados (HANA memory usage).
