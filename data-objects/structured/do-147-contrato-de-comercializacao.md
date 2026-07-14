---
id: DO-147
name: "Contrato de Comercialização"
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

# Contrato de Comercialização (DO-147)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Contrato de Comercialização** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Instrumento jurídico que formaliza a compra e venda de energia entre agentes, registrado e validado na CCEE.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Clientes / Mercado
*   **Sistemas e Aplicações que Manipulam (Applications):** Sistemas de Mercado, SCL (CCEE)
*   **Sistema de Registro Canônico (System of Truth):** CCEE (SCL - Sistema de Contabilização)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Contrato` | String (ID) | Atributo técnico representando o campo mestre 'ID do Contrato'. |
| `Partes (comprador/vendedor)` | String | Atributo técnico representando o campo mestre 'Partes (comprador/vendedor)'. |
| `Montante de Energia (MCBem)` | String | Atributo técnico representando o campo mestre 'Montante de Energia (MCBem)'. |
| `Período de Vigência` | String | Atributo técnico representando o campo mestre 'Período de Vigência'. |
| `Submercado` | String | Atributo técnico representando o campo mestre 'Submercado'. |
| `Tipo de Contrato (ACL/ACR).` | String (Enum) | Atributo técnico representando o campo mestre 'Tipo de Contrato (ACL/ACR).'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_contrato": "REF-DO-147-001",
  "partes_comprador_ven": "Dados de Exemplo",
  "montante_de_energia_": "Dados de Exemplo",
  "periodo_de_vigencia": "2026-07-14T06:55:00Z",
  "submercado": "Dados de Exemplo"
}
```

## # Citations

1. CCEE (Procedimentos de Comercialização)
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
