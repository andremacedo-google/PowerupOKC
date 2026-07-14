---
id: DO-140
name: "Posição Mensal"
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

# Posição Mensal (DO-140)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Posição Mensal** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Consolidação mensal lógico-aritmética do balanço energético de cada agente (diferença entre energia contratada e energia medida/gerada), indicando as exposições financeiras a serem liquidadas no MCP.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Clientes / Comercialização
*   **Sistemas e Aplicações que Manipulam (Applications):** Sistemas CCEE (DRI), ETRM
*   **Sistema de Registro Canônico (System of Truth):** CCEE (DRI - Divulgação de Resultados)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `CodAgente` | String (ID) | Atributo técnico representando o campo mestre 'CodAgente'. |
| `val_exposicao_mwh` | Float | Atributo técnico representando o campo mestre 'val_exposicao_mwh'. |
| `val_encargo_ess` | Float | Atributo técnico representando o campo mestre 'val_encargo_ess'. |
| `val_penalidade_energia` | String (ID) | Atributo técnico representando o campo mestre 'val_penalidade_energia'. |
| `val_recontabilizacao` | Float | Atributo técnico representando o campo mestre 'val_recontabilizacao'. |
| `val_saldo_mcp (R$).` | Float | Atributo técnico representando o campo mestre 'val_saldo_mcp (R$).'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "codagente": "REF-DO-140-001",
  "val_exposicao_mwh": 150.45,
  "val_encargo_ess": 150.45,
  "val_penalidade_energ": "REF-DO-140-001",
  "val_recontabilizacao": 150.45
}
```

## # Citations

1. CCEE: Processo de Contabilização
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
