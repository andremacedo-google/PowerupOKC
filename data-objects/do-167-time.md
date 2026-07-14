---
id: DO-167
name: "Time"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Restrito (LGPD)"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Nível 3"
  - "Corporativo"
  - "Recursos Humanos"
  - "LeanIX-v4"
---

# Time (DO-167)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Time** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Grupo funcional ou multidisciplinar de pessoas (squad, gerência ou centro de operação como COD/COG) focado em metas operacionais (como indicadores DEC/FEC) ou comerciais.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Recursos Humanos
*   **Sistemas e Aplicações que Manipulam (Applications):** HCM (SAP SuccessFactors), ServiceNow
*   **Sistema de Registro Canônico (System of Truth):** HCM (Human Capital Management)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Time` | String (ID) | Atributo técnico representando o campo mestre 'ID do Time'. |
| `Nome do Time` | DateTime | Atributo técnico representando o campo mestre 'Nome do Time'. |
| `Unidade Organizacional (Parent)` | String (ID) | Atributo técnico representando o campo mestre 'Unidade Organizacional (Parent)'. |
| `Líder do Time` | DateTime | Atributo técnico representando o campo mestre 'Líder do Time'. |
| `OKRs Associados` | String | Atributo técnico representando o campo mestre 'OKRs Associados'. |
| `Centro de Custo Vinculado.` | Float | Atributo técnico representando o campo mestre 'Centro de Custo Vinculado.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_time": "REF-DO-167-001",
  "nome_do_time": "2026-07-14T06:55:00Z",
  "unidade_organizacion": "REF-DO-167-001",
  "lider_do_time": "REF-DO-167-001",
  "okrs_associados": "Dados de Exemplo"
}
```

## # Citations

1. Gestão de Equipes / Desempenho e Metas (OKRs)
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
