---
id: DO-141
name: "Preço de Liquidação das Diferenças (PLD)"
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
  - "Comercialização"
  - "LeanIX-v4"
---

# Preço de Liquidação das Diferenças (PLD) (DO-141)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Preço de Liquidação das Diferenças (PLD)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Preço de referência horário da energia no mercado spot de curto prazo, calculado pela CCEE por submercado para valorar as exposições de compra e venda de energia.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Clientes / Comercialização
*   **Sistemas e Aplicações que Manipulam (Applications):** Sistemas CCEE, ETRM, TRM (SAP)
*   **Sistema de Registro Canônico (System of Truth):** CCEE (Dados Públicos)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `submercado (SE/CO` | String | Atributo técnico representando o campo mestre 'submercado (SE/CO'. |
| `S` | String | Atributo técnico representando o campo mestre 'S'. |
| `N` | String | Atributo técnico representando o campo mestre 'N'. |
| `NE)` | String | Atributo técnico representando o campo mestre 'NE)'. |
| `data_hora` | DateTime | Atributo técnico representando o campo mestre 'data_hora'. |
| `val_pld_horario (R$/MWh)` | Float | Atributo técnico representando o campo mestre 'val_pld_horario (R$/MWh)'. |
| `val_pld_medio` | Float | Atributo técnico representando o campo mestre 'val_pld_medio'. |
| `sts_limite (máximo/mínimo)` | Float | Atributo técnico representando o campo mestre 'sts_limite (máximo/mínimo)'. |
| `fcf_valores.` | Float | Atributo técnico representando o campo mestre 'fcf_valores.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "submercado_se_co": "Dados de Exemplo",
  "s": "Dados de Exemplo",
  "n": "Dados de Exemplo",
  "ne": "Dados de Exemplo",
  "data_hora": "2026-07-14T06:55:00Z"
}
```

## # Citations

1. CCEE: Regras de Comercialização (Preço Spot)
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
