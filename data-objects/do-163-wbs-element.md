---
id: DO-163
name: "WBS Element"
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

# WBS Element (DO-163)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **WBS Element** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Elemento PEP (Projeto Estruturado do Projeto) do SAP PS que atua como coletor de custos de investimentos em andamento (CAPEX) de projetos de rede antes de sua unitização regulatória.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Financeiro
*   **Sistemas e Aplicações que Manipulam (Applications):** ERP (SAP PS)
*   **Sistema de Registro Canônico (System of Truth):** ERP (SAP PS)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Elemento PEP` | String (ID) | Atributo técnico representando o campo mestre 'ID do Elemento PEP'. |
| `ID do Projeto Pai` | String (ID) | Atributo técnico representando o campo mestre 'ID do Projeto Pai'. |
| `Descrição` | String | Atributo técnico representando o campo mestre 'Descrição'. |
| `Orçamento Alocado` | String | Atributo técnico representando o campo mestre 'Orçamento Alocado'. |
| `Tipo (Real/Estatístico)` | String (Enum) | Atributo técnico representando o campo mestre 'Tipo (Real/Estatístico)'. |
| `Custos Acumulados (AuC)` | Float | Atributo técnico representando o campo mestre 'Custos Acumulados (AuC)'. |
| `Centro de Custo Responsável.` | Float | Atributo técnico representando o campo mestre 'Centro de Custo Responsável.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_elemento_pep": "REF-DO-163-001",
  "id_do_projeto_pai": "REF-DO-163-001",
  "descricao": "Dados de Exemplo",
  "orcamento_alocado": "Dados de Exemplo",
  "tipo_real_estatistic": "Active"
}
```

## # Citations

1. ANEEL: PRORET Submódulo 2.3 - Unitização de Ativos / BRR, Ciclo de Vida do Ativo
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
