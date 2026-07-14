---
id: DO-155
name: "Centro de Lucro"
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

# Centro de Lucro (DO-155)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Centro de Lucro** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Elemento de estrutura organizacional no ERP usado para rastrear receitas, despesas e margens associadas a segmentos de negócio (G, T, D, C) ou produtos de valor agregado.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Financeiro
*   **Sistemas e Aplicações que Manipulam (Applications):** ERP (SAP S/4HANA CO/FI)
*   **Sistema de Registro Canônico (System of Truth):** ERP (SAP Controlling)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `Código do Centro de Lucro` | String | Atributo técnico representando o campo mestre 'Código do Centro de Lucro'. |
| `Nome` | String | Atributo técnico representando o campo mestre 'Nome'. |
| `Segmento de Negócio` | String | Atributo técnico representando o campo mestre 'Segmento de Negócio'. |
| `Responsável` | String | Atributo técnico representando o campo mestre 'Responsável'. |
| `Hierarquia de Centros de Lucro.` | String | Atributo técnico representando o campo mestre 'Hierarquia de Centros de Lucro.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "codigo_do_centro_de_": "REF-DO-155-001",
  "nome": "Dados de Exemplo",
  "segmento_de_negocio": "Dados de Exemplo",
  "responsavel": "Dados de Exemplo",
  "hierarquia_de_centro": "Dados de Exemplo"
}
```

## # Citations

1. Contabilidade Geral / Relatórios por Segmento (IFRS 8) e Regulatório
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
