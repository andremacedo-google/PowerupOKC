---
id: DO-156
name: "Contas a Pagar"
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
  - "Corporativo"
  - "Financeiro"
  - "LeanIX-v4"
---

# Contas a Pagar (DO-156)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Contas a Pagar** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Obrigações financeiras de curto e longo prazo a serem pagas a fornecedores, empreiteiras de obras ou órgãos setoriais, controladas pelo contas a pagar do ERP.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Financeiro
*   **Sistemas e Aplicações que Manipulam (Applications):** ERP (SAP FI-AP)
*   **Sistema de Registro Canônico (System of Truth):** ERP (SAP Financials)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Pagamento` | String (ID) | Atributo técnico representando o campo mestre 'ID do Pagamento'. |
| `ID do Fornecedor` | String (ID) | Atributo técnico representando o campo mestre 'ID do Fornecedor'. |
| `ID da Fatura` | String (ID) | Atributo técnico representando o campo mestre 'ID da Fatura'. |
| `Valor do Pagamento` | Float | Atributo técnico representando o campo mestre 'Valor do Pagamento'. |
| `Data de Vencimento` | DateTime | Atributo técnico representando o campo mestre 'Data de Vencimento'. |
| `Status de Aprovação` | String (Enum) | Atributo técnico representando o campo mestre 'Status de Aprovação'. |
| `Banco Beneficiário.` | String | Atributo técnico representando o campo mestre 'Banco Beneficiário.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_pagamento": "REF-DO-156-001",
  "id_do_fornecedor": "REF-DO-156-001",
  "id_da_fatura": "REF-DO-156-001",
  "valor_do_pagamento": 150.45,
  "data_de_vencimento": "2026-07-14T06:55:00Z"
}
```

## # Citations

1. Processo de Tesouraria e Liquidação de Fornecedores, Controle de Custos de CAPEX/OPEX
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
