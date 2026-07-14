---
id: DO-112
name: "Conjunto de Usinas"
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
  - "Ativos"
  - "Geração e Transmissão"
  - "LeanIX-v4"
---

# Conjunto de Usinas (DO-112)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Conjunto de Usinas** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Estrutura lógica definida pelo ONS para agrupar e consolidar o despacho de usinas eológicas e fotovoltaicas menores na rede de operação.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Ativos / Geração e Transmissão
*   **Sistemas e Aplicações que Manipulam (Applications):** GMS, ONS
*   **Sistema de Registro Canônico (System of Truth):** GMS (Generation Management System)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `id_ons_conjunto` | String (ID) | Atributo técnico representando o campo mestre 'id_ons_conjunto'. |
| `nom_conjunto` | String | Atributo técnico representando o campo mestre 'nom_conjunto'. |
| `nom_subsistema` | String | Atributo técnico representando o campo mestre 'nom_subsistema'. |
| `estad_id` | String (ID) | Atributo técnico representando o campo mestre 'estad_id'. |
| `id_tipousina` | String (ID) | Atributo técnico representando o campo mestre 'id_tipousina'. |
| `dat_iniciorelacionamento` | DateTime | Atributo técnico representando o campo mestre 'dat_iniciorelacionamento'. |
| `dat_fimrelacionamento.` | DateTime | Atributo técnico representando o campo mestre 'dat_fimrelacionamento.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_ons_conjunto": "REF-DO-112-001",
  "nom_conjunto": "Dados de Exemplo",
  "nom_subsistema": "Dados de Exemplo",
  "estad_id": "REF-DO-112-001",
  "id_tipousina": "REF-DO-112-001"
}
```

## # Citations

1. ONS: Procedimentos de Rede
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
