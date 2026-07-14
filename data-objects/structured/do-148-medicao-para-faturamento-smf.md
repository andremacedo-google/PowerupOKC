---
id: DO-148
name: "Medição para Faturamento (SMF)"
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
  - "Mercado"
  - "LeanIX-v4"
---

# Medição para Faturamento (SMF) (DO-148)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Medição para Faturamento (SMF)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Dados de medição de geração e consumo coletados em alta frequência pela CCEE para fins de contabilização.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Clientes / Mercado
*   **Sistemas e Aplicações que Manipulam (Applications):** SCDE (CCEE), MDM
*   **Sistema de Registro Canônico (System of Truth):** SCDE (CCEE)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `Código do Ponto de Medição (SCDE - nmro_mae)` | String | Atributo técnico representando o campo mestre 'Código do Ponto de Medição (SCDE - nmro_mae)'. |
| `Dados Brutos (RAWCij/RAWUGij)` | String | Atributo técnico representando o campo mestre 'Dados Brutos (RAWCij/RAWUGij)'. |
| `Timestamp (din_instante)` | DateTime | Atributo técnico representando o campo mestre 'Timestamp (din_instante)'. |
| `Energia Ativa/Reativa (MWh).` | Float | Atributo técnico representando o campo mestre 'Energia Ativa/Reativa (MWh).'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "codigo_do_ponto_de_m": "REF-DO-148-001",
  "dados_brutos_rawcij_": "Dados de Exemplo",
  "timestamp_din_instan": "2026-07-14T06:55:00Z",
  "energia_ativa_reativ": "Dados de Exemplo"
}
```

## # Citations

1. CCEE (Procedimentos de Comercialização)
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
