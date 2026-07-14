---
id: DO-144
name: "Fatura (Conta de Energia)"
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
  - "Faturamento"
  - "LeanIX-v4"
---

# Fatura (Conta de Energia) (DO-144)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Fatura (Conta de Energia)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Documento financeiro que detalha o consumo, tarifas aplicadas (TE/TUSD), impostos e valor a ser pago pelo cliente.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Clientes / Faturamento
*   **Sistemas e Aplicações que Manipulam (Applications):** CIS, Billing
*   **Sistema de Registro Canônico (System of Truth):** CIS (Customer Information System)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID da Fatura` | String (ID) | Atributo técnico representando o campo mestre 'ID da Fatura'. |
| `ID do Contrato/UC` | String (ID) | Atributo técnico representando o campo mestre 'ID do Contrato/UC'. |
| `Período de Referência` | String | Atributo técnico representando o campo mestre 'Período de Referência'. |
| `Data de Vencimento` | DateTime | Atributo técnico representando o campo mestre 'Data de Vencimento'. |
| `Valor Total` | Float | Atributo técnico representando o campo mestre 'Valor Total'. |
| `Detalhamento de Itens (Energia` | String | Atributo técnico representando o campo mestre 'Detalhamento de Itens (Energia'. |
| `TUSD` | String | Atributo técnico representando o campo mestre 'TUSD'. |
| `TE` | String | Atributo técnico representando o campo mestre 'TE'. |
| `Impostos` | String | Atributo técnico representando o campo mestre 'Impostos'. |
| `Bandeiras Tarifárias).` | String | Atributo técnico representando o campo mestre 'Bandeiras Tarifárias).'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_da_fatura": "REF-DO-144-001",
  "id_do_contrato_uc": "REF-DO-144-001",
  "periodo_de_referenci": "2026-07-14T06:55:00Z",
  "data_de_vencimento": "2026-07-14T06:55:00Z",
  "valor_total": 150.45
}
```

## # Citations

1. ANEEL: PRODIST Módulo 6
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
