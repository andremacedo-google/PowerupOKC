---
id: DO-179
name: "Mudança (Change)"
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

# Mudança (Change) (DO-179)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Mudança (Change)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Objeto utilizado para planejar, aprovar, executar e documentar qualquer modificação controlada no ambiente produtivo de TI ou TO (como atualização de patches de segurança em sistemas industriais ou servidores SCADA). Visa minimizar riscos de paradas inesperadas na operação de energia por meio de avaliações rigorosas de impacto e comitês de aprovação (CAB).

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Tecnologia da Informação
*   **Sistemas e Aplicações que Manipulam (Applications):** ServiceNow ITSM (Change Management), Jira Service Management
*   **Sistema de Registro Canônico (System of Truth):** ServiceNow ITSM (Change Management)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID da Mudança` | String (ID) | Atributo técnico representando o campo mestre 'ID da Mudança'. |
| `Tipo de Mudança (Padrão` | String (Enum) | Atributo técnico representando o campo mestre 'Tipo de Mudança (Padrão'. |
| `Normal` | String | Atributo técnico representando o campo mestre 'Normal'. |
| `Emergencial)` | String | Atributo técnico representando o campo mestre 'Emergencial)'. |
| `Risco Associado (Alto` | String | Atributo técnico representando o campo mestre 'Risco Associado (Alto'. |
| `Médio` | String | Atributo técnico representando o campo mestre 'Médio'. |
| `Baixo)` | String | Atributo técnico representando o campo mestre 'Baixo)'. |
| `Status (Planejada` | String (Enum) | Atributo técnico representando o campo mestre 'Status (Planejada'. |
| `Em Aprovação` | String | Atributo técnico representando o campo mestre 'Em Aprovação'. |
| `Autorizada` | String | Atributo técnico representando o campo mestre 'Autorizada'. |
| `Em Execução` | String | Atributo técnico representando o campo mestre 'Em Execução'. |
| `Concluída)` | String | Atributo técnico representando o campo mestre 'Concluída)'. |
| `Item de Configuração (CI) Alvo` | String | Atributo técnico representando o campo mestre 'Item de Configuração (CI) Alvo'. |
| `Plano de Implementação` | String | Atributo técnico representando o campo mestre 'Plano de Implementação'. |
| `Plano de Rollback (Backout Plan)` | String | Atributo técnico representando o campo mestre 'Plano de Rollback (Backout Plan)'. |
| `Janela de Manutenção Programada` | String | Atributo técnico representando o campo mestre 'Janela de Manutenção Programada'. |
| `Aprovação do CAB.` | String | Atributo técnico representando o campo mestre 'Aprovação do CAB.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_da_mudanca": "REF-DO-179-001",
  "tipo_de_mudanca_padr": "Active",
  "normal": "Dados de Exemplo",
  "emergencial": "Dados de Exemplo",
  "risco_associado_alto": "Dados de Exemplo"
}
```

## # Citations

1. Gestão de Mudanças (ITIL v4), Rotinas de Manutenção Programada de TI/TO, Conformidade Regulatória (ANEEL 964/2021 / DORA).
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
