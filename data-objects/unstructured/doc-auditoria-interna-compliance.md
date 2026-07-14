---
id: DO-211
name: "Relatórios de Auditoria Interna e Compliance"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Confidencial"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Não Estruturado"
  - "LeanIX-v4"
---

# Relatórios de Auditoria Interna e Compliance (DO-211)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança da base de conhecimento não estruturada **Relatórios de Auditoria Interna e Compliance** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Relatórios formais gerados pelas Três Linhas de Defesa que avaliam a eficácia dos controles internos, conformidade regulatória e compliance com as normas SOX e regulamentos da ANEEL.

Este objeto de dados não estruturado é de extrema importância para as regras de conformidade regulatória (conforme as diretrizes de regulação tarifária, fiscalização ou as instruções operacionais do SIN). Sua correta catalogação impede silos de conhecimento e vazamentos de informações classificadas.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade, linhagem e governança de dados no repositório corporativo da PowerUp, este Data Object mantém as seguintes conexões estáveis:

*   **Subdomínio de Dados (Nível 1):** Corporativo e Governança / Gestão de Riscos e Controles
*   **Sistemas e Aplicações Relacionadas (Applications):** SAP GRC, ServiceNow GRC, SharePoint de Auditoria Interna
*   **Repositório/Sistema de Registro Canônico (System of Truth):** Repositório de Auditoria e GRC Corporativo (Comitê de Auditoria)
*   **Capacidade de Negócio Relacionada:** Gestão de Riscos, Controles Internos, Auditoria e Conformidade Societária
*   **Documento de Referência (Mestre):** nao

## # Schema

Este ativo de dados não estruturados de referência é composto e regido pelos seguintes temas críticos e tipos de informações:

*   **Informações Críticas e Conteúdo Típico:** Resultados de auditorias em processos operacionais (ex: unitização de ativos, faturamento M2C), pareceres sobre riscos regulatórios, planos de mitigação de conformidade e testes de controles internos.
*   **Classificação de Privacidade e Sensibilidade (Compliance/LGPD):** Confidencial

## # Examples

Abaixo está exemplificado um rascunho de metadados em formato estruturado representando o objeto documental, indicando as variáveis comumente contidas em seu fluxo de indexação:

```json
{"relatorio_auditoria_m2c": {"status": "Revisão concluída com ressalvas", "controles_validados": ["Reconciliação entre faturas do faturador CIS e lançamentos contábeis SAP FI-CA", "Controles SOX de acesso a tabelas de faturamento"]}}
```

## # Citations

1. [Manual de Governança de Informações Não Estruturadas PowerupOKC] - Rege os padrões de indexação, controle e privacidade das bases de conhecimento setoriais.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
