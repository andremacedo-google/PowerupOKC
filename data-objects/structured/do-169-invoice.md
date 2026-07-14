---
id: DO-169
name: "Invoice"
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
  - "Corporativo"
  - "Suprimentos"
  - "LeanIX-v4"
---

# Invoice (DO-169)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Invoice** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Fatura ou Nota Fiscal de Fornecedor enviada para cobrança de fornecimento de equipamentos ou serviços de obras de rede, sujeita à conciliação de 3 vias (3-way match) para liberação de pagamento.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Suprimentos
*   **Sistemas e Aplicações que Manipulam (Applications):** ERP (SAP FI/MM), BSM (Coupa / Ariba)
*   **Sistema de Registro Canônico (System of Truth):** ERP (SAP Financials)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID da Fatura (Nota Fiscal)` | String (ID) | Atributo técnico representando o campo mestre 'ID da Fatura (Nota Fiscal)'. |
| `ID do Fornecedor` | String (ID) | Atributo técnico representando o campo mestre 'ID do Fornecedor'. |
| `ID do Pedido de Compra` | String (ID) | Atributo técnico representando o campo mestre 'ID do Pedido de Compra'. |
| `Itens da Nota Fiscal` | String | Atributo técnico representando o campo mestre 'Itens da Nota Fiscal'. |
| `Valor Total` | Float | Atributo técnico representando o campo mestre 'Valor Total'. |
| `Impostos Retidos` | String (ID) | Atributo técnico representando o campo mestre 'Impostos Retidos'. |
| `Chave de Acesso NF-e.` | String | Atributo técnico representando o campo mestre 'Chave de Acesso NF-e.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_da_fatura_nota_fi": "REF-DO-169-001",
  "id_do_fornecedor": "REF-DO-169-001",
  "id_do_pedido_de_comp": "REF-DO-169-001",
  "itens_da_nota_fiscal": "Dados de Exemplo",
  "valor_total": 150.45
}
```

## # Citations

1. Processo Procure-to-Pay (P2P), Conciliação Físico-Financeira de Ativos (MCPSE)
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
