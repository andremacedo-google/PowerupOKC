---
id: DO-162
name: "Programa"
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

# Programa (DO-162)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Programa** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Agrupamento de múltiplos projetos de investimento (CAPEX) interconectados gerenciados de forma coordenada para atingir metas de expansão de rede ou conformidade regulatória.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Financeiro
*   **Sistemas e Aplicações que Manipulam (Applications):** ERP (SAP PPM / IM)
*   **Sistema de Registro Canônico (System of Truth):** ERP (SAP PPM)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Programa` | String (ID) | Atributo técnico representando o campo mestre 'ID do Programa'. |
| `Nome do Programa` | String | Atributo técnico representando o campo mestre 'Nome do Programa'. |
| `Direcionador Estratégico` | String | Atributo técnico representando o campo mestre 'Direcionador Estratégico'. |
| `Orçamento Total` | String | Atributo técnico representando o campo mestre 'Orçamento Total'. |
| `Benefício Estimado` | String | Atributo técnico representando o campo mestre 'Benefício Estimado'. |
| `Data de Início/Fim` | DateTime | Atributo técnico representando o campo mestre 'Data de Início/Fim'. |
| `Diretoria Responsável.` | String | Atributo técnico representando o campo mestre 'Diretoria Responsável.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_programa": "REF-DO-162-001",
  "nome_do_programa": "Dados de Exemplo",
  "direcionador_estrate": "Dados de Exemplo",
  "orcamento_total": "Dados de Exemplo",
  "beneficio_estimado": "Dados de Exemplo"
}
```

## # Citations

1. ANEEL: P&D, Eficiência Energética (PEE), Luz para Todos / Planejamento de CAPEX
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
