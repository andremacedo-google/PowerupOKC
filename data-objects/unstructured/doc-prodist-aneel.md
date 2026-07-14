---
id: DO-202
name: "PRODIST - Procedimentos de Distribuição da ANEEL"
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

# PRODIST - Procedimentos de Distribuição da ANEEL (DO-202)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança da base de conhecimento não estruturada **PRODIST - Procedimentos de Distribuição da ANEEL** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Normas técnicas e comerciais elaboradas pela ANEEL para padronizar e regular as atividades das distribuidoras de energia em tensões inferiores a 230 kV.

Este objeto de dados não estruturado é de extrema importância para as regras de conformidade regulatória (conforme as diretrizes de regulação tarifária, fiscalização ou as instruções operacionais do SIN). Sua correta catalogação impede silos de conhecimento e vazamentos de informações classificadas.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade, linhagem e governança de dados no repositório corporativo da PowerUp, este Data Object mantém as seguintes conexões estáveis:

*   **Subdomínio de Dados (Nível 1):** Regulatório e Planejamento / Arcabouço Regulatório
*   **Sistemas e Aplicações Relacionadas (Applications):** Portal ANEEL, SharePoint de Engenharia e Operações, GED de Distribuição
*   **Repositório/Sistema de Registro Canônico (System of Truth):** Biblioteca Reguladora da ANEEL / GED Regulatório
*   **Capacidade de Negócio Relacionada:** Planejamento, Conexão, Medição e Operação Técnica da Distribuição de Energia
*   **Documento de Referência (Mestre):** sim

## # Schema

Este ativo de dados não estruturados de referência é composto e regido pelos seguintes temas críticos e tipos de informações:

*   **Informações Críticas e Conteúdo Típico:** Glossário (Mód. 1), Planejamento da expansão (Mód. 2), Critérios de conexão de unidades e usinas (Mód. 3), Medição de faturamento (Mód. 5), Perdas técnicas e comerciais (Mód. 7), DEC/FEC (Mód. 8).
*   **Classificação de Privacidade e Sensibilidade (Compliance/LGPD):** Público

## # Examples

Abaixo está exemplificado um rascunho de metadados em formato estruturado representando o objeto documental, indicando as variáveis comumente contidas em seu fluxo de indexação:

```json
{"prodist_modulo_8": {"secao": "Qualidade do Fornecimento", "indicadores": ["DEC", "FEC", "DIC", "FIC"], "regra": "Estabelece metas e limites máximos de interrupção individual por Unidade Consumidora"}}
```

## # Citations

1. [Manual de Governança de Informações Não Estruturadas PowerupOKC] - Rege os padrões de indexação, controle e privacidade das bases de conhecimento setoriais.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
