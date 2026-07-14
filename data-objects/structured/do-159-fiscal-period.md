---
id: DO-159
name: "Fiscal Period"
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

# Fiscal Period (DO-159)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Fiscal Period** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Divisão do ano fiscal (meses calendários e períodos especiais de encerramento) usada para lançamento de transações societárias e regulatórias, essencial para reportes setoriais.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Financeiro
*   **Sistemas e Aplicações que Manipulam (Applications):** ERP (SAP FI)
*   **Sistema de Registro Canônico (System of Truth):** ERP (SAP Financials)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `Período Fiscal (Mês)` | String | Atributo técnico representando o campo mestre 'Período Fiscal (Mês)'. |
| `Exercício Fiscal (Ano)` | String | Atributo técnico representando o campo mestre 'Exercício Fiscal (Ano)'. |
| `Variante de Ano Fiscal (FYV)` | String | Atributo técnico representando o campo mestre 'Variante de Ano Fiscal (FYV)'. |
| `Status do Período (Aberto/Fechado).` | String (Enum) | Atributo técnico representando o campo mestre 'Status do Período (Aberto/Fechado).'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "periodo_fiscal_mes": "2026-07-14T06:55:00Z",
  "exercicio_fiscal_ano": "Dados de Exemplo",
  "variante_de_ano_fisc": "Dados de Exemplo",
  "status_do_periodo_ab": "2026-07-14T06:55:00Z"
}
```

## # Citations

1. Fechamento Contábil e Fiscal Periódico, Reportes Regulatórios ANEEL
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
