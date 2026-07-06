---
id: DO-013
name: "Minutas e Termos Contratuais"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Confidencial"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Corporativo"
  - "LeanIX-v4"
---

# Minutas e Termos Contratuais (ID: DO-013)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Minutas e Termos Contratuais** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Contratos de fornecedores de EPC, contratos PPA de venda de energia a longo prazo e termos de confidencialidade (NDA).

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, da CCEE e as regras nacionais de segurança da informação e privacidade de dados (LGPD), garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Capacidades de Negócio que Consomem/Produzem (Business Capabilities N3):**
    *   [/cap-l3-gestao-de-contratos](Capacidade Gestao De Contratos)
    *   [/cap-l3-compras-estrategicas-procurement](Capacidade Compras Estrategicas Procurement)
*   **Sistemas e Aplicações que Manipulam (Applications):**
    *   [/applications/app-clm-gestao-contratos](Aplicação Clm Gestao Contratos)
    *   [/applications/app-grc-governanca-riscos](Aplicação Grc Governanca Riscos)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `id_contrato` | String | Código identificador do documento de contrato no sistema CLM. |
| `tipo_contrato` | String | Classificação do acordo (ex: COMPRA_EQUIPAMENTO, PRESTACAO_SERVICOS, PPA). |
| `cnpj_fornecedor` | String | CNPJ da empresa fornecedora ou parceira homologada. |
| `valor_total_contrato_r` | Decimal | Montante monetário total sob risco empenhado no contrato (R$). |
| `vigencia_fim` | Date | Data final do período de vigência para conformidade e renovação. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_contrato": "CON-2026-00412",
  "tipo_contrato": "COMPRA_EQUIPAMENTO",
  "cnpj_fornecedor": "98.765.432/0001-11",
  "valor_total_contrato_r": 1250000.00,
  "vigencia_fim": "2028-12-31"
}
```

## # Citations

1. [Manual de Governança de Dados PowerupOKC] - Estabelece as regras de classificação de segurança e sensibilidade das informações corporativas e reguladas.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
