---
id: DO-164
name: "Projeto de Investimento"
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
  - "Projetos e Investimentos"
  - "LeanIX-v4"
---

# Projeto de Investimento (DO-164)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Projeto de Investimento** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Estrutura no ERP (SAP PS) que representa um projeto de capital (CAPEX) (ex: construção de subestação) e acumula os custos em Elementos PEP.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Projetos e Investimentos
*   **Sistemas e Aplicações que Manipulam (Applications):** ERP (SAP PS, IM)
*   **Sistema de Registro Canônico (System of Truth):** ERP (SAP PS)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Projeto/PEP` | String (ID) | Atributo técnico representando o campo mestre 'ID do Projeto/PEP'. |
| `Descrição` | String | Atributo técnico representando o campo mestre 'Descrição'. |
| `Orçamento` | String | Atributo técnico representando o campo mestre 'Orçamento'. |
| `Cronograma (EAP)` | String | Atributo técnico representando o campo mestre 'Cronograma (EAP)'. |
| `Status` | String (Enum) | Atributo técnico representando o campo mestre 'Status'. |
| `Custos Acumulados (Ativo Imobilizado em Curso - AIC / AuC).` | Float | Atributo técnico representando o campo mestre 'Custos Acumulados (Ativo Imobilizado em Curso - AIC / AuC).'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_projeto_pep": "REF-DO-164-001",
  "descricao": "Dados de Exemplo",
  "orcamento": "Dados de Exemplo",
  "cronograma_eap": "Dados de Exemplo",
  "status": "Active"
}
```

## # Citations

1. Ciclo de Vida do Ativo / CAPEX
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
