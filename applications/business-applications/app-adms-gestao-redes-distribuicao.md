---
id: AP-009
name: "ADMS / OMS - Gestão de Redes de Distribuição"
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
  - "Operações"
  - "Distribuição"
  - "SCADA"
  - "LeanIX-v4"
---

# ADMS / OMS - Gestão de Redes de Distribuição (ID: AP-009)

O **Advanced Distribution Management System (ADMS)** é o sistema core de Tecnologia da Operação (TO) que orquestra a supervisão, controle e resiliência da rede física de média e baixa tensão da distribuidora [411].

## 1. Escopo Técnico e de Negócio
O ADMS unifica as funcionalidades de SCADA de distribuição (controle de chaves e religadores), DMS (análises e cálculos elétricos de topologia) e OMS (gerenciamento de interrupções de energia) [337]. Ele executa automações de redes inteligentes de alta criticidade operacional, como o algoritmo **FLISR (Fault Location, Isolation, and Service Restoration)**, que isola de forma autônoma trechos em curto-circuito e restaura a energia em áreas sãs em milissegundos [337].

## 2. Integrações e Fluxo de Dados (Data Objects)
*   **Inputs (Dados de Entrada):**
    *   `DO-003 Status e Alarmes (SCADA)`: Coleta em tempo real de posições de equipamentos e proteções no campo [411].
    *   `DO-002 Cadastro de Rede (GIS)`: Modelo georreferenciado mestre para renderização da topologia unifilar exata da rede operada [411].
*   **Outputs (Dados de Saída):**
    *   `DO-011 Tickets e Ouvidoria (Outage)`: Geração e envio síncrono de notificações de falta de energia (Outages) coletivas integradas ao sistema de CRM de atendimento de clientes [337].
    *   `DO-017 Logs de Acesso e SOC (Eventos)`: Histórico de manobras de chaveamento integrados de forma síncrona ao módulo de manutenção SAP PM para atualização de ciclos de ativos [337].

## 3. Capacidades de Negócio Suportadas
*   `cap-l3-operacao-da-rede-de-distribuicao` [338]
*   `cap-l3-manutencao-de-redes-e-equipamentos` [338]

## 4. Exemplos de Soluções e Tecnologias de Mercado
*   **Siemens ADMS (Spectrum Power 7)**: Solução global de ponta para operação física digital integrada de média e baixa tensão elétricas [337].
*   **Schneider Electric EcoStruxure ADMS**: Líder mundial em inteligência analítica de TO aplicadas a redes Smart Grids.

## 5. Práticas de Governança e FinOps
*   Como infraestrutura crítica de segurança nacional de TO, o ADMS exige conformidade rigorosa com normas estritas de cibersegurança industrial (IEC 62443 e normas de isolamento de redes industriais da ANEEL).
