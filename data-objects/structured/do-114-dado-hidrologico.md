---
id: DO-114
name: "Dado Hidrológico"
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

# Dado Hidrológico (DO-114)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Dado Hidrológico** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Informações sobre os níveis e vazões dos reservatórios das usinas hidrelétricas, vitais para o planejamento energético.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Ativos / Geração e Transmissão
*   **Sistemas e Aplicações que Manipulam (Applications):** SCADA, Sistemas de Previsão
*   **Sistema de Registro Canônico (System of Truth):** SCADA

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Reservatório` | String (ID) | Atributo técnico representando o campo mestre 'ID do Reservatório'. |
| `Data/Hora` | DateTime | Atributo técnico representando o campo mestre 'Data/Hora'. |
| `Nível (m)` | String | Atributo técnico representando o campo mestre 'Nível (m)'. |
| `Vazão Afluente (m³/s)` | String | Atributo técnico representando o campo mestre 'Vazão Afluente (m³/s)'. |
| `Vazão Defluente/Turbinada (m³/s).` | String | Atributo técnico representando o campo mestre 'Vazão Defluente/Turbinada (m³/s).'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_reservatorio": "REF-DO-114-001",
  "data_hora": "2026-07-14T06:55:00Z",
  "nivel_m": "Dados de Exemplo",
  "vazao_afluente_m_s": "Dados de Exemplo",
  "vazao_defluente_turb": "Dados de Exemplo"
}
```

## # Citations

1. ONS: Procedimentos de Rede
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
