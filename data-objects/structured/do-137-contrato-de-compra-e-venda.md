---
id: DO-137
name: "Contrato de Compra e Venda"
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
  - "Comercialização"
  - "LeanIX-v4"
---

# Contrato de Compra e Venda (DO-137)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Contrato de Compra e Venda** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Contrato bilateral de fornecimento ou compra de energia de longo ou médio prazo, registrado e validado por ambas as contrapartes perante a CCEE.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Clientes / Comercialização
*   **Sistemas e Aplicações que Manipulam (Applications):** Sistemas CCEE (CliqCCEE), ETRM (Thunders), SAP S/4HANA (CLM)
*   **Sistema de Registro Canônico (System of Truth):** ETRM / CCEE (SCL)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `CodContrato` | String (ID) | Atributo técnico representando o campo mestre 'CodContrato'. |
| `comprador (FK)` | String | Atributo técnico representando o campo mestre 'comprador (FK)'. |
| `vendedor (FK)` | String | Atributo técnico representando o campo mestre 'vendedor (FK)'. |
| `val_mwh` | Float | Atributo técnico representando o campo mestre 'val_mwh'. |
| `vig_inicio` | DateTime | Atributo técnico representando o campo mestre 'vig_inicio'. |
| `vig_fim` | DateTime | Atributo técnico representando o campo mestre 'vig_fim'. |
| `tipo_contrato (CCEAR` | String (Enum) | Atributo técnico representando o campo mestre 'tipo_contrato (CCEAR'. |
| `CCEAL` | String | Atributo técnico representando o campo mestre 'CCEAL'. |
| `CER)` | String | Atributo técnico representando o campo mestre 'CER)'. |
| `sazonalizacao` | String | Atributo técnico representando o campo mestre 'sazonalizacao'. |
| `modulacao.` | String | Atributo técnico representando o campo mestre 'modulacao.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "codcontrato": "REF-DO-137-001",
  "comprador_fk": "Dados de Exemplo",
  "vendedor_fk": "Dados de Exemplo",
  "val_mwh": 150.45,
  "vig_inicio": "2026-07-14T06:55:00Z"
}
```

## # Citations

1. CCEE: Procedimentos de Comercialização (Módulo 3)
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
