---
id: DO-019
name: "Inventário de Peças Sobressalentes (MRO)"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Interno"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Corporativo"
  - "LeanIX-v4"
---

# Inventário de Peças Sobressalentes (MRO) (ID: DO-019)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Inventário de Peças Sobressalentes (MRO)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Dados de estoque de cabos, disjuntores reservas, isoladores de passagem, óleos minerais e postes mantidos nos almoxarifados.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, da CCEE e as regras nacionais de segurança da informação e privacidade de dados (LGPD), garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Capacidades de Negócio que Consomem/Produzem (Business Capabilities N3):**
    *   [/cap-l3-gestao-de-estoques-e-logistica](Capacidade Gestao De Estoques E Logistica)
*   **Sistemas e Aplicações que Manipulam (Applications):**
    *   [/applications/app-gis-georreferenciamento-redes](Aplicação Gis Georreferenciamento Redes)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `id_material_mro` | String | Código identificador do material cadastrado no mestre de materiais ERP (SKU). |
| `nome_peca` | String | Descrição detalhada técnica do componente de campo sobressalente. |
| `quantidade_estoque` | Integer | Unidades de peças fisicamente disponíveis no almoxarifado regional. |
| `ponto_reposicao_minimo` | Integer | Nível crítico de reabastecimento logístico para gerar compra automática. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_material_mro": "SKU-MRO-TRAFO-ISOL-500",
  "nome_peca": "Isolador de Passagem Cerâmica 500kV",
  "quantidade_estoque": 14,
  "ponto_reposicao_minimo": 5
}
```

## # Citations

1. [Manual de Governança de Dados PowerupOKC] - Estabelece as regras de classificação de segurança e sensibilidade das informações corporativas e reguladas.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
