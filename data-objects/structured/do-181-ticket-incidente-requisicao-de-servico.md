---
id: DO-181
name: "Ticket (Incidente / Requisição de Serviço)"
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
  - "Corporativo"
  - "Tecnologia da Informação"
  - "LeanIX-v4"
---

# Ticket (Incidente / Requisição de Serviço) (DO-181)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Ticket (Incidente / Requisição de Serviço)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Registro mestre que documenta uma interrupção não planejada de um serviço de TI/TO (Incidente) ou uma solicitação formal de um novo serviço, acesso, hardware ou software pré-aprovado (Requisição de Serviço) por parte de funcionários ou equipes operacionais (como COD/COG). Essencial para a conformidade DORA e governança de incidentes de tecnologia.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Tecnologia da Informação
*   **Sistemas e Aplicações que Manipulam (Applications):** ServiceNow ITSM, Jira Service Management, Freshservice
*   **Sistema de Registro Canônico (System of Truth):** ServiceNow (ou sistema de ITSM adotado)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Ticket` | String (ID) | Atributo técnico representando o campo mestre 'ID do Ticket'. |
| `Tipo (Incidente / Requisição)` | String (ID) | Atributo técnico representando o campo mestre 'Tipo (Incidente / Requisição)'. |
| `Solicitante (ID do Funcionário)` | String (ID) | Atributo técnico representando o campo mestre 'Solicitante (ID do Funcionário)'. |
| `Descrição do Problema/Solicitação` | String | Atributo técnico representando o campo mestre 'Descrição do Problema/Solicitação'. |
| `Prioridade (Crítica` | String (ID) | Atributo técnico representando o campo mestre 'Prioridade (Crítica'. |
| `Alta` | String | Atributo técnico representando o campo mestre 'Alta'. |
| `Média` | String | Atributo técnico representando o campo mestre 'Média'. |
| `Baixa)` | String | Atributo técnico representando o campo mestre 'Baixa)'. |
| `Status (Aberto` | String (Enum) | Atributo técnico representando o campo mestre 'Status (Aberto'. |
| `Em Atendimento` | String | Atributo técnico representando o campo mestre 'Em Atendimento'. |
| `Pendente` | String | Atributo técnico representando o campo mestre 'Pendente'. |
| `Concluído)` | String | Atributo técnico representando o campo mestre 'Concluído)'. |
| `Item de Configuração (CI) Afetado` | String | Atributo técnico representando o campo mestre 'Item de Configuração (CI) Afetado'. |
| `Agente de TI Designado` | String | Atributo técnico representando o campo mestre 'Agente de TI Designado'. |
| `SLA Associado` | String | Atributo técnico representando o campo mestre 'SLA Associado'. |
| `Timestamp de Abertura/Encerramento` | DateTime | Atributo técnico representando o campo mestre 'Timestamp de Abertura/Encerramento'. |
| `Categoria de Impacto DORA.` | String | Atributo técnico representando o campo mestre 'Categoria de Impacto DORA.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_ticket": "REF-DO-181-001",
  "tipo_incidente_requi": "REF-DO-181-001",
  "solicitante_id_do_fu": "REF-DO-181-001",
  "descricao_do_problem": "Dados de Exemplo",
  "prioridade_critica": "REF-DO-181-001"
}
```

## # Citations

1. Processo de Gestão de Incidentes e Requisições (ITIL v4), Diretrizes DORA (Resiliência Operacional Digital), ISO/IEC 20000 / Operação de TI/TO.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
