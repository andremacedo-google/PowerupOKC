---
id: DO-217
name: "Documentação de Sistemas (SCADA, GIS, EAM) e TDDs"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Interno"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Não Estruturado"
  - "LeanIX-v4"
---

# Documentação de Sistemas (SCADA, GIS, EAM) e TDDs (DO-217)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança da base de conhecimento não estruturada **Documentação de Sistemas (SCADA, GIS, EAM) e TDDs** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Manuais de usuário, guias de configuração e Technical Design Documents (TDDs) que especificam o design de integrações, dicionários de dados e lógicas dos sistemas de TI e TO.

Este objeto de dados não estruturado é de extrema importância para as regras de conformidade regulatória (conforme as diretrizes de regulação tarifária, fiscalização ou as instruções operacionais do SIN). Sua correta catalogação impede silos de conhecimento e vazamentos de informações classificadas.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade, linhagem e governança de dados no repositório corporativo da PowerUp, este Data Object mantém as seguintes conexões estáveis:

*   **Subdomínio de Dados (Nível 1):** Técnico e Operacional / TI / TO
*   **Sistemas e Aplicações Relacionadas (Applications):** ServiceNow, Confluence, GED de TI/TO, Jira
*   **Repositório/Sistema de Registro Canônico (System of Truth):** Repositório de Arquitetura e Engenharia de Software (Confluence/ServiceNow)
*   **Capacidade de Negócio Relacionada:** Governança de TI/TO, Arquitetura de Sistemas, Sustentação de Infraestrutura
*   **Documento de Referência (Mestre):** sim

## # Schema

Este ativo de dados não estruturados de referência é composto e regido pelos seguintes temas críticos e tipos de informações:

*   **Informações Críticas e Conteúdo Típico:** Dicionários de dados internos das bases, diagramas de arquitetura e servidores, configurações de protocolos industriais (DNP3, IEC 61850) e especificações de APIs de integração.
*   **Classificação de Privacidade e Sensibilidade (Compliance/LGPD):** Interno

## # Examples

Abaixo está exemplificado um rascunho de metadados em formato estruturado representando o objeto documental, indicando as variáveis comumente contidas em seu fluxo de indexação:

```json
{"tdd_api_gis_scada": {"api_id": "API-GIS-ADMS-012", "protocolo": "REST / XML CIM", "tipo_transferencia": "Sincronização topológica assíncrona diária de novos ramais elétricos cadastrados no GIS"}}
```

## # Citations

1. [Manual de Governança de Informações Não Estruturadas PowerupOKC] - Rege os padrões de indexação, controle e privacidade das bases de conhecimento setoriais.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
