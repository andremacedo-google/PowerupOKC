---
id: DO-154
name: "Centro de Custo"
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

# Centro de Custo (DO-154)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Centro de Custo** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Elemento financeiro básico usado para acumular e categorizar despesas operacionais (OPEX) por departamento, equipe de campo ou centro operacional (ex: COD, COT).

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Financeiro
*   **Sistemas e Aplicações que Manipulam (Applications):** ERP (SAP S/4HANA CO)
*   **Sistema de Registro Canônico (System of Truth):** ERP (SAP Controlling)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `Código do Centro de Custo` | Float | Atributo técnico representando o campo mestre 'Código do Centro de Custo'. |
| `Nome` | String | Atributo técnico representando o campo mestre 'Nome'. |
| `Responsável` | String | Atributo técnico representando o campo mestre 'Responsável'. |
| `Centro de Lucro Relacionado` | String | Atributo técnico representando o campo mestre 'Centro de Lucro Relacionado'. |
| `Grupo de Custos.` | Float | Atributo técnico representando o campo mestre 'Grupo de Custos.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "codigo_do_centro_de_": "REF-DO-154-001",
  "nome": "Dados de Exemplo",
  "responsavel": "Dados de Exemplo",
  "centro_de_lucro_rela": "Dados de Exemplo",
  "grupo_de_custos": 150.45
}
```

## # Citations

1. ANEEL: PRORET Submódulo 2.2 - PMSO, Controle de Despesas Operacionais (OPEX)
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
