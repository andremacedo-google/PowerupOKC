---
id: "BC-VENDAS-AQUISICAO-CLIENTES"
name: "Vendas e Aquisição de Clientes"
type: "Business Capability"
subtype: "Level 2"
parent: "Engajamento com o Cliente"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
strategicImportance: "tier2"
maturity: "Level 3 - Defined"
tags:
  - "Cliente"
  - "Vendas"
  - "Onboarding"
  - "Contratos"
  - "LeanIX-v4"
---

# Especificação Técnica: Vendas e Aquisição de Clientes (ID: BC-VENDAS-AQUISICAO-CLIENTES)

Esta Business Capability de Nível 2 pertence ao domínio principal de **Engajamento com o Cliente** no ecossistema de Enterprise Architecture da companhia. Ela representa o conjunto de habilidades, competências de pessoas, ferramentas de tecnologia e modelagens de dados corporativos necessários para governar de forma ótima esta frente de trabalho específica do setor de energia.

## 1. Sub-capacidades de Nível 3 Associadas
De acordo com a taxonomia padronizada e o Mapa de Capacidades de Negócio, este grupo gerencial decompõe-se nas seguintes habilidades e atividades operacionais de Nível 3:

*   **Gestão de Leads e Oportunidades:** Gerencia o funil de vendas, desde a qualificação técnica de um lead industrial B2B até o fechamento comercial no ACL.
*   **Contratação de Serviços:** Formaliza a contratação de fornecimento de energia (PPAs comerciais) e serviços associados, reduzindo atritos burocráticos.
*   **Onboarding de Clientes:** Simplifica e digitaliza o processo de adesão de novos clientes livres, validando a documentação e integrando-os aos sistemas comerciais.

## 2. Agentes de Inteligência Artificial Habilitados
Esta capacidade de negócio é modernizada no Gemini Enterprise através dos seguintes agentes de IA especializados que atuam no refinamento ou automação de suas tarefas:

*   **Lead Scoring & Funnel Velocity Agent (Data Agent (Conversational Analytics)):** Classifica leads do mercado livre de energia, priorizando contas industriais (B2B) baseado em potencial de faturamento e regras de negócio.
*   **Services Procurement & SOW Manager (No-code (Agent Designer)):** Apoia na redação de escopos técnicos, termos de referência e acordos de nível de serviço (SOW) para contratação de terceiros.
*   **Orquestrador de Onboarding Digital (No-code (Agent Designer)):** Auxilia na ativação rápida de novas contas de clientes livres, guiando o processo cadastral de forma simplificada e síncrona.

## 3. Relações no Metamodelo LeanIX (Fact Sheets Relacionados)
*   **Supports (Apoia):** Redução do ciclo médio de vendas no mercado livre de energia B2B, onboarding de clientes em horas ao invés de semanas, e automação de propostas comerciais.
*   **Supported by (Suportado por):** CRM de Vendas (Salesforce / Dynamics 365), Sistemas de Assinatura Digital (DocuSign), BigQuery para Scoring Preditivo.
*   **Data Objects (Objetos de Dados) Associados:** Leituras de telemetria, relatórios de faturamento, dados cadastrais mestre e bases documentais síncronas.

## 4. Avaliação de Maturidade e Importância Estratégica (Heatmap)
*   **Importância Estratégica (Business Importance):** `tier2` (Mapeado no heatmap corporativo para priorização de recursos e investimentos em modernização tecnológica).
*   **Maturidade Atual (As-Is Maturity):** `Level 3 - Defined` (Escala de maturidade avaliada periodicamente para identificar gaps organizacionais ou de infraestrutura tecnológica).
*   **Diretriz de Roadmap de TI:** Os investimentos de tecnologia devem focar na capacitação contínua das squads, integração ágil via APIs modernas, e na adoção de agentes inteligentes baseados no motor do **Gemini 3.5** para eliminação de gargalos manuais síncronos de alta frequência.
