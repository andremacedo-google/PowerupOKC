---
id: CAP-L3-012
name: "Segurança Cibernética (TI/OT)"
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
  - "Gestão de Tecnologia da Informação"
  - "ADK (Custom Agent)"
---

# Segurança Cibernética (TI/OT) (CAP-L3-012)

Esta capacidade técnica detalhada de Nível 3 faz parte do grupo funcional **Gestão de Tecnologia da Informação** sob a área principal de **Corporativo e Suporte ao Negócio** no Mapa de Capacidades do Setor de Energia.

---

## 1. Descrição Geral da Capacidade
A capacidade **Segurança Cibernética (TI/OT)** rege o controle e a operação das atividades granulares de utilities relacionadas ao seu escopo. No contexto do setor elétrico brasileiro, ela é fundamental para a transição para uma rede mais conectada, sustentável e eficiente, alinhada com as macrotendências de Descarbonização, Descentralização e Digitalização (3Ds).

---

## 2. Orquestração da Inteligência Artificial

Para automatizar e elevar o nível de maturidade desta capacidade, sugere-se a implantação de uma solução baseada em agentes inteligentes, conforme especificado abaixo:

*   **Agente Sugerido:** SIEM Alert Triage & Defender TI/OT
*   **Classificação Arquitetural:** ADK (Custom Agent)
*   **Papel Operacional & Integrações:** SOC inteligente focado na triagem em tempo real de ameaças e detecção de anomalias em firewalls industriais e redes SCADA.

---

## 3. Especificação de Dados e Governança

A integridade e confiabilidade da operação dependem de barramentos de dados governados estruturados na nuvem (Data Lakehouse corporativo):

*   **Inputs e Base de Conhecimento Requeridos:** Logs de Acesso a Servidores, Logs de Redes SCADA/TO, Alertas SIEM, Políticas de Acesso IAM.
*   **Saída Esperada do Processo:** Triagem e Priorização de Alertas de Segurança, Alertas de Comportamentos Anômalos em Redes.

---

## 4. Relações no Metamodelo SAP LeanIX v4

Como elemento integrante da arquitetura corporativa da PowerUp, esta capacidade mantém as seguintes associações estáveis:

*   **Parent Capability (Nível 2):** [/business-capabilities/corporativo-e-suporte-ao-negocio/gestao-de-tecnologia-da-informacao/index.md](Gestão de Tecnologia da Informação)
*   **Parent Capability (Nível 1):** [/business-capabilities/corporativo-e-suporte-ao-negocio/index.md](Corporativo e Suporte ao Negócio)
*   **Supported by (Applications):** [/applications/siem-alert-triage-defender-tiot.md](SIEM Alert Triage & Defender TI/OT)
*   **Associated Data Objects:** [/data-objects/logs-de-acesso-a-servidores.md](Logs de Acesso a Servidores, Logs de Redes SCADA/TO, Alertas SIEM, Políticas de Acesso IAM.)
*   **Importance Heatmap:** `parity` (Commodity (operational needs, maintaining baseline parity))
*   **Current Maturity:** `Level 4 - Managed`

---

## 5. Citações e Referências Regulatórias
1. [Regulações ANEEL e Procedimentos de Rede ONS](https://www.aneel.gov.br/) - Padrões de conformidade técnica e operacional exigidos para a operação coordenada do sistema elétrico nacional.
2. [SAP LeanIX Best Practice Reference Model](https://www.leanix.net/) - Framework estrutural para modelagem e mapeamento de capacidades de Utilities.
