---
id: DO-007
name: "Cadastro de Cliente Livre"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Restrito (LGPD - Dados Cadastrais)"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Clientes"
  - "LeanIX-v4"
---

# Cadastro de Cliente Livre (ID: DO-007)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Cadastro de Cliente Livre** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Dados mestres de identificação, faturamento, contratos corporativos, pontos de conexão e limites de demanda acordados de consumidores livres (ACL).

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, da CCEE e as regras nacionais de segurança da informação e privacidade de dados (LGPD), garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Capacidades de Negócio que Consomem/Produzem (Business Capabilities N3):**
    *   [/cap-l3-onboarding-de-clientes](Capacidade Onboarding De Clientes)
    *   [/cap-l3-gestao-de-leads-e-oportunidades](Capacidade Gestao De Leads E Oportunidades)
*   **Sistemas e Aplicações que Manipulam (Applications):**
    *   [/applications/app-crm-relacionamento-cliente](Aplicação Crm Relacionamento Cliente)
    *   [/applications/app-cis-faturamento-comercial](Aplicação Cis Faturamento Comercial)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `id_cliente_libre` | String | Código interno exclusivo de identificação do cliente no CRM/CIS. |
| `razao_social` | String | Nome da razão social ou entidade legal do cliente livre B2B. |
| `cnpj_cliente` | String | Cadastro Nacional da Pessoa Jurídica (CNPJ) formatado. |
| `demanda_contratada_kw` | Integer | Limite de demanda ativa de potência contratada em contrato (kW). |
| `id_ponto_entrega` | String | Identificador exclusivo do barramento ou local físico de entrega do ACL. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_cliente_libre": "CLI-ACL-88712",
  "razao_social": "Metalúrgica Leste Brasileira S.A.",
  "cnpj_cliente": "12.345.678/0001-99",
  "demanda_contratada_kw": 5000,
  "id_ponto_entrega": "PE-SE-LESTE-772"
}
```

## # Citations

1. [Manual de Governança de Dados PowerupOKC] - Estabelece as regras de classificação de segurança e sensibilidade das informações corporativas e reguladas.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
