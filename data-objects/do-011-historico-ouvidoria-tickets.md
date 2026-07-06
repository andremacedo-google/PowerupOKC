---
id: DO-011
name: "Histórico de Ouvidoria e Tickets"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Restrito"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Clientes"
  - "LeanIX-v4"
---

# Histórico de Ouvidoria e Tickets (ID: DO-011)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Histórico de Ouvidoria e Tickets** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Transcrições de chamadas de voz de clientes, e-mails de reclamação e tickets de falta de energia ou erro de faturamento.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, da CCEE e as regras nacionais de segurança da informação e privacidade de dados (LGPD), garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Capacidades de Negócio que Consomem/Produzem (Business Capabilities N3):**
    *   [/cap-l3-atendimento-ao-cliente-multicanal](Capacidade Atendimento Ao Cliente Multicanal)
    *   [/cap-l3-gestao-de-reclamacoes](Capacidade Gestao De Reclamacoes)
*   **Sistemas e Aplicações que Manipulam (Applications):**
    *   [/applications/app-crm-relacionamento-cliente](Aplicação Crm Relacionamento Cliente)
    *   [/applications/app-cis-faturamento-comercial](Aplicação Cis Faturamento Comercial)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `id_ticket_crm` | String | Código identificador do chamado ou caso no CRM. |
| `id_cliente` | String | ID do parceiro de negócio ou cliente associado no cadastro. |
| `categoria_reclamacao` | String | Natureza do chamado (FALTA_ENERGIA, ERRO_FATURAMENTO, NOVA_CONEXAO, OUTROS). |
| `score_sentimento` | String (Enum) | Percepção de urgência/sentimento (CRITICO, NEGATIVO, NEUTRO, AMIGAVEL). |
| `transcricao_interacao` | Text | Conteúdo textual bruto das mensagens ou conversas do atendimento síncrono. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_ticket_crm": "CASE-9988122",
  "id_cliente": "CLI-CAT-4431",
  "categoria_reclamacao": "ERRO_FATURAMENTO",
  "score_sentimento": "NEGATIVO",
  "transcricao_interacao": "O cliente contesta o valor cobrado de TUSD de R$185.30 no ciclo de Junho..."
}
```

## # Citations

1. [Manual de Governança de Dados PowerupOKC] - Estabelece as regras de classificação de segurança e sensibilidade das informações corporativas e reguladas.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
