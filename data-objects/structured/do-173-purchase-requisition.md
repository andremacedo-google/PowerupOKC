---
id: DO-173
name: "Purchase Requisition"
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
  - "Suprimentos"
  - "LeanIX-v4"
---

# Purchase Requisition (DO-173)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Purchase Requisition** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Requisição de Compra (PR) interna gerada pelas equipes operacionais de rede ou de projetos para solicitar materiais ou serviços, iniciando o fluxo de sourcing e aprovação orçamentária.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Suprimentos
*   **Sistemas e Aplicações que Manipulam (Applications):** ERP (SAP MM), BSM (Coupa / Ariba)
*   **Sistema de Registro Canônico (System of Truth):** BSM (Coupa / Ariba)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID da Requisição (PR Number)` | String (ID) | Atributo técnico representando o campo mestre 'ID da Requisição (PR Number)'. |
| `Área Solicitante` | String | Atributo técnico representando o campo mestre 'Área Solicitante'. |
| `Código do Material/Serviço` | String | Atributo técnico representando o campo mestre 'Código do Material/Serviço'. |
| `Quantidade Estimada` | String (ID) | Atributo técnico representando o campo mestre 'Quantidade Estimada'. |
| `Valor Estimado` | Float | Atributo técnico representando o campo mestre 'Valor Estimado'. |
| `Código do Elemento PEP / Centro de Custo` | Float | Atributo técnico representando o campo mestre 'Código do Elemento PEP / Centro de Custo'. |
| `Fluxo de Aprovações.` | String | Atributo técnico representando o campo mestre 'Fluxo de Aprovações.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_da_requisicao_pr_": "REF-DO-173-001",
  "area_solicitante": "Dados de Exemplo",
  "codigo_do_material_s": "REF-DO-173-001",
  "quantidade_estimada": "REF-DO-173-001",
  "valor_estimado": 150.45
}
```

## # Citations

1. Início do Processo de Suprimentos / Planejamento de CAPEX
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
