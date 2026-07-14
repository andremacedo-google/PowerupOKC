---
id: DO-135
name: "Agente"
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

# Agente (DO-135)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Agente** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Entidade cadastral que representa a empresa que possui relação jurídica e contratual de compra e venda de energia no Ambiente de Contratação Livre (ACL) ou Regulado (ACR) perante a CCEE.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Clientes / Comercialização
*   **Sistemas e Aplicações que Manipulam (Applications):** Sistemas CCEE (SCL/CliqCCEE), ETRM, ERP
*   **Sistema de Registro Canônico (System of Truth):** CCEE (Sistemas Proprietários)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `CodAgente` | String (ID) | Atributo técnico representando o campo mestre 'CodAgente'. |
| `CNPJ` | String (ID) | Atributo técnico representando o campo mestre 'CNPJ'. |
| `classe_agente (Gerador/Distribuidor/Comercializador/Consumidor)` | String (ID) | Atributo técnico representando o campo mestre 'classe_agente (Gerador/Distribuidor/Comercializador/Consumidor)'. |
| `sts_cadastro` | String (Enum) | Atributo técnico representando o campo mestre 'sts_cadastro'. |
| `capital_social` | String | Atributo técnico representando o campo mestre 'capital_social'. |
| `termo_adesao.` | String | Atributo técnico representando o campo mestre 'termo_adesao.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "codagente": "REF-DO-135-001",
  "cnpj": "REF-DO-135-001",
  "classe_agente_gerado": "Dados de Exemplo",
  "sts_cadastro": "Active",
  "capital_social": "Dados de Exemplo"
}
```

## # Citations

1. CCEE: Procedimentos de Comercialização (Módulo 1)
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
