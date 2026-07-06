---
id: AP-007
name: "CIS - Sistema de Faturamento e Informações Comerciais"
type: "Application"
subtype: "Business Application"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
businessCriticality: "Mission Critical"
functionalSuitability: "Adequate"
technicalSuitability: "Excellent"
tags:
  - "Setor Elétrico"
  - "Clientes"
  - "Faturamento"
  - "IS-U"
  - "LeanIX-v4"
---

# CIS - Sistema de Faturamento e Informações Comerciais (ID: AP-007)

O **Customer Information System (CIS)** é o sistema transacional core responsável pelo cálculo tarifário complexo, processamento das contas de energia dos consumidores e compensação financeira.

## 1. Escopo Técnico e de Negócio
No setor elétrico, o CIS é o coração do fluxo financeiro de faturamento. Ele parametriza as complexas estruturas tarifárias reguladas pela ANEEL, compostas por componentes como **TE (Tarifa de Energia)** e **TUSD (Tarifa de Uso do Sistema de Distribuição)**, incluindo bandeiras tarifárias e impostos federais/estaduais [389]. Ele realiza o faturamento do prossumidor (Geração Distribuída), liquidando créditos de energia de forma automatizada no faturamento mensal.

## 2. Integrações e Fluxo de Dados (Data Objects)
*   **Inputs (Dados de Entrada):**
    *   `DO-001 Leituras de Telemetria (AMI)`: Ingestão de medições consolidadas e purificadas enviadas pelo sistema MDM de medição [367].
    *   `DO-008 Cadastro de Prossumidor`: Configuração de dados de potência de geração para regras de compensação.
*   **Outputs (Dados de Saída):**
    *   `DO-010 Fatura de Energia (CIS)`: Emissão da conta contendo os dados fiscais e o saldo de créditos atualizados que alimenta o ERP [335].

## 3. Capacidades de Negócio Suportadas
*   `cap-l3-processamento-de-faturas` [338]
*   `cap-l3-gestao-de-inadimplencia` [338]

## 4. Exemplos de Soluções e Tecnologias de Mercado
*   **SAP Utilities (IS-U)**: Plataforma líder em concessionárias brasileiras para o faturamento transacional de energia complexa de alto volume de dados [331].
*   **Oracle Utilities Customer Cloud Service (CCS)**: Solução modular unificada baseada em arquiteturas em nuvem modernas para faturamento elétrico [334].

## 5. Práticas de Governança e FinOps
*   **Racionalização de Consultas:** O faturamento envolve o processamento em lote (batch billing) de milhões de instalações simultaneamente. O monitoramento de desempenho de banco de dados deve assegurar que consultas massivas ocorram em janelas de menor carga (ex: fins de semana) para controlar custos computacionais de FinOps.
