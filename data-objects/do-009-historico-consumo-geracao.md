---
id: DO-009
name: "Histórico de Consumo e Geração"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Restrito (LGPD)"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Clientes"
  - "LeanIX-v4"
---

# Histórico de Consumo e Geração (ID: DO-009)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Histórico de Consumo e Geração** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Balanço mensal consolidado de kWh consumido e injetado pelo cliente prossumidor na rede para faturamento e rateio.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, da CCEE e as regras nacionais de segurança da informação e privacidade de dados (LGPD), garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Capacidades de Negócio que Consomem/Produzem (Business Capabilities N3):**
    *   [/cap-l3-processamento-de-faturas](Capacidade Processamento De Faturas)
    *   [/cap-l3-atendimento-ao-cliente-multicanal](Capacidade Atendimento Ao Cliente Multicanal)
*   **Sistemas e Aplicações que Manipulam (Applications):**
    *   [/applications/app-cis-faturamento-comercial](Aplicação Cis Faturamento Comercial)
    *   [/applications/app-crm-relacionamento-cliente](Aplicação Crm Relacionamento Cliente)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `id_instalacao_cis` | String | Identificador mestre da instalação comercial (Contract Location ID). |
| `periodo_faturamento` | String (YYYYMM) | Mês e ano fiscal do ciclo de faturamento consolidado. |
| `energia_consumida_kwh` | Float | Total acumulado de energia elétrica ativa consumida no ciclo (kWh). |
| `energia_injetada_kwh` | Float | Total de energia elétrica injetada na rede pelo prossumidor (kWh). |
| `saldo_credito_anterior_kwh` | Float | Crédito acumulado de ciclos de compensação anteriores pendentes (kWh). |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_instalacao_cis": "INST-4431201",
  "periodo_faturamento": "202606",
  "energia_consumida_kwh": 350.0,
  "energia_injetada_kwh": 480.0,
  "saldo_credito_anterior_kwh": 120.5
}
```

## # Citations

1. [Manual de Governança de Dados PowerupOKC] - Estabelece as regras de classificação de segurança e sensibilidade das informações corporativas e reguladas.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
