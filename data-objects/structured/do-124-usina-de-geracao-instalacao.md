---
id: DO-124
name: "Usina de Geração (Instalação)"
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
  - "Geração e Transmissão"
  - "LeanIX-v4"
---

# Usina de Geração (Instalação) (DO-124)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Usina de Geração (Instalação)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Instalação geradora de energia elétrica composta por uma ou mais unidades geradoras de fontes hídricas, térmicas, eólicas ou solares, despachada ou supervisionada pelo ONS.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Ativos / Geração e Transmissão
*   **Sistemas e Aplicações que Manipulam (Applications):** GMS, EMS, SCADA
*   **Sistema de Registro Canônico (System of Truth):** GMS (Generation Management System)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ceg (Código Único)` | String | Atributo técnico representando o campo mestre 'ceg (Código Único)'. |
| `id_ons` | String (ID) | Atributo técnico representando o campo mestre 'id_ons'. |
| `nom_usina` | String | Atributo técnico representando o campo mestre 'nom_usina'. |
| `nom_tipousina (Fonte)` | String (Enum) | Atributo técnico representando o campo mestre 'nom_tipousina (Fonte)'. |
| `sts_aneel` | String (Enum) | Atributo técnico representando o campo mestre 'sts_aneel'. |
| `nom_subsistema` | String | Atributo técnico representando o campo mestre 'nom_subsistema'. |
| `val_potenciaefetiva` | Float | Atributo técnico representando o campo mestre 'val_potenciaefetiva'. |
| `id_modalidade_operacao.` | String (ID) | Atributo técnico representando o campo mestre 'id_modalidade_operacao.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "ceg_codigo_unico": "REF-DO-124-001",
  "id_ons": "REF-DO-124-001",
  "nom_usina": "Dados de Exemplo",
  "nom_tipousina_fonte": "Active",
  "sts_aneel": "Active"
}
```

## # Citations

1. ONS: Procedimentos de Rede / ANEEL: SIGA
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
