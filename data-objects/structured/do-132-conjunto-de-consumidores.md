---
id: DO-132
name: "Conjunto de Consumidores"
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
  - "Clientes"
  - "Cadastro"
  - "LeanIX-v4"
---

# Conjunto de Consumidores (DO-132)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Conjunto de Consumidores** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Delimitação espacial do conjunto de unidades consumidoras atendidas por uma Subestação de Distribuição. Base para cálculo de indicadores coletivos DEC/FEC.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Clientes / Cadastro
*   **Sistemas e Aplicações que Manipulam (Applications):** GIS, ADMS, CIS
*   **Sistema de Registro Canônico (System of Truth):** GIS (Geographic Information System)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `Sigla: CONJ. COD_ID (PK)` | String (ID) | Atributo técnico representando o campo mestre 'Sigla: CONJ. COD_ID (PK)'. |
| `DIST (FK)` | String | Atributo técnico representando o campo mestre 'DIST (FK)'. |
| `NOME` | String | Atributo técnico representando o campo mestre 'NOME'. |
| `DESCR. Relações: N:1 com ARAT; 1:N com SUB` | String | Atributo técnico representando o campo mestre 'DESCR. Relações: N:1 com ARAT; 1:N com SUB'. |
| `UCs` | String | Atributo técnico representando o campo mestre 'UCs'. |
| `PONNOT.` | String | Atributo técnico representando o campo mestre 'PONNOT.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "sigla_conj_cod_id_pk": "REF-DO-132-001",
  "dist_fk": "Dados de Exemplo",
  "nome": "Dados de Exemplo",
  "descr_relacoes_n_1_c": "Dados de Exemplo",
  "ucs": "Dados de Exemplo"
}
```

## # Citations

1. ANEEL: PRODIST Módulo 8 / BDGD
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
