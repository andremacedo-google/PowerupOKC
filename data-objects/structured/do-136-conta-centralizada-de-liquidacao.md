---
id: DO-136
name: "Conta Centralizada de Liquidação"
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
  - "Comercialização"
  - "LeanIX-v4"
---

# Conta Centralizada de Liquidação (DO-136)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Conta Centralizada de Liquidação** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Cadastro e gestão de contas bancárias de agentes, garantias financeiras aportadas e acompanhamento da liquidação multilateral mensal do Mercado de Curto Prazo (MCP).

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Clientes / Comercialização
*   **Sistemas e Aplicações que Manipulam (Applications):** Sistemas CCEE, ERP (SAP FI)
*   **Sistema de Registro Canônico (System of Truth):** CCEE / ERP (SAP S/4HANA)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `CodAgente` | String (ID) | Atributo técnico representando o campo mestre 'CodAgente'. |
| `val_garantia_financeira` | Float | Atributo técnico representando o campo mestre 'val_garantia_financeira'. |
| `val_liquidacao_mcp_debito` | String (ID) | Atributo técnico representando o campo mestre 'val_liquidacao_mcp_debito'. |
| `val_liquidacao_mcp_credito` | String (ID) | Atributo técnico representando o campo mestre 'val_liquidacao_mcp_credito'. |
| `banco_custodiante` | Float | Atributo técnico representando o campo mestre 'banco_custodiante'. |
| `sts_adimplemento.` | String (Enum) | Atributo técnico representando o campo mestre 'sts_adimplemento.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "codagente": "REF-DO-136-001",
  "val_garantia_finance": 150.45,
  "val_liquidacao_mcp_d": "REF-DO-136-001",
  "val_liquidacao_mcp_c": "REF-DO-136-001",
  "banco_custodiante": 150.45
}
```

## # Citations

1. CCEE: Procedimentos de Comercialização (Módulo 5)
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
