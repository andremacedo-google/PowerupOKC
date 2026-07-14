---
id: DO-123
name: "Unidade Geradora (Equipamento)"
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

# Unidade Geradora (Equipamento) (DO-123)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Unidade Geradora (Equipamento)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Equipamento individual de geração (turbina/gerador, conjunto de painéis) pertencente a uma Usina de Geração, avaliado em tempo de comissionamento e operação comercial.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Ativos / Geração e Transmissão
*   **Sistemas e Aplicações que Manipulam (Applications):** GMS, EAM (SAP PM), SCADA
*   **Sistema de Registro Canônico (System of Truth):** GMS (Generation Management System) / EAM

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `cod_equipamento` | String (ID) | Atributo técnico representando o campo mestre 'cod_equipamento'. |
| `num_unidadegeradora` | String (ID) | Atributo técnico representando o campo mestre 'num_unidadegeradora'. |
| `nom_unidadegeradora` | String (ID) | Atributo técnico representando o campo mestre 'nom_unidadegeradora'. |
| `val_potenciaefetiva (MW)` | Float | Atributo técnico representando o campo mestre 'val_potenciaefetiva (MW)'. |
| `nom_combustivel` | String | Atributo técnico representando o campo mestre 'nom_combustivel'. |
| `dat_entradateste` | DateTime | Atributo técnico representando o campo mestre 'dat_entradateste'. |
| `dat_entradaoperacao.` | DateTime | Atributo técnico representando o campo mestre 'dat_entradaoperacao.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "cod_equipamento": "REF-DO-123-001",
  "num_unidadegeradora": "REF-DO-123-001",
  "nom_unidadegeradora": "REF-DO-123-001",
  "val_potenciaefetiva_": 150.45,
  "nom_combustivel": "Dados de Exemplo"
}
```

## # Citations

1. ONS: Procedimentos de Rede (Submódulo 9.2)
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
