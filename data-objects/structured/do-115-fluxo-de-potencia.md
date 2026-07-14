---
id: DO-115
name: "Fluxo de Potência"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Confidencial (Infraestrutura Crítica)"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Nível 3"
  - "Ativos"
  - "Geração e Transmissão"
  - "LeanIX-v4"
---

# Fluxo de Potência (DO-115)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Fluxo de Potência** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Objeto de dados dinâmico e em tempo real que representa a quantidade de energia ativa e reativa fluindo através da rede de geração e transmissão.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Ativos / Geração e Transmissão
*   **Sistemas e Aplicações que Manipulam (Applications):** EMS, ADMS, SCADA
*   **Sistema de Registro Canônico (System of Truth):** ADMS / EMS (Energy Management System)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Elemento de Rede` | String (ID) | Atributo técnico representando o campo mestre 'ID do Elemento de Rede'. |
| `Timestamp` | DateTime | Atributo técnico representando o campo mestre 'Timestamp'. |
| `Potência Ativa (MW)` | Float | Atributo técnico representando o campo mestre 'Potência Ativa (MW)'. |
| `Potência Reativa (MVAr)` | Float | Atributo técnico representando o campo mestre 'Potência Reativa (MVAr)'. |
| `Tensão (kV)` | String | Atributo técnico representando o campo mestre 'Tensão (kV)'. |
| `Corrente (A).` | String | Atributo técnico representando o campo mestre 'Corrente (A).'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_elemento_de_re": "REF-DO-115-001",
  "timestamp": "2026-07-14T06:55:00Z",
  "potencia_ativa_mw": 150.45,
  "potencia_reativa_mva": 150.45,
  "tensao_kv": "Dados de Exemplo"
}
```

## # Citations

1. ONS: Procedimentos de Rede
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
