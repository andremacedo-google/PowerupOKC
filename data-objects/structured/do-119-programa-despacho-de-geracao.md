---
id: DO-119
name: "Programa/Despacho de Geração"
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

# Programa/Despacho de Geração (DO-119)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Programa/Despacho de Geração** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Programação da quantidade de energia que uma usina deve produzir em intervalos específicos, conforme despacho do ONS.

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
| `ID do Despacho` | String (ID) | Atributo técnico representando o campo mestre 'ID do Despacho'. |
| `ID da Usina/UG` | String (ID) | Atributo técnico representando o campo mestre 'ID da Usina/UG'. |
| `Período` | String | Atributo técnico representando o campo mestre 'Período'. |
| `Potência Programada (MW)` | Float | Atributo técnico representando o campo mestre 'Potência Programada (MW)'. |
| `Limites de Rampa.` | Float | Atributo técnico representando o campo mestre 'Limites de Rampa.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_despacho": "REF-DO-119-001",
  "id_da_usina_ug": "REF-DO-119-001",
  "periodo": "2026-07-14T06:55:00Z",
  "potencia_programada_": 150.45,
  "limites_de_rampa": 150.45
}
```

## # Citations

1. ONS: Procedimentos de Rede (PMO, PDO)
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
