---
id: DO-111
name: "Unidade Transformadora (Instalação)"
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

# Unidade Transformadora (Instalação) (DO-111)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Unidade Transformadora (Instalação)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Representação geológica das unidades físicas de transformação de tensão (média para baixa tensão) localizadas na rede de distribuição (ex: transformadores de poste de 75kVA).

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Ativos / Distribuição
*   **Sistemas e Aplicações que Manipulam (Applications):** GIS, EAM, ADMS
*   **Sistema de Registro Canônico (System of Truth):** GIS (Geographic Information System)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `Sigla: UNTRMT. COD_ID (PK)` | String (ID) | Atributo técnico representando o campo mestre 'Sigla: UNTRMT. COD_ID (PK)'. |
| `DIST` | String | Atributo técnico representando o campo mestre 'DIST'. |
| `POT_NOM` | Float | Atributo técnico representando o campo mestre 'POT_NOM'. |
| `PER_FER (Perda no ferro)` | String | Atributo técnico representando o campo mestre 'PER_FER (Perda no ferro)'. |
| `PER_TOT` | String | Atributo técnico representando o campo mestre 'PER_TOT'. |
| `CTMT (Feeder)` | String | Atributo técnico representando o campo mestre 'CTMT (Feeder)'. |
| `SUB` | String | Atributo técnico representando o campo mestre 'SUB'. |
| `CONJ` | String | Atributo técnico representando o campo mestre 'CONJ'. |
| `BANC` | String | Atributo técnico representando o campo mestre 'BANC'. |
| `TIP_TRAFO.` | String | Atributo técnico representando o campo mestre 'TIP_TRAFO.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "sigla_untrmt_cod_id_": "REF-DO-111-001",
  "dist": "Dados de Exemplo",
  "pot_nom": 150.45,
  "per_fer_perda_no_fer": "Dados de Exemplo",
  "per_tot": "Dados de Exemplo"
}
```

## # Citations

1. ANEEL (BDGD) / Perdas Técnicas
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
