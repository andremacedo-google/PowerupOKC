---
id: DO-120
name: "Reservatório Hidráulico"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Confidencial (Infraestrutura Crítica)"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Nível 3"
  - "Ativos"
  - "Geração e Transmissão"
  - "LeanIX-v4"
---

# Reservatório Hidráulico (DO-120)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Reservatório Hidráulico** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Reservatório de acumulação de água associado a uma Usina Hidrelétrica (UHE) para fins de coordenação hidráulica e otimização energética pelo ONS.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Ativos / Geração e Transmissão
*   **Sistemas e Aplicações que Manipulam (Applications):** SCADA, GMS, ONS
*   **Sistema de Registro Canônico (System of Truth):** SCADA / GMS (Generation Management System)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ceg` | String | Atributo técnico representando o campo mestre 'ceg'. |
| `nom_usina` | String | Atributo técnico representando o campo mestre 'nom_usina'. |
| `nom_bacia` | String | Atributo técnico representando o campo mestre 'nom_bacia'. |
| `nom_rio` | String | Atributo técnico representando o campo mestre 'nom_rio'. |
| `val_volutiltot` | Float | Atributo técnico representando o campo mestre 'val_volutiltot'. |
| `val_volmax` | Float | Atributo técnico representando o campo mestre 'val_volmax'. |
| `val_volmin (hm³)` | Float | Atributo técnico representando o campo mestre 'val_volmin (hm³)'. |
| `val_cotamaxima` | Float | Atributo técnico representando o campo mestre 'val_cotamaxima'. |
| `val_cotaminima (m).` | Float | Atributo técnico representando o campo mestre 'val_cotaminima (m).'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "ceg": "Dados de Exemplo",
  "nom_usina": "Dados de Exemplo",
  "nom_bacia": "Dados de Exemplo",
  "nom_rio": "Dados de Exemplo",
  "val_volutiltot": 150.45
}
```

## # Citations

1. ONS: Procedimentos de Rede (EAR / Planejamento)
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
