---
id: DO-010
name: "Fatura de Energia (Conta de Luz)"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Restrito (LGPD - Financeiro)"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Clientes"
  - "LeanIX-v4"
---

# Fatura de Energia (Conta de Luz) (ID: DO-010)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Fatura de Energia (Conta de Luz)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Documento contendo faturamento detalhado, tarifas aplicadas (TUSD/TE), impostos (ICMS/PIS/COFINS) e créditos compensados.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, da CCEE e as regras nacionais de segurança da informação e privacidade de dados (LGPD), garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Capacidades de Negócio que Consomem/Produzem (Business Capabilities N3):**
    *   [/cap-l3-processamento-de-faturas](Capacidade Processamento De Faturas)
    *   [/cap-l3-gestao-de-inadimplencia](Capacidade Gestao De Inadimplencia)
*   **Sistemas e Aplicações que Manipulam (Applications):**
    *   [/applications/app-cis-faturamento-comercial](Aplicação Cis Faturamento Comercial)
    *   [/applications/app-crm-relacionamento-cliente](Aplicação Crm Relacionamento Cliente)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `numero_fatura` | String | ID exclusivo da fatura financeira de faturamento elétrico emitido. |
| `id_conta_contrato` | String | Código da conta contrato do parceiro de negócio para cobrança. |
| `valor_te_r` | Decimal | Valor monetário correspondente à Tarifa de Energia (TE). |
| `valor_tusd_r` | Decimal | Valor monetário correspondente à Tarifa de Uso do Sistema de Distribuição (TUSD). |
| `valor_total_fatura_r` | Decimal | Valor total geral faturado da conta elétrico a pagar (R$). |
| `data_vencimento` | Date | Data limite regulatória para o pagamento do débito (YYYY-MM-DD). |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "numero_fatura": "FAT-2026-9908122",
  "id_conta_contrato": "CC-10022312",
  "valor_te_r": 120.45,
  "valor_tusd_r": 185.30,
  "valor_total_fatura_r": 350.75,
  "data_vencimento": "2026-07-20"
}
```

## # Citations

1. [Manual de Governança de Dados PowerupOKC] - Estabelece as regras de classificação de segurança e sensibilidade das informações corporativas e reguladas.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
