---
id: DO-117
name: "Linha de Transmissão (LT)"
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

# Linha de Transmissão (LT) (DO-117)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Linha de Transmissão (LT)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Instalações de alta tensão (igual ou superior a 230kV) que interligam as subestações do SIN, controladas pelo ONS e mantidas sob contratos de concessão.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Ativos / Geração e Transmissão
*   **Sistemas e Aplicações que Manipulam (Applications):** EAM (SAP PM), EMS, GIS
*   **Sistema de Registro Canônico (System of Truth):** EAM (SAP PM) / EMS / GIS

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `nom_linhadetransmissao` | String | Atributo técnico representando o campo mestre 'nom_linhadetransmissao'. |
| `cod_equipamento` | String (ID) | Atributo técnico representando o campo mestre 'cod_equipamento'. |
| `val_comprimento (km)` | Float | Atributo técnico representando o campo mestre 'val_comprimento (km)'. |
| `val_resistencia` | Float | Atributo técnico representando o campo mestre 'val_resistencia'. |
| `val_reatancia` | Float | Atributo técnico representando o campo mestre 'val_reatancia'. |
| `val_shunt` | Float | Atributo técnico representando o campo mestre 'val_shunt'. |
| `nom_agenteproprietario` | String | Atributo técnico representando o campo mestre 'nom_agenteproprietario'. |
| `limite_térmico (ampacidade).` | String (ID) | Atributo técnico representando o campo mestre 'limite_térmico (ampacidade).'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "nom_linhadetransmiss": "Dados de Exemplo",
  "cod_equipamento": "REF-DO-117-001",
  "val_comprimento_km": 150.45,
  "val_resistencia": 150.45,
  "val_reatancia": 150.45
}
```

## # Citations

1. ONS: Procedimentos de Rede (Submódulo 2.7) / ANEEL
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
