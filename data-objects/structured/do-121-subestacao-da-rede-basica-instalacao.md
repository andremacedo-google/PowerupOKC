---
id: DO-121
name: "Subestação da Rede Básica (Instalação)"
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

# Subestação da Rede Básica (Instalação) (DO-121)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Subestação da Rede Básica (Instalação)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Nó de alta tensão da Rede de Operação (igual ou superior a 69kV) que concentra os barramentos de interligação física do SIN.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Ativos / Geração e Transmissão
*   **Sistemas e Aplicações que Manipulam (Applications):** EMS, SCADA, GIS
*   **Sistema de Registro Canônico (System of Truth):** EMS (Energy Management System)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `id_subestacao` | String (ID) | Atributo técnico representando o campo mestre 'id_subestacao'. |
| `nom_subestacao` | String | Atributo técnico representando o campo mestre 'nom_subestacao'. |
| `id_estacao` | String (ID) | Atributo técnico representando o campo mestre 'id_estacao'. |
| `val_niveltensao (kV)` | Float | Atributo técnico representando o campo mestre 'val_niveltensao (kV)'. |
| `num_barra` | String | Atributo técnico representando o campo mestre 'num_barra'. |
| `id_subsistema` | String (ID) | Atributo técnico representando o campo mestre 'id_subsistema'. |
| `estad_id` | String (ID) | Atributo técnico representando o campo mestre 'estad_id'. |
| `coord_geograficas.` | String | Atributo técnico representando o campo mestre 'coord_geograficas.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_subestacao": "REF-DO-121-001",
  "nom_subestacao": "Dados de Exemplo",
  "id_estacao": "REF-DO-121-001",
  "val_niveltensao_kv": 150.45,
  "num_barra": "Dados de Exemplo"
}
```

## # Citations

1. ONS: Procedimentos de Rede (Submódulo 2.1)
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
