---
id: CAP-L3-015
name: "Compras Estratégicas (Procurement)"
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
  - "Gestão da Cadeia de Suprimentos"
  - "No-code (Agent Designer)"
---

# Compras Estratégicas (Procurement) (CAP-L3-015)

Esta capacidade técnica detalhada de Nível 3 faz parte do grupo funcional **Gestão da Cadeia de Suprimentos** sob a área principal de **Corporativo e Suporte ao Negócio** no Mapa de Capacidades do Setor de Energia.

---

## 1. Descrição Geral da Capacidade
A capacidade **Compras Estratégicas (Procurement)** rege o controle e a operação das atividades granulares de utilities relacionadas ao seu escopo. No contexto do setor elétrico brasileiro, ela é fundamental para a transição para uma rede mais conectada, sustentável e eficiente, alinhada com as macrotendências de Descarbonização, Descentralização e Digitalização (3Ds).

---

## 2. Orquestração da Inteligência Artificial

Para automatizar e elevar o nível de maturidade desta capacidade, sugere-se a implantação de uma solução baseada em agentes inteligentes, conforme especificado abaixo:

*   **Agente Sugerido:** RFx Builder & Sourcing Orchestrator
*   **Classificação Arquitetural:** No-code (Agent Designer)
*   **Papel Operacional & Integrações:** Digeere requisitos brutos de áreas técnicas para formular editais formais (RFP/RFQ) concorrencialmente neutros.

---

## 3. Especificação de Dados e Governança

A integridade e confiabilidade da operação dependem de barramentos de dados governados estruturados na nuvem (Data Lakehouse corporativo):

*   **Inputs e Base de Conhecimento Requeridos:** Memorial Descritivo Bruto, Requisições de Compras, Histórico de Licitações (RFx).
*   **Saída Esperada do Processo:** Editais de Licitação Estruturados (RFI/RFP/RFQ), Templates de Proposta Comercial e Scorecard.

---

## 4. Relações no Metamodelo SAP LeanIX v4

Como elemento integrante da arquitetura corporativa da PowerUp, esta capacidade mantém as seguintes associações estáveis:

*   **Parent Capability (Nível 2):** [/business-capabilities/corporativo-e-suporte-ao-negocio/gestao-da-cadeia-de-suprimentos/index.md](Gestão da Cadeia de Suprimentos)
*   **Parent Capability (Nível 1):** [/business-capabilities/corporativo-e-suporte-ao-negocio/index.md](Corporativo e Suporte ao Negócio)
*   **Supported by (Applications):** [/applications/rfx-builder-sourcing-orchestrator.md](RFx Builder & Sourcing Orchestrator)
*   **Associated Data Objects:** [/data-objects/memorial-descritivo-bruto.md](Memorial Descritivo Bruto, Requisições de Compras, Histórico de Licitações (RFx).)
*   **Importance Heatmap:** `parity` (Commodity (operational needs, maintaining baseline parity))
*   **Current Maturity:** `Level 4 - Managed`

---

## 5. Citações e Referências Regulatórias
1. [Regulações ANEEL e Procedimentos de Rede ONS](https://www.aneel.gov.br/) - Padrões de conformidade técnica e operacional exigidos para a operação coordenada do sistema elétrico nacional.
2. [SAP LeanIX Best Practice Reference Model](https://www.leanix.net/) - Framework estrutural para modelagem e mapeamento de capacidades de Utilities.
