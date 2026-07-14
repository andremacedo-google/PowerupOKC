---
id: DO-128
name: "Ordem de Serviço Comercial"
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

# Ordem de Serviço Comercial (DO-128)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Ordem de Serviço Comercial** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Solicitação para execução de um serviço de campo comercial (ex: nova ligação, corte, religação), gerada no CIS e despachada via WFM.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Clientes / Atendimento
*   **Sistemas e Aplicações que Manipulam (Applications):** WFM (ClickSoftware), CIS
*   **Sistema de Registro Canônico (System of Truth):** WFM (Workforce Management)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID da OS` | String (ID) | Atributo técnico representando o campo mestre 'ID da OS'. |
| `Tipo de Serviço` | String (Enum) | Atributo técnico representando o campo mestre 'Tipo de Serviço'. |
| `ID da UC` | String (ID) | Atributo técnico representando o campo mestre 'ID da UC'. |
| `Status (Aberta` | String (Enum) | Atributo técnico representando o campo mestre 'Status (Aberta'. |
| `Despachada` | String | Atributo técnico representando o campo mestre 'Despachada'. |
| `Concluída)` | String | Atributo técnico representando o campo mestre 'Concluída)'. |
| `Prioridade` | String (ID) | Atributo técnico representando o campo mestre 'Prioridade'. |
| `Data de Abertura/Fechamento` | DateTime | Atributo técnico representando o campo mestre 'Data de Abertura/Fechamento'. |
| `Equipe Designada` | String | Atributo técnico representando o campo mestre 'Equipe Designada'. |
| `Materiais Utilizados.` | String | Atributo técnico representando o campo mestre 'Materiais Utilizados.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_da_os": "REF-DO-128-001",
  "tipo_de_servico": "Active",
  "id_da_uc": "REF-DO-128-001",
  "status_aberta": "Active",
  "despachada": "Dados de Exemplo"
}
```

## # Citations

1. ANEEL: PRODIST Módulo 3
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
