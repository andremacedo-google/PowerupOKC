---
id: DO-105
name: "Evento de Interrupção (DEC/FEC)"
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
  - "Distribuição"
  - "LeanIX-v4"
---

# Evento de Interrupção (DEC/FEC) (DO-105)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Evento de Interrupção (DEC/FEC)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Registro de uma interrupção no fornecimento, detectado pelo SCADA/ADMS, enviado ao CIS para cálculo de compensação (DIC) e apuração de indicadores (DEC/FEC).

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Ativos / Distribuição
*   **Sistemas e Aplicações que Manipulam (Applications):** ADMS, OMS, SCADA, CIS
*   **Sistema de Registro Canônico (System of Truth):** ADMS (OMS - Outage Management System)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Evento` | String (ID) | Atributo técnico representando o campo mestre 'ID do Evento'. |
| `UCs afetadas` | String | Atributo técnico representando o campo mestre 'UCs afetadas'. |
| `Data/Hora de Início e Fim` | DateTime | Atributo técnico representando o campo mestre 'Data/Hora de Início e Fim'. |
| `Duração da Interrupção` | String | Atributo técnico representando o campo mestre 'Duração da Interrupção'. |
| `Causa Provável.` | String | Atributo técnico representando o campo mestre 'Causa Provável.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_evento": "REF-DO-105-001",
  "ucs_afetadas": "Dados de Exemplo",
  "data_hora_de_inicio_": "2026-07-14T06:55:00Z",
  "duracao_da_interrupc": "Dados de Exemplo",
  "causa_provavel": "Dados de Exemplo"
}
```

## # Citations

1. ANEEL: PRODIST Módulo 8
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
