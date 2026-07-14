---
id: DO-160
name: "Lançamento Contábil"
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

# Lançamento Contábil (DO-160)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Lançamento Contábil** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Registro de uma transação financeira nos livros contábeis da empresa (ex: receita do faturamento M2C ou capitalização de ativo).

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Financeiro
*   **Sistemas e Aplicações que Manipulam (Applications):** ERP (SAP FI, CO)
*   **Sistema de Registro Canônico (System of Truth):** ERP (SAP FI)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Lançamento` | String (ID) | Atributo técnico representando o campo mestre 'ID do Lançamento'. |
| `Data` | DateTime | Atributo técnico representando o campo mestre 'Data'. |
| `Conta Débito` | String | Atributo técnico representando o campo mestre 'Conta Débito'. |
| `Conta Crédito` | String | Atributo técnico representando o campo mestre 'Conta Crédito'. |
| `Valor` | Float | Atributo técnico representando o campo mestre 'Valor'. |
| `Centro de Custo` | Float | Atributo técnico representando o campo mestre 'Centro de Custo'. |
| `Descrição.` | String | Atributo técnico representando o campo mestre 'Descrição.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_lancamento": "REF-DO-160-001",
  "data": "2026-07-14T06:55:00Z",
  "conta_debito": "Dados de Exemplo",
  "conta_credito": "Dados de Exemplo",
  "valor": 150.45
}
```

## # Citations

1. Contabilidade Geral
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
