---
id: DO-168
name: "Fornecedor"
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

# Fornecedor (DO-168)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Fornecedor** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Informações cadastrais e fiscais sobre empresas que fornecem materiais (ex: postes, cabos) ou serviços para a distribuidora.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Suprimentos
*   **Sistemas e Aplicações que Manipulam (Applications):** ERP (SAP MM), SRM
*   **Sistema de Registro Canônico (System of Truth):** ERP (SAP FI/MM)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Fornecedor` | String (ID) | Atributo técnico representando o campo mestre 'ID do Fornecedor'. |
| `CNPJ` | String (ID) | Atributo técnico representando o campo mestre 'CNPJ'. |
| `Razão Social` | String | Atributo técnico representando o campo mestre 'Razão Social'. |
| `Endereço` | String | Atributo técnico representando o campo mestre 'Endereço'. |
| `Dados de Contato` | String | Atributo técnico representando o campo mestre 'Dados de Contato'. |
| `Avaliação de Desempenho (SLA).` | Float | Atributo técnico representando o campo mestre 'Avaliação de Desempenho (SLA).'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_fornecedor": "REF-DO-168-001",
  "cnpj": "REF-DO-168-001",
  "razao_social": "Dados de Exemplo",
  "endereco": "Dados de Exemplo",
  "dados_de_contato": "Dados de Exemplo"
}
```

## # Citations

1. Processo de Compras
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
