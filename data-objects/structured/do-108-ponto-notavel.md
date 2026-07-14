---
id: DO-108
name: "Ponto Notável"
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

# Ponto Notável (DO-108)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Ponto Notável** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Ponto georreferenciado que localiza as estruturas de suporte físico da rede aérea, tais como postes e torres, contendo dados patrimoniais vinculados ao MCPSE da ANEEL.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Ativos / Distribuição
*   **Sistemas e Aplicações que Manipulam (Applications):** GIS, EAM (SAP PM)
*   **Sistema de Registro Canônico (System of Truth):** GIS (Geographic Information System)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `Sigla: PONNOT. COD_ID (PK)` | String (ID) | Atributo técnico representando o campo mestre 'Sigla: PONNOT. COD_ID (PK)'. |
| `DIST` | String | Atributo técnico representando o campo mestre 'DIST'. |
| `TIP_PN` | String | Atributo técnico representando o campo mestre 'TIP_PN'. |
| `ESTR` | String | Atributo técnico representando o campo mestre 'ESTR'. |
| `MAT (Concreto/Madeira)` | String | Atributo técnico representando o campo mestre 'MAT (Concreto/Madeira)'. |
| `ALT` | String | Atributo técnico representando o campo mestre 'ALT'. |
| `ODI (Ordem de Imobilização)` | String | Atributo técnico representando o campo mestre 'ODI (Ordem de Imobilização)'. |
| `TI (Tipo Instalação)` | String (Enum) | Atributo técnico representando o campo mestre 'TI (Tipo Instalação)'. |
| `CM (Centro Modular).` | String | Atributo técnico representando o campo mestre 'CM (Centro Modular).'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "sigla_ponnot_cod_id_": "REF-DO-108-001",
  "dist": "Dados de Exemplo",
  "tip_pn": "Dados de Exemplo",
  "estr": "Dados de Exemplo",
  "mat_concreto_madeira": "Dados de Exemplo"
}
```

## # Citations

1. ANEEL (BDGD) / ANEEL: MCPSE
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
