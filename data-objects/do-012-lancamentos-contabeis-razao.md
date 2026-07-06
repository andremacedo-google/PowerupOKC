---
id: DO-012
name: "Lançamentos Contábeis e Razão"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Confidencial (Financeiro)"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Corporativo"
  - "LeanIX-v4"
---

# Lançamentos Contábeis e Razão (ID: DO-012)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Lançamentos Contábeis e Razão** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Dados financeiros de lançamentos diários, balancetes de verificação, notas fiscais e relatórios contábeis da corporação.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, da CCEE e as regras nacionais de segurança da informação e privacidade de dados (LGPD), garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Capacidades de Negócio que Consomem/Produzem (Business Capabilities N3):**
    *   [/cap-l3-contabilidade-e-fechamento-financeiro](Capacidade Contabilidade E Fechamento Financeiro)
    *   [/cap-l3-gestao-de-tesouraria](Capacidade Gestao De Tesouraria)
*   **Sistemas e Aplicações que Manipulam (Applications):**
    *   [/applications/app-erp-gestao-financeira](Aplicação Erp Gestao Financeira)
    *   [/applications/app-erp-tesouraria](Aplicação Erp Tesouraria)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `numero_documento_co` | String | Código exclusivo de lançamento contábil no livro contábil (Universal Journal). |
| `data_lancamento` | Date | Data efetiva do lançamento ou variação fiscal (YYYY-MM-DD). |
| `id_conta_geral` | String | ID da conta contábil correspondente do plano de contas mestre. |
| `centro_custo_debitado` | String | ID do centro de custo corporativo para apropriação de despesas. |
| `valor_lancamento_r` | Decimal | Montante monetário creditado ou debitado (R$). |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "numero_documento_co": "DOC-FI-1004291",
  "data_lancamento": "2026-07-06",
  "id_conta_geral": "33411022",
  "centro_custo_debitado": "CC-CSC-SUPLEMENTO",
  "valor_lancamento_r": 4500.00
}
```

## # Citations

1. [Manual de Governança de Dados PowerupOKC] - Estabelece as regras de classificação de segurança e sensibilidade das informações corporativas e reguladas.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
