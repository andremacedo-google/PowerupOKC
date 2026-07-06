---
id: DO-008
name: "Cadastro de Prossumidor"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Restrito (LGPD - Dados Cadastrais)"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Clientes"
  - "LeanIX-v4"
---

# Cadastro de Prossumidor (ID: DO-008)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Cadastro de Prossumidor** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Dados cadastrais e técnicos dos consumidores ativos de Geração Distribuída (GD) que possuem micro ou minigeração e injetam energia ativa excedente na rede.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, da CCEE e as regras nacionais de segurança da informação e privacidade de dados (LGPD), garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Capacidades de Negócio que Consomem/Produzem (Business Capabilities N3):**
    *   [/cap-l3-onboarding-de-clientes](Capacidade Onboarding De Clientes)
    *   [/cap-l3-processamento-de-faturas](Capacidade Processamento De Faturas)
*   **Sistemas e Aplicações que Manipulam (Applications):**
    *   [/applications/app-crm-relacionamento-cliente](Aplicação Crm Relacionamento Cliente)
    *   [/applications/app-cis-faturamento-comercial](Aplicação Cis Faturamento Comercial)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `id_prossumidor` | String | Identificador único do prossumidor cadastrado na distribuidora. |
| `potencia_instalada_kwp` | Float | Capacidade de potência de pico instalada do gerador solar/eólico (kWp). |
| `tipo_geracao_gd` | String (Enum) | Subtipo tecnológico de geração (FOTOVOLTAICA, EOLICA, BIOMASSA, MINI_HYDRO). |
| `percentual_credito_rateio` | JSON | Matriz com os percentuais e contas de destino para rateio dos créditos acumulados. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_prossumidor": "PROS-GD-55412",
  "potencia_instalada_kwp": 7.5,
  "tipo_geracao_gd": "FOTOVOLTAICA",
  "percentual_credito_rateio": [
    {"conta_destino": "1002231", "percentual": 70.0},
    {"conta_destino": "1005542", "percentual": 30.0}
  ]
}
```

## # Citations

1. [Manual de Governança de Dados PowerupOKC] - Estabelece as regras de classificação de segurança e sensibilidade das informações corporativas e reguladas.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
