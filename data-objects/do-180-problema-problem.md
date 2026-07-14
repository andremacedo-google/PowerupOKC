---
id: DO-180
name: "Problema (Problem)"
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
  - "Corporativo"
  - "Tecnologia da Informação"
  - "LeanIX-v4"
---

# Problema (Problem) (DO-180)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Problema (Problem)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Registro mestre voltado à análise de causa raiz de um ou mais incidentes recorrentes ou de um incidente de alto impacto sistêmico que afete as operações de TI ou TO da utility (como indisponibilidade momentânea de dados de telemetria). Agrupa múltiplos tickets de incidentes para centralizar a investigação de engenharia de confiabilidade e propor soluções de contorno ou definitivas.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Tecnologia da Informação
*   **Sistemas e Aplicações que Manipulam (Applications):** ServiceNow ITSM (Problem Management), Jira Service Management
*   **Sistema de Registro Canônico (System of Truth):** ServiceNow ITSM

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Problema` | String (ID) | Atributo técnico representando o campo mestre 'ID do Problema'. |
| `Categoria de Impacto` | String | Atributo técnico representando o campo mestre 'Categoria de Impacto'. |
| `Status da Investigação (Sob Análise` | String (Enum) | Atributo técnico representando o campo mestre 'Status da Investigação (Sob Análise'. |
| `Erro Conhecido` | String (ID) | Atributo técnico representando o campo mestre 'Erro Conhecido'. |
| `Resolvido)` | String (ID) | Atributo técnico representando o campo mestre 'Resolvido)'. |
| `Causa Raiz Identificada` | String (ID) | Atributo técnico representando o campo mestre 'Causa Raiz Identificada'. |
| `Erro Conhecido Relacionado (Workaround)` | String (ID) | Atributo técnico representando o campo mestre 'Erro Conhecido Relacionado (Workaround)'. |
| `Lista de Incidentes Vinculados` | String (ID) | Atributo técnico representando o campo mestre 'Lista de Incidentes Vinculados'. |
| `CIs Associados` | String | Atributo técnico representando o campo mestre 'CIs Associados'. |
| `Plano de Ação` | String | Atributo técnico representando o campo mestre 'Plano de Ação'. |
| `Timestamp de Resolução.` | DateTime | Atributo técnico representando o campo mestre 'Timestamp de Resolução.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_problema": "REF-DO-180-001",
  "categoria_de_impacto": "Dados de Exemplo",
  "status_da_investigac": "Active",
  "erro_conhecido": "REF-DO-180-001",
  "resolvido": "REF-DO-180-001"
}
```

## # Citations

1. Gestão de Problemas (causa raiz - ITIL v4), Melhoria Contínua de Processos, Conformidade e Resiliência de Infraestrutura Crítica (DORA / NERC CIP).
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
