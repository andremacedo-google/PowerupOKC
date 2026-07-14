---
id: DO-142
name: "Resposta de Demanda (RD)"
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

# Resposta de Demanda (RD) (DO-142)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Resposta de Demanda (RD)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Objeto de dados que gerencia as ofertas de redução voluntária de consumo por grandes consumidores industriais em momentos de pico do sistema, remunerados pelo ONS/CCEE para auxiliar na estabilidade do SIN.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Clientes / Comercialização
*   **Sistemas e Aplicações que Manipulam (Applications):** Sistemas CCEE, ETRM, ONS
*   **Sistema de Registro Canônico (System of Truth):** ONS / CCEE

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `CodAgente` | String (ID) | Atributo técnico representando o campo mestre 'CodAgente'. |
| `val_capacidade_reducao` | String (ID) | Atributo técnico representando o campo mestre 'val_capacidade_reducao'. |
| `val_mwh_reduzido` | String (ID) | Atributo técnico representando o campo mestre 'val_mwh_reduzido'. |
| `val_pago_rd (R$).` | Float | Atributo técnico representando o campo mestre 'val_pago_rd (R$).'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "codagente": "REF-DO-142-001",
  "val_capacidade_reduc": "REF-DO-142-001",
  "val_mwh_reduzido": "REF-DO-142-001",
  "val_pago_rd_r": 150.45
}
```

## # Citations

1. CCEE: Procedimentos de Comercialização (Módulo 9)
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
