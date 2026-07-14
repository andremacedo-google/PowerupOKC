---
id: DO-104
name: "Equipamento Distribuidora (Ativo)"
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
  - "Ativos"
  - "Distribuição"
  - "LeanIX-v4"
---

# Equipamento Distribuidora (Ativo) (DO-104)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Equipamento Distribuidora (Ativo)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Ativo físico não geográfico acoplado à unidade técnica (como o transformador físico acoplado à UNTRMT ou o medidor físico), contendo as especificações técnicas de placa e dados do cadastro regulatório de ativos.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Ativos / Distribuição
*   **Sistemas e Aplicações que Manipulam (Applications):** EAM (SAP PM), ERP (SAP FI-AA)
*   **Sistema de Registro Canônico (System of Truth):** EAM / ERP (SAP S/4HANA)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `Sigla: EQTRMT / EQME. COD_ID` | String (ID) | Atributo técnico representando o campo mestre 'Sigla: EQTRMT / EQME. COD_ID'. |
| `UN_TR_MT (FK)` | String | Atributo técnico representando o campo mestre 'UN_TR_MT (FK)'. |
| `CLAS_TEN` | String | Atributo técnico representando o campo mestre 'CLAS_TEN'. |
| `POT_NOM` | Float | Atributo técnico representando o campo mestre 'POT_NOM'. |
| `LIG` | String | Atributo técnico representando o campo mestre 'LIG'. |
| `TUC` | String | Atributo técnico representando o campo mestre 'TUC'. |
| `A1 a A6` | String | Atributo técnico representando o campo mestre 'A1 a A6'. |
| `UAR (Unidade de Adição e Retirada)` | String (ID) | Atributo técnico representando o campo mestre 'UAR (Unidade de Adição e Retirada)'. |
| `SITCONT (Situação Contábil)` | String | Atributo técnico representando o campo mestre 'SITCONT (Situação Contábil)'. |
| `DAT_IMO.` | DateTime | Atributo técnico representando o campo mestre 'DAT_IMO.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "sigla_eqtrmt_eqme_co": "Dados de Exemplo",
  "un_tr_mt_fk": "Dados de Exemplo",
  "clas_ten": "Dados de Exemplo",
  "pot_nom": 150.45,
  "lig": "Dados de Exemplo"
}
```

## # Citations

1. ANEEL: MCPSE
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
