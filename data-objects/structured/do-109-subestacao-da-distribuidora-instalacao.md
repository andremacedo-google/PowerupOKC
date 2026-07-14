---
id: DO-109
name: "Subestação da Distribuidora (Instalação)"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Confidencial (Infraestrutura Crítica)"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Nível 3"
  - "Ativos"
  - "Distribuição"
  - "LeanIX-v4"
---

# Subestação da Distribuidora (Instalação) (DO-109)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Subestação da Distribuidora (Instalação)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Polígono geográfico ou ponto que delimita a área geográfica física ocupada por uma subestação de interesse regulatório e tarifário da distribuidora (rebaixadora, elevadora).

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Ativos / Distribuição
*   **Sistemas e Aplicações que Manipulam (Applications):** GIS, EAM, ADMS, SCADA
*   **Sistema de Registro Canônico (System of Truth):** GIS (Geographic Information System)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `Sigla: SUB. COD_ID (PK)` | String (ID) | Atributo técnico representando o campo mestre 'Sigla: SUB. COD_ID (PK)'. |
| `DIST (FK)` | String | Atributo técnico representando o campo mestre 'DIST (FK)'. |
| `POS (DDA)` | String | Atributo técnico representando o campo mestre 'POS (DDA)'. |
| `NOME` | String | Atributo técnico representando o campo mestre 'NOME'. |
| `DESCR. Relações: N:1 com CONJ; 1:N com BAR (Barramentos)` | String | Atributo técnico representando o campo mestre 'DESCR. Relações: N:1 com CONJ; 1:N com BAR (Barramentos)'. |
| `BAY (Vãos).` | String | Atributo técnico representando o campo mestre 'BAY (Vãos).'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "sigla_sub_cod_id_pk": "REF-DO-109-001",
  "dist_fk": "Dados de Exemplo",
  "pos_dda": "Dados de Exemplo",
  "nome": "Dados de Exemplo",
  "descr_relacoes_n_1_c": "Dados de Exemplo"
}
```

## # Citations

1. ANEEL (BDGD) / PRODIST Módulo 3
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
