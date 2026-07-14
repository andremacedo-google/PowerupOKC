---
id: DO-113
name: "Curva de Capacidade/Eficiência"
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
  - "Ativos"
  - "Geração e Transmissão"
  - "LeanIX-v4"
---

# Curva de Capacidade/Eficiência (DO-113)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Curva de Capacidade/Eficiência** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Modelo matemático que descreve os limites de operação e eficiência de uma unidade geradora em função de variáveis (ex: nível do reservatório, vento).

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Ativos / Geração e Transmissão
*   **Sistemas e Aplicações que Manipulam (Applications):** GMS, Sistemas de Otimização
*   **Sistema de Registro Canônico (System of Truth):** GMS (Generation Management System)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID da Unidade Geradora` | String (ID) | Atributo técnico representando o campo mestre 'ID da Unidade Geradora'. |
| `Variável de Entrada (vazão` | String | Atributo técnico representando o campo mestre 'Variável de Entrada (vazão'. |
| `vento)` | String | Atributo técnico representando o campo mestre 'vento)'. |
| `Potência Máxima/Mínima de Saída (MW).` | Float | Atributo técnico representando o campo mestre 'Potência Máxima/Mínima de Saída (MW).'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_da_unidade_gerado": "REF-DO-113-001",
  "variavel_de_entrada_": "Dados de Exemplo",
  "vento": "Dados de Exemplo",
  "potencia_maxima_mini": 150.45
}
```

## # Citations

1. Processo de Despacho Econômico
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
