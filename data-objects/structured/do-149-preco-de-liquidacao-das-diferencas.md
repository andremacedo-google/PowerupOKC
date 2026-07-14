---
id: DO-149
name: "Preço de Liquidação das Diferenças"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Confidencial (Financeiro)"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Nível 3"
  - "Clientes"
  - "Mercado"
  - "LeanIX-v4"
---

# Preço de Liquidação das Diferenças (DO-149)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Preço de Liquidação das Diferenças** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Preço horário da energia no mercado spot, calculado pela CCEE por submercado e usado para valorar as exposições.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Clientes / Mercado
*   **Sistemas e Aplicações que Manipulam (Applications):** TRM, Sistemas de Mercado, BI
*   **Sistema de Registro Canônico (System of Truth):** CCEE (Dados Públicos)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `Data/Hora` | DateTime | Atributo técnico representando o campo mestre 'Data/Hora'. |
| `Submercado (SE/CO` | String | Atributo técnico representando o campo mestre 'Submercado (SE/CO'. |
| `S` | String | Atributo técnico representando o campo mestre 'S'. |
| `NE` | String | Atributo técnico representando o campo mestre 'NE'. |
| `N)` | String | Atributo técnico representando o campo mestre 'N)'. |
| `Valor (R$/MWh).` | Float | Atributo técnico representando o campo mestre 'Valor (R$/MWh).'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "data_hora": "2026-07-14T06:55:00Z",
  "submercado_se_co": "Dados de Exemplo",
  "s": "Dados de Exemplo",
  "ne": "Dados de Exemplo",
  "n": "Dados de Exemplo"
}
```

## # Citations

1. CCEE: Preço Spot
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
