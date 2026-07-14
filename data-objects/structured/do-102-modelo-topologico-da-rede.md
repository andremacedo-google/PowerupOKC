---
id: DO-102
name: "Modelo Topológico da Rede"
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
  - "Cadastro de Ativos"
  - "LeanIX-v4"
---

# Modelo Topológico da Rede (DO-102)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Modelo Topológico da Rede** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Representação da conectividade lógica entre os ativos da rede, crucial para estudos elétricos. É exportado do GIS (as-built) para o ADMS (as-operated) via CIM XML.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Ativos / Cadastro de Ativos
*   **Sistemas e Aplicações que Manipulam (Applications):** ADMS, GIS
*   **Sistema de Registro Canônico (System of Truth):** GIS (Geographic Information System)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `Relações de conectividade (nó-a-nó)` | String (ID) | Atributo técnico representando o campo mestre 'Relações de conectividade (nó-a-nó)'. |
| `status dinâmico dos dispositivos de manobra (aberto/fechado)` | String (Enum) | Atributo técnico representando o campo mestre 'status dinâmico dos dispositivos de manobra (aberto/fechado)'. |
| `impedâncias de segmento.` | String | Atributo técnico representando o campo mestre 'impedâncias de segmento.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "relacoes_de_conectiv": "Dados de Exemplo",
  "status_dinamico_dos_": "Active",
  "impedancias_de_segme": "Dados de Exemplo"
}
```

## # Citations

1. ANEEL (BDGD), Funções de Automação (FLISR, VVO)
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
