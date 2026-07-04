---
id: "BC-GEST-TECNOLOGIA-INFORMACAO"
name: "Gestão de Tecnologia da Informação"
type: "Business Capability"
subtype: "Level 2"
parent: "Corporativo e Suporte ao Negócio"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
strategicImportance: "parity"
maturity: "Level 4 - Managed"
tags:
  - "Corporativo"
  - "TI"
  - "Ciberseguranca"
  - "Infraestrutura"
  - "LeanIX-v4"
---

# Especificação Técnica: Gestão de Tecnologia da Informação (ID: BC-GEST-TECNOLOGIA-INFORMACAO)

Esta Business Capability de Nível 2 pertence ao domínio principal de **Corporativo e Suporte ao Negócio** no ecossistema de Enterprise Architecture da companhia. Ela representa o conjunto de habilidades, competências de pessoas, ferramentas de tecnologia e modelagens de dados corporativos necessários para governar de forma ótima esta frente de trabalho específica do setor de energia.

## 1. Sub-capacidades de Nível 3 Associadas
De acordo com a taxonomia padronizada e o Mapa de Capacidades de Negócio, este grupo gerencial decompõe-se nas seguintes habilidades e atividades operacionais de Nível 3:

*   **Arquitetura de TI e de Dados:** Desenvolve e mantém a arquitetura de sistemas e dados para garantir escalabilidade, segurança e alinhamento com o negócio.
*   **Segurança Cibernética (TI/OT):** Protege os sistemas de informação e de operação contra ameaças cibernéticas, garantindo a integridade da infraestrutura crítica.
*   **Gestão de Infraestrutura e Operações de TI:** Gerencia data centers, redes de comunicação e a infraestrutura de nuvem que suporta as operações da empresa.

## 2. Agentes de Inteligência Artificial Habilitados
Esta capacidade de negócio é modernizada no Gemini Enterprise através dos seguintes agentes de IA especializados que atuam no refinamento ou automação de suas tarefas:

*   **System Dependency Mapper & API Governance (ADK (Custom Agent)):** Varre programmaticamente os catálogos de APIs e os repositórios da empresa para documentar e auditar dependências sistêmicas.
*   **SIEM Alert Triage & Defender TI/OT (ADK (Custom Agent)):** SOC inteligente focado na triagem em tempo real de ameaças e detecção de anomalias em firewalls industriais e redes SCADA.
*   **Cloud Cost Optimizer & IaC Drift Detector (ADK (Custom Agent)):** Analisa continuamente a volumetria de custos em nuvem (FinOps), recomendando otimizações de recursos e alertando sobre desvios IaC.

## 3. Relações no Metamodelo LeanIX (Fact Sheets Relacionados)
*   **Supports (Apoia):** Governança de APIs, redução de custos de nuvem (FinOps), conformidade com Resolução ANEEL 964/2021 e blindagem de ataques cibernéticos em subestações de rede.
*   **Supported by (Suportado por):** Nuvens Públicas (Google Cloud, AWS, Azure), Ferramentas IaC (Terraform), Soluções de SOC/SIEM (Splunk, Chronicle), e Repositórios de Dados (BigQuery).
*   **Data Objects (Objetos de Dados) Associados:** Leituras de telemetria, relatórios de faturamento, dados cadastrais mestre e bases documentais síncronas.

## 4. Avaliação de Maturidade e Importância Estratégica (Heatmap)
*   **Importância Estratégica (Business Importance):** `parity` (Mapeado no heatmap corporativo para priorização de recursos e investimentos em modernização tecnológica).
*   **Maturidade Atual (As-Is Maturity):** `Level 4 - Managed` (Escala de maturidade avaliada periodicamente para identificar gaps organizacionais ou de infraestrutura tecnológica).
*   **Diretriz de Roadmap de TI:** Os investimentos de tecnologia devem focar na capacitação contínua das squads, integração ágil via APIs modernas, e na adoção de agentes inteligentes baseados no motor do **Gemini 3.5** para eliminação de gargalos manuais síncronos de alta frequência.
