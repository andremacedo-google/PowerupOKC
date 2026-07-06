---
id: AP-002
name: "ERP - Gestão de Tesouraria e Riscos Financeiros"
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
  - "Tesouraria"
  - "Hedge"
  - "LeanIX-v4"
---

# ERP - Gestão de Tesouraria e Riscos Financeiros (ID: AP-002)

Esta aplicação gerencia as posições de liquidez, fluxo de caixa projetado, operações de financiamento, captação de dívidas e operações de derivativos para proteção cambial e de preços de energia (hedge).

## 1. Escopo Técnico e de Negócio
No setor elétrico brasileiro, a volatilidade de curto prazo do preço PLD (CCEE) e o risco de crédito de contrapartes exigem uma tesouraria especializada. Esta aplicação monitora os saldos bancários, os fluxos de caixa corporativos de curto e longo prazo e calcula a marcação a mercado (MtM) e o valor em risco (Value at Risk - VaR) de contratos de longo prazo (PPAs) bilaterais da comercializadora.

## 2. Integrações e Fluxo de Dados (Data Objects)
*   **Inputs (Dados de Entrada):**
    *   `DO-010 Fatura de Energia (CIS)`: Para consolidação de previsões de entrada de caixa provenientes de arrecadação.
    *   `DO-005 Preço de Liquidação (PLD)`: Dados de preços horários reais e futuros publicados pela CCEE para cálculo de exposição.
*   **Outputs (Dados de Saída):**
    *   `DO-012 Lançamentos Contábeis`: Movimentações de fluxo de caixa projetado, conciliações bancárias e lançamentos de juros/amortizações de dívidas para o razão contábil.

## 3. Capacidades de Negócio Suportadas
Este sistema suporta diretamente as seguintes capacidades do mapa:
*   `cap-l3-gestao-de-tesouraria` [338]
*   `cap-l3-gestao-de-risco-de-preco` [338]

## 4. Exemplos de Soluções e Tecnologias de Mercado
*   **SAP S/4HANA (TRM - Treasury and Risk Management)**: Solução integrada para hedging e tesouraria complexa [338].
*   **Kyriba Cash Management**: Solução especializada SaaS em nuvem para orquestração de liquidez.

## 5. Práticas de Governança e FinOps
*   A governança exige auditoria contínua de limites de alçada para liberação de pagamentos e aprovação de derivativos financeiros de energia, integrada com políticas de conformidade do SOX (Sarbanes-Oxley).
