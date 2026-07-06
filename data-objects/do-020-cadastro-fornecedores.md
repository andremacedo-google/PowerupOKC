---
id: DO-020
name: "Cadastro de Fornecedores"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Interno"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Corporativo"
  - "LeanIX-v4"
---

# Cadastro de Fornecedores (ID: DO-020)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Cadastro de Fornecedores** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Documentos de homologação, histórico de certidões negativas, pontuações de ESG de fornecedores técnicos da companhia.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, da CCEE e as regras nacionais de segurança da informação e privacidade de dados (LGPD), garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Capacidades de Negócio que Consomem/Produzem (Business Capabilities N3):**
    *   [/cap-l3-gestao-de-fornecedores](Capacidade Gestao De Fornecedores)
    *   [/cap-l3-compras-estrategicas-procurement](Capacidade Compras Estrategicas Procurement)
*   **Sistemas e Aplicações que Manipulam (Applications):**
    *   [/applications/app-clm-gestao-contratos](Aplicação Clm Gestao Contratos)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `id_fornecedor` | String | Código de identificação mestre do parceiro fornecedor no ERP. |
| `cnpj_fornecedor` | String | CNPJ cadastrado e ativo do prestador de serviços ou fabricante. |
| `score_qualidade` | Integer | Pontuação histórica de qualidade de entregas e SLA de atendimento (faixa 0 a 100). |
| `status_homologacao` | String (Enum) | Estado cadastral regulado do parceiro (HOMOLOGADO, EXPIRADO, BLOQUEADO). |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_fornecedor": "SUP-MRO-7721",
  "cnpj_fornecedor": "98.765.432/0001-11",
  "score_qualidade": 92,
  "status_homologacao": "HOMOLOGADO"
}
```

## # Citations

1. [Manual de Governança de Dados PowerupOKC] - Estabelece as regras de classificação de segurança e sensibilidade das informações corporativas e reguladas.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
