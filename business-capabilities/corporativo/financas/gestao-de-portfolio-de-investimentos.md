---
id: CAP-L3-002
name: "Gestão de Portfólio de Investimentos"
type: "Business Capability"
subtype: "Level 3"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
strategicImportance: "parity"
maturity: "Level 4 - Managed"
tags:
  - "Setor Elétrico"
  - "Nível 3"
  - "Corporativo e Suporte ao Negócio"
  - "Gestão Estratégica e Financeira"
  - "Data Agent (Conversational Analytics)"
---

# Gestão de Portfólio de Investimentos (CAP-L3-002)

Esta capacidade técnica detalhada de Nível 3 faz parte do grupo funcional **Gestão Estratégica e Financeira** sob a área principal de **Corporativo e Suporte ao Negócio** no Mapa de Capacidades do Setor de Energia.

---

## 1. Descrição Geral da Capacidade
A capacidade **Gestão de Portfólio de Investimentos** rege o controle e a operação das atividades granulares de utilities relacionadas ao seu escopo. No contexto do setor elétrico brasileiro, ela é fundamental para a transição para uma rede mais conectada, sustentável e eficiente, alinhada com as macrotendências de Descarbonização, Descentralização e Digitalização (3Ds).

---

## 2. Orquestração da Inteligência Artificial

Para automatizar e elevar o nível de maturidade desta capacidade, sugere-se a implantação de uma solução baseada em agentes inteligentes, conforme especificado abaixo:

*   **Agente Sugerido:** Modelador de Cenários e Portfólio CAPEX
*   **Classificação Arquitetural:** Data Agent (Conversational Analytics)
*   **Papel Operacional & Integrações:** Analisa a viabilidade econômica, projeta LCOE e simula o retorno de investimentos em novos ativos e na modernização do portfólio.

---

## 3. Especificação de Dados e Governança

A integridade e confiabilidade da operação dependem de barramentos de dados governados estruturados na nuvem (Data Lakehouse corporativo):

*   **Inputs e Base de Conhecimento Requeridos:** Projetos de CAPEX, Modelos Financeiros de Projetos, Taxas de Desconto (WACC), Estimativas de LCOE.
*   **Saída Esperada do Processo:** Simulações de Fluxo de Caixa Descontado (DCF), Ranking de Rentabilidade (VPL, TIR) de Ativos.

---

## 4. Relações no Metamodelo SAP LeanIX v4

Como elemento integrante da arquitetura corporativa da PowerUp, esta capacidade mantém as seguintes associações estáveis:

*   **Parent Capability (Nível 2):** [/business-capabilities/corporativo-e-suporte-ao-negocio/gestao-estrategica-e-financeira/index.md](Gestão Estratégica e Financeira)
*   **Parent Capability (Nível 1):** [/business-capabilities/corporativo-e-suporte-ao-negocio/index.md](Corporativo e Suporte ao Negócio)
*   **Supported by (Applications):** [/applications/modelador-de-cenarios-e-portfolio-capex.md](Modelador de Cenários e Portfólio CAPEX)
*   **Associated Data Objects:** [/data-objects/projetos-de-capex.md](Projetos de CAPEX, Modelos Financeiros de Projetos, Taxas de Desconto (WACC), Estimativas de LCOE.)
*   **Importance Heatmap:** `parity` (Commodity (operational needs, maintaining baseline parity))
*   **Current Maturity:** `Level 4 - Managed`

---

## 5. Citações e Referências Regulatórias
1. [Regulações ANEEL e Procedimentos de Rede ONS](https://www.aneel.gov.br/) - Padrões de conformidade técnica e operacional exigidos para a operação coordenada do sistema elétrico nacional.
2. [SAP LeanIX Best Practice Reference Model](https://www.leanix.net/) - Framework estrutural para modelagem e mapeamento de capacidades de Utilities.
