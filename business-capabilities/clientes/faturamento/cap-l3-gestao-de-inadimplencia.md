---
id: CAP-L3-028
name: "Gestão de Inadimplência"
type: "Business Capability"
subtype: "Level 3"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
strategicImportance: "tier2"
maturity: "Level 3 - Defined"
tags:
  - "Setor Elétrico"
  - "Nível 3"
  - "Engajamento com o Cliente"
  - "Faturamento e Cobrança"
  - "Data Agent (Conversational Analytics)"
---

# Gestão de Inadimplência (CAP-L3-028)

Esta capacidade técnica detalhada de Nível 3 faz parte do grupo funcional **Faturamento e Cobrança** sob a área principal de **Engajamento com o Cliente** no Mapa de Capacidades do Setor de Energia.

---

## 1. Descrição Geral da Capacidade
A capacidade **Gestão de Inadimplência** rege o controle e a operação das atividades granulares de utilities relacionadas ao seu escopo. No contexto do setor elétrico brasileiro, ela é fundamental para a transição para uma rede mais conectada, sustentável e eficiente, alinhada com as macrotendências de Descarbonização, Descentralização e Digitalização (3Ds).

---

## 2. Orquestração da Inteligência Artificial

Para automatizar e elevar o nível de maturidade desta capacidade, sugere-se a implantação de uma solução baseada em agentes inteligentes, conforme especificado abaixo:

*   **Agente Sugerido:** Dunning Communication & Credit Scorer Agent
*   **Classificação Arquitetural:** Data Agent (Conversational Analytics)
*   **Papel Operacional & Integrações:** Avalia riscos de crédito de clientes em atraso e gera réguas inteligentes de cobrança com ajuste automático de tom comercial.

---

## 3. Especificação de Dados e Governança

A integridade e confiabilidade da operação dependem de barramentos de dados governados estruturados na nuvem (Data Lakehouse corporativo):

*   **Inputs e Base de Conhecimento Requeridos:** Histórico de Atrasos de Pagamento, Perfil de Risco de Crédito do Cliente, Réguas de Cobrança.
*   **Saída Esperada do Processo:** Scripts de Cobrança com Ajuste de Tom Emocional, Priorização de Clientes para Cobrança.

---

## 4. Relações no Metamodelo SAP LeanIX v4

Como elemento integrante da arquitetura corporativa da PowerUp, esta capacidade mantém as seguintes associações estáveis:

*   **Parent Capability (Nível 2):** [/business-capabilities/engajamento-com-o-cliente/faturamento-e-cobranca/index.md](Faturamento e Cobrança)
*   **Parent Capability (Nível 1):** [/business-capabilities/engajamento-com-o-cliente/index.md](Engajamento com o Cliente)
*   **Supported by (Applications):** [/applications/dunning-communication-credit-scorer-agent.md](Dunning Communication & Credit Scorer Agent)
*   **Associated Data Objects:** [/data-objects/historico-de-atrasos-de-pagamento.md](Histórico de Atrasos de Pagamento, Perfil de Risco de Crédito do Cliente, Réguas de Cobrança.)
*   **Importance Heatmap:** `tier2` (Differentiation (excellence to compete and differentiate))
*   **Current Maturity:** `Level 3 - Defined`

---

## 5. Citações e Referências Regulatórias
1. [Regulações ANEEL e Procedimentos de Rede ONS](https://www.aneel.gov.br/) - Padrões de conformidade técnica e operacional exigidos para a operação coordenada do sistema elétrico nacional.
2. [SAP LeanIX Best Practice Reference Model](https://www.leanix.net/) - Framework estrutural para modelagem e mapeamento de capacidades de Utilities.
