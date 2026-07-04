---
id: CAP-L3-005
name: "Aquisição de Talentos"
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
  - "Gestão de Pessoas e Cultura"
  - "No-code (Agent Designer)"
---

# Aquisição de Talentos (CAP-L3-005)

Esta capacidade técnica detalhada de Nível 3 faz parte do grupo funcional **Gestão de Pessoas e Cultura** sob a área principal de **Corporativo e Suporte ao Negócio** no Mapa de Capacidades do Setor de Energia.

---

## 1. Descrição Geral da Capacidade
A capacidade **Aquisição de Talentos** rege o controle e a operação das atividades granulares de utilities relacionadas ao seu escopo. No contexto do setor elétrico brasileiro, ela é fundamental para a transição para uma rede mais conectada, sustentável e eficiente, alinhada com as macrotendências de Descarbonização, Descentralização e Digitalização (3Ds).

---

## 2. Orquestração da Inteligência Artificial

Para automatizar e elevar o nível de maturidade desta capacidade, sugere-se a implantação de uma solução baseada em agentes inteligentes, conforme especificado abaixo:

*   **Agente Sugerido:** Tech Recruiter & Resume Screener
*   **Classificação Arquitetural:** No-code (Agent Designer)
*   **Papel Operacional & Integrações:** Automatiza a triagem de currículos, cruza as qualificações com as especificações do cargo e desenvolve roteiros estruturados de perguntas técnicas.

---

## 3. Especificação de Dados e Governança

A integridade e confiabilidade da operação dependem de barramentos de dados governados estruturados na nuvem (Data Lakehouse corporativo):

*   **Inputs e Base de Conhecimento Requeridos:** Currículos (PDF/Docx), Perfis de Cargos (Job Descriptions), Critérios Técnicos de Avaliação da Vaga.
*   **Saída Esperada do Processo:** Parecer de Aderência Candidato-Vaga (Score de Match), Roteiro de Entrevista Técnica Customizado.

---

## 4. Relações no Metamodelo SAP LeanIX v4

Como elemento integrante da arquitetura corporativa da PowerUp, esta capacidade mantém as seguintes associações estáveis:

*   **Parent Capability (Nível 2):** [/business-capabilities/corporativo-e-suporte-ao-negocio/gestao-de-pessoas-e-cultura/index.md](Gestão de Pessoas e Cultura)
*   **Parent Capability (Nível 1):** [/business-capabilities/corporativo-e-suporte-ao-negocio/index.md](Corporativo e Suporte ao Negócio)
*   **Supported by (Applications):** [/applications/tech-recruiter-resume-screener.md](Tech Recruiter & Resume Screener)
*   **Associated Data Objects:** [/data-objects/curriculos-pdfdocx.md](Currículos (PDF/Docx), Perfis de Cargos (Job Descriptions), Critérios Técnicos de Avaliação da Vaga.)
*   **Importance Heatmap:** `parity` (Commodity (operational needs, maintaining baseline parity))
*   **Current Maturity:** `Level 4 - Managed`

---

## 5. Citações e Referências Regulatórias
1. [Regulações ANEEL e Procedimentos de Rede ONS](https://www.aneel.gov.br/) - Padrões de conformidade técnica e operacional exigidos para a operação coordenada do sistema elétrico nacional.
2. [SAP LeanIX Best Practice Reference Model](https://www.leanix.net/) - Framework estrutural para modelagem e mapeamento de capacidades de Utilities.
