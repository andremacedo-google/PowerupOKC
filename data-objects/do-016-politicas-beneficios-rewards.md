---
id: DO-016
name: "Políticas de Benefícios e Total Rewards"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Interno"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Corporativo"
  - "LeanIX-v4"
---

# Políticas de Benefícios e Total Rewards (ID: DO-016)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Políticas de Benefícios e Total Rewards** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Manuais de procedimentos internos de RH detalhando regras de coparticipação de saúde, previdência privada corporativa e licenças.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, da CCEE e as regras nacionais de segurança da informação e privacidade de dados (LGPD), garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Capacidades de Negócio que Consomem/Produzem (Business Capabilities N3):**
    *   [/cap-l3-remuneracao-e-beneficios](Capacidade Remuneracao E Beneficios)
*   **Sistemas e Aplicações que Manipulam (Applications):**
    *   [/applications/app-hris-sistema-rh](Aplicação Hris Sistema Rh)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `id_politica` | String | Identificador mestre do manual de benefícios no portal corporativo. |
| `nome_beneficio` | String | Nome comercial do benefício associado (ex: Plano de Saúde Executivo, PGBL). |
| `faixa_coparticipacao_pct` | Float | Percentual regulado de coparticipação retido na folha do empregado. |
| `elegibilidade_cargo` | String | Critério de elegibilidade funcional de cargo para usufruir do item. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_politica": "POL-BEN-HLTH-02",
  "nome_beneficio": "Plano de Saúde Premium Bradesco",
  "faixa_coparticipacao_pct": 20.0,
  "elegibilidade_cargo": "Diretor, Gerente, Coordenador, Especialista"
}
```

## # Citations

1. [Manual de Governança de Dados PowerupOKC] - Estabelece as regras de classificação de segurança e sensibilidade das informações corporativas e reguladas.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
