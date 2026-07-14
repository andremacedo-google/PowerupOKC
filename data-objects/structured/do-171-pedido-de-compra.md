---
id: DO-171
name: "Pedido de Compra"
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

# Pedido de Compra (DO-171)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Pedido de Compra** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Documento que formaliza a aquisição de um material ou serviço de um fornecedor, vinculando o custo ao projeto de investimento (CAPEX).

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Suprimentos
*   **Sistemas e Aplicações que Manipulam (Applications):** ERP (SAP MM), SRM
*   **Sistema de Registro Canônico (System of Truth):** ERP (SAP MM)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Pedido` | String (ID) | Atributo técnico representando o campo mestre 'ID do Pedido'. |
| `Fornecedor` | String | Atributo técnico representando o campo mestre 'Fornecedor'. |
| `Material` | String | Atributo técnico representando o campo mestre 'Material'. |
| `Quantidade` | String (ID) | Atributo técnico representando o campo mestre 'Quantidade'. |
| `Preço` | String | Atributo técnico representando o campo mestre 'Preço'. |
| `Classificação Contábil (Elemento PEP / Ordem de Imobilização - ODI).` | String | Atributo técnico representando o campo mestre 'Classificação Contábil (Elemento PEP / Ordem de Imobilização - ODI).'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_pedido": "REF-DO-171-001",
  "fornecedor": "Dados de Exemplo",
  "material": "Dados de Exemplo",
  "quantidade": "REF-DO-171-001",
  "preco": 150.45
}
```

## # Citations

1. Processo de Compras
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
