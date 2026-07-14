---
id: DO-170
name: "Mestre de Materiais"
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

# Mestre de Materiais (DO-170)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Mestre de Materiais** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Item de catálogo corporativo com especificações técnicas e contábeis de materiais, pré-requisito para processos de aquisição.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Suprimentos
*   **Sistemas e Aplicações que Manipulam (Applications):** ERP (SAP MM)
*   **Sistema de Registro Canônico (System of Truth):** ERP (SAP MM)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `Código do Material` | String | Atributo técnico representando o campo mestre 'Código do Material'. |
| `Descrição` | String | Atributo técnico representando o campo mestre 'Descrição'. |
| `Grupo de Mercadoria` | String | Atributo técnico representando o campo mestre 'Grupo de Mercadoria'. |
| `Unidade de Medida` | String (ID) | Atributo técnico representando o campo mestre 'Unidade de Medida'. |
| `Classificação Regulatória (Unidade de Cadastro - UC ou Componente Menor - COM).` | String (ID) | Atributo técnico representando o campo mestre 'Classificação Regulatória (Unidade de Cadastro - UC ou Componente Menor - COM).'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "codigo_do_material": "REF-DO-170-001",
  "descricao": "Dados de Exemplo",
  "grupo_de_mercadoria": "Dados de Exemplo",
  "unidade_de_medida": "REF-DO-170-001",
  "classificacao_regula": "Dados de Exemplo"
}
```

## # Citations

1. Processo de Compras
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
