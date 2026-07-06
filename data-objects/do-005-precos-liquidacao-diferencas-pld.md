---
id: DO-005
name: "Preços de Liquidação de Diferenças (PLD)"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Público"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Operações"
  - "LeanIX-v4"
---

# Preços de Liquidação de Diferenças (PLD) (ID: DO-005)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Preços de Liquidação de Diferenças (PLD)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Matriz horária e semanal contendo a precificação da energia elétrica em R$/MWh publicada diariamente pela CCEE para cada submercado elétrico nacional.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, da CCEE e as regras nacionais de segurança da informação e privacidade de dados (LGPD), garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Capacidades de Negócio que Consomem/Produzem (Business Capabilities N3):**
    *   [/cap-l3-analise-de-mercado-de-energia](Capacidade Analise De Mercado De Energia)
    *   [/cap-l3-gestao-de-risco-de-preco](Capacidade Gestao De Risco De Preco)
*   **Sistemas e Aplicações que Manipulam (Applications):**
    *   [/applications/app-erp-gestao-financeira](Aplicação Erp Gestao Financeira)
    *   [/applications/app-erp-tesouraria](Aplicação Erp Tesouraria)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `submercado` | String (Enum) | Submercado de referência (SE_CO, SUL, NORDESTE, NORTE). |
| `data_referencia` | Date | Data de validade do preço horário apurado (YYYY-MM-DD). |
| `hora_referencia` | Integer | Hora do dia correspondente ao PLD horário (faixa de 1 a 24). |
| `valor_pld_mwh` | Float | Valor monetário do Preço de Liquidação de Diferenças (R$/MWh). |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "submercado": "SE_CO",
  "data_referencia": "2026-07-06",
  "hora_referencia": 14,
  "valor_pld_mwh": 142.50
}
```

## # Citations

1. [Manual de Governança de Dados PowerupOKC] - Estabelece as regras de classificação de segurança e sensibilidade das informações corporativas e reguladas.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
