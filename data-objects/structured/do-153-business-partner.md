---
id: DO-153
name: "Business Partner"
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

# Business Partner (DO-153)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Business Partner** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Entidade de negócio externa (cliente, fornecedor ou parceiro) com a qual a empresa transaciona. No SAP S/4HANA, unifica os cadastros de clientes e fornecedores para maior integridade financeira.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Financeiro
*   **Sistemas e Aplicações que Manipulam (Applications):** ERP (SAP S/4HANA BP/FI), CRM, BSM (Coupa)
*   **Sistema de Registro Canônico (System of Truth):** ERP / CRM

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Parceiro de Negócio (BP ID)` | String (ID) | Atributo técnico representando o campo mestre 'ID do Parceiro de Negócio (BP ID)'. |
| `CNPJ/CPF` | String (ID) | Atributo técnico representando o campo mestre 'CNPJ/CPF'. |
| `Razão Social/Nome` | String | Atributo técnico representando o campo mestre 'Razão Social/Nome'. |
| `Endereço Fiscal` | String | Atributo técnico representando o campo mestre 'Endereço Fiscal'. |
| `Grupo de Contas` | String | Atributo técnico representando o campo mestre 'Grupo de Contas'. |
| `Condições de Pagamento` | String | Atributo técnico representando o campo mestre 'Condições de Pagamento'. |
| `Categoria de Parceiro.` | String | Atributo técnico representando o campo mestre 'Categoria de Parceiro.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_parceiro_de_ne": "REF-DO-153-001",
  "cnpj_cpf": "REF-DO-153-001",
  "razao_social_nome": "Dados de Exemplo",
  "endereco_fiscal": "Dados de Exemplo",
  "grupo_de_contas": "Dados de Exemplo"
}
```

## # Citations

1. Processo Procure-to-Pay (P2P) e Order-to-Cash (O2C)
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
