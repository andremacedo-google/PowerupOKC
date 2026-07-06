---
id: AP-008
name: "MDM - Gestão de Dados de Medição"
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
  - "Clientes"
  - "Medidores"
  - "VEE"
  - "LeanIX-v4"
---

# MDM - Gestão de Dados de Medição (ID: AP-008)

O **Meter Data Management (MDM)** atua como o repositório centralizado síncrono para ingestão, governança e tratamento analítico de grandes volumes de medição de dados elétricos de campo [363].

## 1. Escopo Técnico e de Negócio
O MDM é um componente essencial na transição para redes inteligentes (Smart Grids). Ele não se comunica com os medidores em campo diretamente, mas ingere os dados brutos de sistemas de cabeceira (*Head-End Systems - HES*) [372]. Ele executa o processo de **VEE (Validação, Edição e Estimativa)**, que valida a qualidade da curva de carga do cliente, limpando lacunas, corrigindo picos de medição e sinalizando anomalias fiscais antes que as séries refinadas alimentem o faturamento [367].

## 2. Integrações e Fluxo de Dados (Data Objects)
*   **Inputs (Dados de Entrada):**
    *   `DO-001 Leituras de Telemetria (AMI)`: Dados brutos de injeção e consumo de medidores síncronos inteligentes [376].
*   **Outputs (Dados de Saída):**
    *   `DO-001 Leituras de Telemetria (AMI - Validadas)`: Série de dados de consumo finalizada ("faturável") que é disponibilizada ao sistema CIS para faturamento [367].
    *   `DO-011 Tickets e Ouvidoria`: Criação automática de ordens de serviço de fiscalização de perdas elétricas para o sistema WFM de campo caso detecte violações físicas do medidor [368].

## 3. Capacidades de Negócio Suportadas
*   `cap-l3-medicao-e-coleta-de-dados` [338]
*   `cap-l3-gestao-de-perdas` [338]

## 4. Exemplos de Soluções e Tecnologias de Mercado
*   **Oracle Utilities Meter Data Management (MDM)**: Líder de mercado especializado no tratamento analítico estruturado de grandes bases de medição elétricas [363].
*   **Siemens EnergyIP**: Plataforma global de IoT e processamento analítico para redes e dados inteligentes.

## 5. Práticas de Governança e FinOps
*   Como hospeda bilhões de leituras de série temporais (ex: leituras de 15 em 15 minutos), o arquiteto deve desenhar estratégias rígidas de particionamento e retenção de dados (data tiering) para conter os custos exponenciais de armazenamento em nuvem de FinOps.
