---
id: "BC-TRADING-ENERGIA-GEST-RISCO"
name: "Trading de Energia e Gestão de Risco"
type: "Business Capability"
subtype: "Level 2"
parent: "Operações de Energia"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
strategicImportance: "tier1"
maturity: "Level 3 - Defined"
tags:
  - "Operacoes"
  - "Trading"
  - "Mercado Livre"
  - "PLD"
  - "Hedge"
  - "LeanIX-v4"
---

# Especificação Técnica: Trading de Energia e Gestão de Risco (ID: BC-TRADING-ENERGIA-GEST-RISCO)

Esta Business Capability de Nível 2 pertence ao domínio principal de **Operações de Energia** no ecossistema de Enterprise Architecture da companhia. Ela representa o conjunto de habilidades, competências de pessoas, ferramentas de tecnologia e modelagens de dados corporativos necessários para governar de forma ótima esta frente de trabalho específica do setor de energia.

## 1. Sub-capacidades de Nível 3 Associadas
De acordo com a taxonomia padronizada e o Mapa de Capacidades de Negócio, este grupo gerencial decompõe-se nas seguintes habilidades e atividades operacionais de Nível 3:

*   **Análise de Mercado de Energia:** Estuda modelos climáticos de bacias hidrográficas, afluências (ENA) e predições de sol/vento para a precificação de contratos de energia.
*   **Negociação de Contratos (Spot e Futuros):** Executa a compra e venda síncrona de lotes de energia (MWh) em pregões eletrônicos e através de PPAs bilaterais estruturados.
*   **Gestão de Risco de Preço e Volatilidade:** Aplica modelos e ferramentas financeiras (VaR, Monte Carlo) para criar estratégias de hedge para mitigar a volatilidade do PLD na CCEE.

## 2. Agentes de Inteligência Artificial Habilitados
Esta capacidade de negócio é modernizada no Gemini Enterprise através dos seguintes agentes de IA especializados que atuam no refinamento ou automação de suas tarefas:

*   **Previsor de PLD e Oferta de Energia (Data Agent (Conversational Analytics)):** Processa dados meteorológicos, de bacias hidrográficas e preços da CCEE/ONS para estimar a formação do PLD.
*   **Estrategista de Contratos de Energia Livre (No-code (Agent Designer)):** Auxilia na elaboração de propostas comerciais de contratos bilaterais e atua como playbook consultivo de negociação comercial.
*   **Simulador de Risco e Portfólio de Hedge (Data Agent (Conversational Analytics)):** Realiza análises complexas de Value at Risk (VaR) e simulações de estresse de volatilidade para proteger o portfólio de trading.

## 3. Relações no Metamodelo LeanIX (Fact Sheets Relacionados)
*   **Supports (Apoia):** Maximização de margens de faturamento em trading comercial de MWh, proteção contra riscos de inadimplência de contrapartes de energia, e acurácia estatística das projeções de receita comercial.
*   **Supported by (Suportado por):** Sistemas de ETRM (Energy Trading and Risk Management), Modelos de Simulação Climática/Econômica (NEWAVE/DECOMP/DESSEM), Portais da CCEE e ONS.
*   **Data Objects (Objetos de Dados) Associados:** Leituras de telemetria, relatórios de faturamento, dados cadastrais mestre e bases documentais síncronas.

## 4. Avaliação de Maturidade e Importância Estratégica (Heatmap)
*   **Importância Estratégica (Business Importance):** `tier1` (Mapeado no heatmap corporativo para priorização de recursos e investimentos em modernização tecnológica).
*   **Maturidade Atual (As-Is Maturity):** `Level 3 - Defined` (Escala de maturidade avaliada periodicamente para identificar gaps organizacionais ou de infraestrutura tecnológica).
*   **Diretriz de Roadmap de TI:** Os investimentos de tecnologia devem focar na capacitação contínua das squads, integração ágil via APIs modernas, e na adoção de agentes inteligentes baseados no motor do **Gemini 3.5** para eliminação de gargalos manuais síncronos de alta frequência.
