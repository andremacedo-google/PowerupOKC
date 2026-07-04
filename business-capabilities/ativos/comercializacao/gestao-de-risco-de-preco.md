---
id: CAP-L3-040
name: "Gestão de Risco de Preço"
type: "Business Capability"
subtype: "Level 3"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
strategicImportance: "tier1"
maturity: "Level 3 - Defined"
tags:
  - "Setor Elétrico"
  - "Nível 3"
  - "Operações de Energia"
  - "Trading de Energia e Gestão de Risco"
  - "Data Agent (Conversational Analytics)"
---

# Gestão de Risco de Preço (CAP-L3-040)

Esta capacidade técnica detalhada de Nível 3 faz parte do grupo funcional **Trading de Energia e Gestão de Risco** sob a área principal de **Operações de Energia** no Mapa de Capacidades do Setor de Energia.

---

## 1. Descrição Geral da Capacidade
A capacidade **Gestão de Risco de Preço** rege o controle e a operação das atividades granulares de utilities relacionadas ao seu escopo. No contexto do setor elétrico brasileiro, ela é fundamental para a transição para uma rede mais conectada, sustentável e eficiente, alinhada com as macrotendências de Descarbonização, Descentralização e Digitalização (3Ds).

---

## 2. Orquestração da Inteligência Artificial

Para automatizar e elevar o nível de maturidade desta capacidade, sugere-se a implantação de uma solução baseada em agentes inteligentes, conforme especificado abaixo:

*   **Agente Sugerido:** Simulador de Risco e Portfólio de Hedge
*   **Classificação Arquitetural:** Data Agent (Conversational Analytics)
*   **Papel Operacional & Integrações:** Realiza análises complexas de Value at Risk (VaR) e simulações de estresse de volatilidade para proteger o portfólio de trading.

---

## 3. Especificação de Dados e Governança

A integridade e confiabilidade da operação dependem de barramentos de dados governados estruturados na nuvem (Data Lakehouse corporativo):

*   **Inputs e Base de Conhecimento Requeridos:** Posições de Contratos Bilaterais, Volatilidade Histórica do PLD, Preços Futuros do Mercado.
*   **Saída Esperada do Processo:** Simulações de Estresse de Volatilidade de Portfólio, Cálculo de Value at Risk (VaR).

---

## 4. Relações no Metamodelo SAP LeanIX v4

Como elemento integrante da arquitetura corporativa da PowerUp, esta capacidade mantém as seguintes associações estáveis:

*   **Parent Capability (Nível 2):** [/business-capabilities/operacoes-de-energia/trading-de-energia-e-gestao-de-risco/index.md](Trading de Energia e Gestão de Risco)
*   **Parent Capability (Nível 1):** [/business-capabilities/operacoes-de-energia/index.md](Operações de Energia)
*   **Supported by (Applications):** [/applications/simulador-de-risco-e-portfolio-de-hedge.md](Simulador de Risco e Portfólio de Hedge)
*   **Associated Data Objects:** [/data-objects/posicoes-de-contratos-bilaterais.md](Posições de Contratos Bilaterais, Volatilidade Histórica do PLD, Preços Futuros do Mercado.)
*   **Importance Heatmap:** `tier1` (Innovation (critical to competitive advantage))
*   **Current Maturity:** `Level 3 - Defined`

---

## 5. Citações e Referências Regulatórias
1. [Regulações ANEEL e Procedimentos de Rede ONS](https://www.aneel.gov.br/) - Padrões de conformidade técnica e operacional exigidos para a operação coordenada do sistema elétrico nacional.
2. [SAP LeanIX Best Practice Reference Model](https://www.leanix.net/) - Framework estrutural para modelagem e mapeamento de capacidades de Utilities.
