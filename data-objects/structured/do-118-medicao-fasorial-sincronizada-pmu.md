---
id: DO-118
name: "Medição Fasorial Sincronizada (PMU)"
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
  - "Ativos"
  - "Geração e Transmissão"
  - "LeanIX-v4"
---

# Medição Fasorial Sincronizada (PMU) (DO-118)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Medição Fasorial Sincronizada (PMU)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Dados de alta frequência sobre tensão, corrente e ângulo de fase da rede, usados para monitoramento dinâmico da estabilidade do SIN.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Ativos / Geração e Transmissão
*   **Sistemas e Aplicações que Manipulam (Applications):** PIMS/Historian, WAMS
*   **Sistema de Registro Canônico (System of Truth):** PIMS (Plant Information Management System)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `Timestamp` | DateTime | Atributo técnico representando o campo mestre 'Timestamp'. |
| `ID da PMU` | String (ID) | Atributo técnico representando o campo mestre 'ID da PMU'. |
| `Magnitude da Tensão/Corrente` | String | Atributo técnico representando o campo mestre 'Magnitude da Tensão/Corrente'. |
| `Ângulo de Fase` | String | Atributo técnico representando o campo mestre 'Ângulo de Fase'. |
| `Frequência.` | String | Atributo técnico representando o campo mestre 'Frequência.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "timestamp": "2026-07-14T06:55:00Z",
  "id_da_pmu": "REF-DO-118-001",
  "magnitude_da_tensao_": "Dados de Exemplo",
  "angulo_de_fase": "Dados de Exemplo",
  "frequencia": "Dados de Exemplo"
}
```

## # Citations

1. ONS: Procedimentos de Rede
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
