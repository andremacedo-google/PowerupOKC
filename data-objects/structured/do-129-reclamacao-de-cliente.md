---
id: DO-129
name: "Reclamação de Cliente"
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
  - "Clientes"
  - "Atendimento"
  - "LeanIX-v4"
---

# Reclamação de Cliente (DO-129)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Reclamação de Cliente** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Registro de uma insatisfação ou solicitação do cliente em canais de atendimento (ex: falta de energia, contestação de fatura).

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Clientes / Atendimento
*   **Sistemas e Aplicações que Manipulam (Applications):** CRM, Contact Center
*   **Sistema de Registro Canônico (System of Truth):** CRM

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID da Reclamação` | String (ID) | Atributo técnico representando o campo mestre 'ID da Reclamação'. |
| `ID do Cliente/UC` | String (ID) | Atributo técnico representando o campo mestre 'ID do Cliente/UC'. |
| `Motivo` | String | Atributo técnico representando o campo mestre 'Motivo'. |
| `Data` | DateTime | Atributo técnico representando o campo mestre 'Data'. |
| `Status` | String (Enum) | Atributo técnico representando o campo mestre 'Status'. |
| `Canal de Entrada (Call Center` | String | Atributo técnico representando o campo mestre 'Canal de Entrada (Call Center'. |
| `Ouvidoria).` | String (ID) | Atributo técnico representando o campo mestre 'Ouvidoria).'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_da_reclamacao": "REF-DO-129-001",
  "id_do_cliente_uc": "REF-DO-129-001",
  "motivo": "Dados de Exemplo",
  "data": "2026-07-14T06:55:00Z",
  "status": "Active"
}
```

## # Citations

1. Resoluções ANEEL (Indicadores de Atendimento)
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
