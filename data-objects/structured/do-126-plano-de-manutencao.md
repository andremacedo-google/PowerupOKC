---
id: DO-126
name: "Plano de Manutenção"
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
  - "Manutenção"
  - "LeanIX-v4"
---

# Plano de Manutenção (DO-126)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Plano de Manutenção** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Cronograma de atividades de manutenção preventiva para um conjunto de ativos, visando garantir a confiabilidade.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Ativos / Manutenção
*   **Sistemas e Aplicações que Manipulam (Applications):** EAM (IBM Maximo), SAP PM
*   **Sistema de Registro Canônico (System of Truth):** EAM / SAP PM

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Plano` | String (ID) | Atributo técnico representando o campo mestre 'ID do Plano'. |
| `Descrição` | String | Atributo técnico representando o campo mestre 'Descrição'. |
| `Frequência (mensal` | String | Atributo técnico representando o campo mestre 'Frequência (mensal'. |
| `anual)` | String | Atributo técnico representando o campo mestre 'anual)'. |
| `Ativos Associados` | String | Atributo técnico representando o campo mestre 'Ativos Associados'. |
| `Procedimentos Técnicos.` | String | Atributo técnico representando o campo mestre 'Procedimentos Técnicos.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_plano": "REF-DO-126-001",
  "descricao": "Dados de Exemplo",
  "frequencia_mensal": "Dados de Exemplo",
  "anual": "Dados de Exemplo",
  "ativos_associados": "Dados de Exemplo"
}
```

## # Citations

1. Processo de Manutenção (O&M)
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
