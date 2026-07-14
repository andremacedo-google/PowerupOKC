---
id: AP-014
name: "EAM - Engenharia e Gestão de Ativos Físicos"
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
  - "LeanIX-v4"
---

# EAM - Engenharia e Gestão de Ativos Físicos (ID: AP-014)

Este Fact Sheet de **Business Application** descreve no padrão de arquitetura empresarial da **SAP LeanIX v4** o escopo de atuação e barramento de dados do sistema **EAM - Engenharia e Gestão de Ativos Físicos** [13, 33]. Ele atua como um pilar fundamental da camada de aplicação e dados da companhia, estruturando as operações no Setor Elétrico Brasileiro [13, 34].

## 1. Escopo Técnico e de Negócio
No contexto das utilities de energia e da transição energética regulada pelas agências setoriais (como ANEEL e ONS), esta aplicação desempenha o papel de:
*   **Sistema responsável pela governança de manutenção preventiva, corretiva e preditiva de equipamentos técnicos elétricos, ciclo de vida útil e apropriação de despesas operacionais (O&M).** [33, 438]

Ela é projetada para manter a consistência lógica, automatizar workflows operacionais síncronos e reduzir atritos nos processos core de negócios [34, 439].

## 2. Integrações e Fluxo de Dados (Data Objects)
No barramento de integração corporativo de TI/OT, esta aplicação atua como **System of Truth (SOT)** canônico ou consumidora nos seguintes fluxos de dados mestre [31, 456]:

*   **Inputs (Dados de Entrada consumidos):**
    *   `[/data-objects/do-004-dados-de-sensores-de-ativos-iot.md](DO-004 Dados de Sensores de Ativos (IoT))` [31, 34]
*   **Outputs (Dados de Saída fornecidos ou gravados):**
    *   `[/data-objects/do-019-inventário-de-peças-sobressalentes-mro-work-orders-e-reservas-de-materiais.md](DO-019 Inventário de Peças Sobressalentes (MRO) (Work Orders e Reservas de Materiais))` [31, 34]

## 3. Capacidades de Negócio Suportadas
Este sistema apoia e habilita tecnologicamente a execução operacional das seguintes capacidades estratégicas de Nível 3 [21, 129]:
*   `[/business-capabilities/cap-l3-planejamento-do-ciclo-de-vida-dos-ativos.md](Planejamento Do Ciclo De Vida Dos Ativos)`
*   `[/business-capabilities/cap-l3-manutencao-preditiva.md](Manutencao Preditiva)` [21, 129]

## 4. Exemplos de Soluções e Tecnologias de Mercado
Como parte das melhores práticas da SAP LeanIX v4, o nome desta aplicação é desacoplado de marcas comerciais. Os principais pacotes de software COTS líderes de mercado que implementam este escopo de negócio são [35, 338]:
*   **SAP S/4HANA Asset Management (PM), IBM Maximo Asset Management, Infor EAM** [35, 338]

## 5. Práticas de Governança e FinOps
*   **Modelagem de Hierarquias (LeanIX):** Recomenda-se modelar esta aplicação em nível lógico de Nível 1, estruturando seus módulos operacionais como filhos lógicos de Nível 2 apenas quando houver necessidade explícita de controle orçamentário segregado [43].
*   **FinOps & Licenciamento:** O monitoramento de custos de computação em nuvem deve isolar e alocar o consumo transacional de alto volume (como barramentos de mensageria de telemetria ou faturamento em massa) em relação aos fluxos de processamento administrativo sob o modelo de tags do provedor [49].
*   **Conformidade & Segurança:** A conformidade com a LGPD e as normas de cibersegurança da ANEEL (REN 964) exige criptografia ativa em repouso e em trânsito (AES-256 e TLS 1.3) para dados classificados como Restritos ou Confidenciais [152].

---

## # Citations
1. [SAP LeanIX - Best Practices Application Modeling Guidelines](https://www.leanix.net/) - Guia oficial de governança de Fact Sheets e modelagem enxuta do metamodelo v4.
2. [Procedimentos e Regras do Setor Elétrico Brasileiro] - Regulamentações de conformidade técnica e faturamento comercial.
