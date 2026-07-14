---
id: DO-133
name: "Contrato de Fornecimento"
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
  - "Cadastro"
  - "LeanIX-v4"
---

# Contrato de Fornecimento (DO-133)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Contrato de Fornecimento** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Formaliza a relação comercial entre o Cliente e a distribuidora para uma UC específica. No CIM, corresponde à classe CustomerAgreement.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Clientes / Cadastro
*   **Sistemas e Aplicações que Manipulam (Applications):** CIS (SAP IS-U)
*   **Sistema de Registro Canônico (System of Truth):** CIS (Customer Information System)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Contrato` | String (ID) | Atributo técnico representando o campo mestre 'ID do Contrato'. |
| `ID do Cliente` | String (ID) | Atributo técnico representando o campo mestre 'ID do Cliente'. |
| `ID da UC` | String (ID) | Atributo técnico representando o campo mestre 'ID da UC'. |
| `Data de Início/Fim` | DateTime | Atributo técnico representando o campo mestre 'Data de Início/Fim'. |
| `Status (Ativo` | String (Enum) | Atributo técnico representando o campo mestre 'Status (Ativo'. |
| `Inativo)` | String | Atributo técnico representando o campo mestre 'Inativo)'. |
| `Modalidade Tarifária` | String (ID) | Atributo técnico representando o campo mestre 'Modalidade Tarifária'. |
| `Demanda Contratada` | String | Atributo técnico representando o campo mestre 'Demanda Contratada'. |
| `Condições de Pagamento.` | String | Atributo técnico representando o campo mestre 'Condições de Pagamento.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_contrato": "REF-DO-133-001",
  "id_do_cliente": "REF-DO-133-001",
  "id_da_uc": "REF-DO-133-001",
  "data_de_inicio_fim": "2026-07-14T06:55:00Z",
  "status_ativo": "Active"
}
```

## # Citations

1. Processo 'Meter-to-Cash'
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
