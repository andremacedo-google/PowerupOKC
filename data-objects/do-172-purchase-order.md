---
id: DO-172
name: "Purchase Order"
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

# Purchase Order (DO-172)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Purchase Order** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Pedido de Compra (PO) formal enviado ao fornecedor para aquisição de materiais de rede (cabos, postes, transformadores) ou contratação de serviços, vinculando os custos ao projeto.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Suprimentos
*   **Sistemas e Aplicações que Manipulam (Applications):** ERP (SAP MM), BSM (Coupa / Ariba)
*   **Sistema de Registro Canônico (System of Truth):** BSM / ERP

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Pedido (PO Number)` | String (ID) | Atributo técnico representando o campo mestre 'ID do Pedido (PO Number)'. |
| `ID do Fornecedor` | String (ID) | Atributo técnico representando o campo mestre 'ID do Fornecedor'. |
| `Código do Material/Serviço` | String | Atributo técnico representando o campo mestre 'Código do Material/Serviço'. |
| `Quantidade` | String (ID) | Atributo técnico representando o campo mestre 'Quantidade'. |
| `Valor Unitário/Total` | Float | Atributo técnico representando o campo mestre 'Valor Unitário/Total'. |
| `Classificação Contábil (PEP/Centro de Custo)` | Float | Atributo técnico representando o campo mestre 'Classificação Contábil (PEP/Centro de Custo)'. |
| `Data de Entrega.` | DateTime | Atributo técnico representando o campo mestre 'Data de Entrega.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_pedido_po_numb": "REF-DO-172-001",
  "id_do_fornecedor": "REF-DO-172-001",
  "codigo_do_material_s": "REF-DO-172-001",
  "quantidade": "REF-DO-172-001",
  "valor_unitario_total": 150.45
}
```

## # Citations

1. Processo Procure-to-Pay (P2P), Rastreabilidade de Custos de CAPEX para Unitização
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
