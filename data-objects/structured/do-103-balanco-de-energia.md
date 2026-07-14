---
id: DO-103
name: "Balanço de Energia"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Interno"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Nível 3"
  - "Ativos"
  - "Distribuição"
  - "LeanIX-v4"
---

# Balanço de Energia (DO-103)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Balanço de Energia** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Consolidação mensal regulatória das energias injetadas (suprimento), fornecidas (faturamento) e passantes na distribuidora por nível de tensão e origem da energia.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Ativos / Distribuição
*   **Sistemas e Aplicações que Manipulam (Applications):** CIS, ERP (Financeiro), BI
*   **Sistema de Registro Canônico (System of Truth):** CIS (Customer Information System)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `Sigla: BE. COD_ID (PK)` | String (ID) | Atributo técnico representando o campo mestre 'Sigla: BE. COD_ID (PK)'. |
| `DIST` | String | Atributo técnico representando o campo mestre 'DIST'. |
| `SUB_GRP (Subgrupo)` | String | Atributo técnico representando o campo mestre 'SUB_GRP (Subgrupo)'. |
| `ORG_ENER (Origem da energia)` | String | Atributo técnico representando o campo mestre 'ORG_ENER (Origem da energia)'. |
| `ENE_01 a ENE_12 (kWh mensais).` | Float | Atributo técnico representando o campo mestre 'ENE_01 a ENE_12 (kWh mensais).'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "sigla_be_cod_id_pk": "REF-DO-103-001",
  "dist": "Dados de Exemplo",
  "sub_grp_subgrupo": "Dados de Exemplo",
  "org_ener_origem_da_e": "Dados de Exemplo",
  "ene_01_a_ene_12_kwh_": 150.45
}
```

## # Citations

1. ANEEL: PRODIST Módulo 6 (SAMP - Balanço)
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
