---
id: DO-152
name: "Ativo Regulatório (BRR)"
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

# Ativo Regulatório (BRR) (DO-152)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Ativo Regulatório (BRR)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Representa o valor do ativo físico que compõe a Base de Remuneração Regulatória (BRR). Gerenciado via Áreas de Avaliação paralelas no ERP, com regras distintas do contábil.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Financeiro
*   **Sistemas e Aplicações que Manipulam (Applications):** ERP (SAP FI-AA), Add-on Regulatório
*   **Sistema de Registro Canônico (System of Truth):** ERP (SAP FI-AA / Módulo Regulatório)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Ativo Regulatório` | String (ID) | Atributo técnico representando o campo mestre 'ID do Ativo Regulatório'. |
| `Código da Unidade de Adição e Retirada (UAR)` | String (ID) | Atributo técnico representando o campo mestre 'Código da Unidade de Adição e Retirada (UAR)'. |
| `Valor Novo de Reposição (VNR)` | Float | Atributo técnico representando o campo mestre 'Valor Novo de Reposição (VNR)'. |
| `Quota de Reintegração Regulatória (QRR)` | String | Atributo técnico representando o campo mestre 'Quota de Reintegração Regulatória (QRR)'. |
| `Vida Útil Regulatória.` | String (ID) | Atributo técnico representando o campo mestre 'Vida Útil Regulatória.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_ativo_regulato": "REF-DO-152-001",
  "codigo_da_unidade_de": "REF-DO-152-001",
  "valor_novo_de_reposi": 150.45,
  "quota_de_reintegraca": "Dados de Exemplo",
  "vida_util_regulatori": "REF-DO-152-001"
}
```

## # Citations

1. ANEEL: MCPSE, Revisão Tarifária
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
