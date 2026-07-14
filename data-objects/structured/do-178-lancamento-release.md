---
id: DO-178
name: "Lançamento (Release)"
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

# Lançamento (Release) (DO-178)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Lançamento (Release)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Registro mestre que coordena o planejamento, empacotamento e a implantação conjunta de um conjunto de mudanças aprovadas, novas versões de software ou correções definitivas de segurança no ambiente produtivo de TI/TO da concessionária de energia.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Tecnologia da Informação
*   **Sistemas e Aplicações que Manipulam (Applications):** ServiceNow ITSM (Release Management), Jira Software / GitLab, Azure DevOps
*   **Sistema de Registro Canônico (System of Truth):** ServiceNow ITSM / Azure DevOps

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Lançamento` | String (ID) | Atributo técnico representando o campo mestre 'ID do Lançamento'. |
| `Nome do Release` | String | Atributo técnico representando o campo mestre 'Nome do Release'. |
| `Versão do Software` | String | Atributo técnico representando o campo mestre 'Versão do Software'. |
| `Status (Planejado` | String (Enum) | Atributo técnico representando o campo mestre 'Status (Planejado'. |
| `Em Desenvolvimento` | String | Atributo técnico representando o campo mestre 'Em Desenvolvimento'. |
| `Em Teste` | String | Atributo técnico representando o campo mestre 'Em Teste'. |
| `Homologado` | String | Atributo técnico representando o campo mestre 'Homologado'. |
| `Implantado)` | String | Atributo técnico representando o campo mestre 'Implantado)'. |
| `Lista de Mudanças (Changes) Integradas` | String | Atributo técnico representando o campo mestre 'Lista de Mudanças (Changes) Integradas'. |
| `CIs Afetados` | String | Atributo técnico representando o campo mestre 'CIs Afetados'. |
| `Cronograma de Implantação` | String | Atributo técnico representando o campo mestre 'Cronograma de Implantação'. |
| `Responsável (Release Manager).` | String | Atributo técnico representando o campo mestre 'Responsável (Release Manager).'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_lancamento": "REF-DO-178-001",
  "nome_do_release": "Dados de Exemplo",
  "versao_do_software": "Dados de Exemplo",
  "status_planejado": "Active",
  "em_desenvolvimento": "Dados de Exemplo"
}
```

## # Citations

1. Gestão de Liberações e Implantação (Release and Deployment - ITIL v4), Ciclo de Desenvolvimento de Software Seguro (DevSecOps).
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
