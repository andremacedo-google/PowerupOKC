---
id: DO-151
name: "Ativo Fixo (Contábil)"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Confidencial (Financeiro)"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Nível 3"
  - "Corporativo"
  - "Financeiro"
  - "LeanIX-v4"
---

# Ativo Fixo (Contábil) (DO-151)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Ativo Fixo (Contábil)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Registro contábil de um bem físico em serviço, criado a partir da capitalização (liquidação) dos custos do Projeto de Investimento (SAP PS). Segue normas societárias (IFRS).

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Financeiro
*   **Sistemas e Aplicações que Manipulam (Applications):** ERP (SAP FI-AA)
*   **Sistema de Registro Canônico (System of Truth):** ERP (SAP FI-AA)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Ativo Contábil` | String (ID) | Atributo técnico representando o campo mestre 'ID do Ativo Contábil'. |
| `Descrição` | String | Atributo técnico representando o campo mestre 'Descrição'. |
| `Data de Aquisição` | DateTime | Atributo técnico representando o campo mestre 'Data de Aquisição'. |
| `Valor de Aquisição (Custo Histórico)` | Float | Atributo técnico representando o campo mestre 'Valor de Aquisição (Custo Histórico)'. |
| `Vida Útil Econômica` | String (ID) | Atributo técnico representando o campo mestre 'Vida Útil Econômica'. |
| `Chave de Depreciação Contábil.` | String | Atributo técnico representando o campo mestre 'Chave de Depreciação Contábil.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_ativo_contabil": "REF-DO-151-001",
  "descricao": "Dados de Exemplo",
  "data_de_aquisicao": "2026-07-14T06:55:00Z",
  "valor_de_aquisicao_c": 150.45,
  "vida_util_economica": "REF-DO-151-001"
}
```

## # Citations

1. Contabilidade Societária / IFRS
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
