---
id: DO-207
name: "Documentação de Audiências e Consultas Públicas"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Público"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Não Estruturado"
  - "LeanIX-v4"
---

# Documentação de Audiências e Consultas Públicas (DO-207)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança da base de conhecimento não estruturada **Documentação de Audiências e Consultas Públicas** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Processos administrativos conduzidos pela ANEEL para promover transparência e participação social antes de editar resoluções normativas ou aprovar revisões tarifárias.

Este objeto de dados não estruturado é de extrema importância para as regras de conformidade regulatória (conforme as diretrizes de regulação tarifária, fiscalização ou as instruções operacionais do SIN). Sua correta catalogação impede silos de conhecimento e vazamentos de informações classificadas.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade, linhagem e governança de dados no repositório corporativo da PowerUp, este Data Object mantém as seguintes conexões estáveis:

*   **Subdomínio de Dados (Nível 1):** Regulatório e Planejamento / Processos Regulatórios
*   **Sistemas e Aplicações Relacionadas (Applications):** Portal da ANEEL, SharePoint Regulatório, GED de Regulação
*   **Repositório/Sistema de Registro Canônico (System of Truth):** Sistema de Consultas Públicas da ANEEL
*   **Capacidade de Negócio Relacionada:** Interface Regulatória, Advocacia e Gestão de Conformidade
*   **Documento de Referência (Mestre):** nao

## # Schema

Este ativo de dados não estruturados de referência é composto e regido pelos seguintes temas críticos e tipos de informações:

*   **Informações Críticas e Conteúdo Típico:** Relatórios de Análise de Impacto Regulatório (AIR), Notas Técnicas das áreas especializadas da agência, e as contribuições e sugestões por escrito enviadas pelas empresas e agentes setoriais.
*   **Classificação de Privacidade e Sensibilidade (Compliance/LGPD):** Público

## # Examples

Abaixo está exemplificado um rascunho de metadados em formato estruturado representando o objeto documental, indicando as variáveis comumente contidas em seu fluxo de indexação:

```json
{"consulta_publica_aneel": {"id": "CP-015/2026", "tema": "Alteração das taxas de fiscalização dos serviços de eletricidade", "documentos_anexos": ["Nota Técnica Reguladora", "AIR preliminar"]}}
```

## # Citations

1. [Manual de Governança de Informações Não Estruturadas PowerupOKC] - Rege os padrões de indexação, controle e privacidade das bases de conhecimento setoriais.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
