---
id: DO-158
name: "Entidade Legal"
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

# Entidade Legal (DO-158)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Entidade Legal** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Razão social legalmente constituída (a holding e suas subsidiárias operacionais de Distribuição, Geração e Transmissão) que possui livros e balanços financeiros geridos em SAP.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Financeiro
*   **Sistemas e Aplicações que Manipulam (Applications):** ERP (SAP S/4HANA FI)
*   **Sistema de Registro Canônico (System of Truth):** ERP (SAP Financials)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `Código da Empresa (Company Code)` | String (ID) | Atributo técnico representando o campo mestre 'Código da Empresa (Company Code)'. |
| `CNPJ` | String (ID) | Atributo técnico representando o campo mestre 'CNPJ'. |
| `Razão Social` | String | Atributo técnico representando o campo mestre 'Razão Social'. |
| `Endereço Fiscal` | String | Atributo técnico representando o campo mestre 'Endereço Fiscal'. |
| `Regime Tributário` | String | Atributo técnico representando o campo mestre 'Regime Tributário'. |
| `Moeda do Razão.` | String | Atributo técnico representando o campo mestre 'Moeda do Razão.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "codigo_da_empresa_co": "REF-DO-158-001",
  "cnpj": "REF-DO-158-001",
  "razao_social": "Dados de Exemplo",
  "endereco_fiscal": "Dados de Exemplo",
  "regime_tributario": "Dados de Exemplo"
}
```

## # Citations

1. Estrutura Societária do Grupo, Consolidação de Demonstrações Financeiras
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
