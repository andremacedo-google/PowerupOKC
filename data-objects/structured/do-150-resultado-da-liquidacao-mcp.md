---
id: DO-150
name: "Resultado da Liquidação (MCP)"
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
  - "Mercado"
  - "LeanIX-v4"
---

# Resultado da Liquidação (MCP) (DO-150)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Resultado da Liquidação (MCP)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Resultado financeiro final (débito ou crédito) de um agente no Mercado de Curto Prazo, apurado pela CCEE.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Clientes / Mercado
*   **Sistemas e Aplicações que Manipulam (Applications):** TRM, Sistemas de Mercado, BI, DRI
*   **Sistema de Registro Canônico (System of Truth):** CCEE (DRI - Divulgação de Resultados)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `Identificação do Agente` | String (ID) | Atributo técnico representando o campo mestre 'Identificação do Agente'. |
| `Mês de Referência` | String | Atributo técnico representando o campo mestre 'Mês de Referência'. |
| `Valor Total a Liquidar` | String (ID) | Atributo técnico representando o campo mestre 'Valor Total a Liquidar'. |
| `Balanço Energético` | String | Atributo técnico representando o campo mestre 'Balanço Energético'. |
| `Encargos (ESS).` | String | Atributo técnico representando o campo mestre 'Encargos (ESS).'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "identificacao_do_age": "REF-DO-150-001",
  "mes_de_referencia": "Dados de Exemplo",
  "valor_total_a_liquid": "REF-DO-150-001",
  "balanco_energetico": "Dados de Exemplo",
  "encargos_ess": "Dados de Exemplo"
}
```

## # Citations

1. CCEE (Processo de Contabilização)
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
