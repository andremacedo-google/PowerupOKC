---
id: DO-127
name: "Pagamento"
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
  - "Clientes"
  - "Arrecadação"
  - "LeanIX-v4"
---

# Pagamento (DO-127)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Pagamento** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Registro da quitação de uma fatura por parte do cliente, recebido via arquivo bancário e processado no CIS para atualizar o status do cliente.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Clientes / Arrecadação
*   **Sistemas e Aplicações que Manipulam (Applications):** CIS, ERP (Financeiro)
*   **Sistema de Registro Canônico (System of Truth):** CIS (Customer Information System)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Pagamento` | String (ID) | Atributo técnico representando o campo mestre 'ID do Pagamento'. |
| `ID da Fatura` | String (ID) | Atributo técnico representando o campo mestre 'ID da Fatura'. |
| `Data do Pagamento` | DateTime | Atributo técnico representando o campo mestre 'Data do Pagamento'. |
| `Valor Pago` | Float | Atributo técnico representando o campo mestre 'Valor Pago'. |
| `Canal de Pagamento (Banco` | String | Atributo técnico representando o campo mestre 'Canal de Pagamento (Banco'. |
| `Loterica` | String | Atributo técnico representando o campo mestre 'Loterica'. |
| `App` | String | Atributo técnico representando o campo mestre 'App'. |
| `Débito Automático)` | String | Atributo técnico representando o campo mestre 'Débito Automático)'. |
| `Status (Liquidado` | String (ID) | Atributo técnico representando o campo mestre 'Status (Liquidado'. |
| `Em aberto).` | String | Atributo técnico representando o campo mestre 'Em aberto).'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_pagamento": "REF-DO-127-001",
  "id_da_fatura": "REF-DO-127-001",
  "data_do_pagamento": "2026-07-14T06:55:00Z",
  "valor_pago": 150.45,
  "canal_de_pagamento_b": "Dados de Exemplo"
}
```

## # Citations

1. Processo de Arrecadação
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
