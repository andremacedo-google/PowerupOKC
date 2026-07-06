---
id: DO-001
name: "Leituras de Telemetria (AMI)"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Restrito (LGPD - Dados de Consumo)"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Operações"
  - "LeanIX-v4"
---

# Leituras de Telemetria (AMI) (ID: DO-001)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Leituras de Telemetria (AMI)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Dados de injeção e consumo em tempo real de medidores inteligentes (AMI) instalados em prossumidores e consumidores livres, coletados de forma contínua para fins de faturamento e crítica de medição.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, da CCEE e as regras nacionais de segurança da informação e privacidade de dados (LGPD), garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Capacidades de Negócio que Consomem/Produzem (Business Capabilities N3):**
    *   [/cap-l3-medicao-e-coleta-de-dados](Capacidade Medicao E Coleta De Dados)
    *   [/cap-l3-processamento-de-faturas](Capacidade Processamento De Faturas)
*   **Sistemas e Aplicações que Manipulam (Applications):**
    *   [/applications/app-mdm-gestao-medicao](Aplicação Mdm Gestao Medicao)
    *   [/applications/app-cis-faturamento-comercial](Aplicação Cis Faturamento Comercial)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `id_medidor` | String | Identificador exclusivo do medidor inteligente físico (tag/número de série). |
| `timestamp_leitura` | DateTime (ISO 8601) | Data e hora exata do registro de medição de telemetria. |
| `consumo_ativo_kwh` | Float | Energia elétrica ativa consumida da rede no intervalo (kWh). |
| `injecao_ativa_kwh` | Float | Energia elétrica ativa injetada na rede pelo prossumidor (kWh). |
| `demanda_reativa_kvarh` | Float | Energia reativa consumida ou injetada para controle de fator de potência (kVArh). |
| `alarme_violacao` | Boolean | Sinalizador de integridade física ou abertura de tampa do medidor de campo (exceção VEE). |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_medidor": "MD-AMI-998812",
  "timestamp_leitura": "2026-07-06T14:15:00Z",
  "consumo_ativo_kwh": 1.45,
  "injecao_ativa_kwh": 3.20,
  "demanda_reativa_kvarh": 0.12,
  "alarme_violacao": false
}
```

## # Citations

1. [Manual de Governança de Dados PowerupOKC] - Estabelece as regras de classificação de segurança e sensibilidade das informações corporativas e reguladas.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
