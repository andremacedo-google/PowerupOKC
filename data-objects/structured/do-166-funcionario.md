---
id: DO-166
name: "Funcionário"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Restrito (LGPD)"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Nível 3"
  - "Corporativo"
  - "Recursos Humanos"
  - "LeanIX-v4"
---

# Funcionário (DO-166)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Funcionário** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Informações sobre os funcionários da empresa (CLT/diretoria) que estão na folha de pagamento ativa, com relação direta de emprego.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Recursos Humanos
*   **Sistemas e Aplicações que Manipulam (Applications):** HCM (SAP SuccessFactors)
*   **Sistema de Registro Canônico (System of Truth):** HCM (Human Capital Management)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Funcionário` | String (ID) | Atributo técnico representando o campo mestre 'ID do Funcionário'. |
| `Nome` | String | Atributo técnico representando o campo mestre 'Nome'. |
| `CPF` | String (ID) | Atributo técnico representando o campo mestre 'CPF'. |
| `Cargo` | String | Atributo técnico representando o campo mestre 'Cargo'. |
| `Lotação` | String | Atributo técnico representando o campo mestre 'Lotação'. |
| `Salário` | String | Atributo técnico representando o campo mestre 'Salário'. |
| `Centro de Custo` | Float | Atributo técnico representando o campo mestre 'Centro de Custo'. |
| `Dados Bancários` | String | Atributo técnico representando o campo mestre 'Dados Bancários'. |
| `Histórico de Treinamentos (NRs).` | String | Atributo técnico representando o campo mestre 'Histórico de Treinamentos (NRs).'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_funcionario": "REF-DO-166-001",
  "nome": "Dados de Exemplo",
  "cpf": "REF-DO-166-001",
  "cargo": "Dados de Exemplo",
  "lotacao": "Dados de Exemplo"
}
```

## # Citations

1. Processos de Recursos Humanos
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
