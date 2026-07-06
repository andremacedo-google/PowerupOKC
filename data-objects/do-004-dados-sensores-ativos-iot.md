---
id: DO-004
name: "Dados de Sensores de Ativos (IoT)"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Interno"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Operações"
  - "LeanIX-v4"
---

# Dados de Sensores de Ativos (IoT) (ID: DO-004)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Dados de Sensores de Ativos (IoT)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Medições analógicas contínuas de alta frequência de sensores de Internet das Coisas (IoT) instalados em grandes ativos industriais, monitorando variáveis de saúde e física térmica.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, da CCEE e as regras nacionais de segurança da informação e privacidade de dados (LGPD), garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Capacidades de Negócio que Consomem/Produzem (Business Capabilities N3):**
    *   [/cap-l3-manutencao-preditiva](Capacidade Manutencao Preditiva)
    *   [/cap-l3-manutencao-de-ativos-de-geracao](Capacidade Manutencao De Ativos De Geracao)
*   **Sistemas e Aplicações que Manipulam (Applications):**
    *   [/applications/app-adms-gestao-redes-distribuicao](Aplicação Adms Gestao Redes Distribuicao)
    *   [/applications/app-gis-georreferenciamento-redes](Aplicação Gis Georreferenciamento Redes)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `id_sensor` | String | Código exclusivo de identificação do nó do sensor de IoT. |
| `id_equipamento_pai` | String | ID do ativo físico de referência no sistema de gestão (SAP PM Equipment ID). |
| `temperatura_oleo_c` | Float | Temperatura medida no enrolamento e óleo isolante do transformador em ºC. |
| `nivel_vibração_mms` | Float | Nível de vibração mecânica medido no eixo da turbina de geração (mm/s). |
| `gases_dissolvidos_ppm` | Integer | Nível de gases de hidrogênio (H2) dissolvidos no óleo (ppm) - Cromatografia online. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_sensor": "SNSR-IOT-TRAFO-12A",
  "id_equipamento_pai": "EQUIP-TRAFO-500KV-01",
  "temperatura_oleo_c": 78.4,
  "nivel_vibração_mms": 1.25,
  "gases_dissolvidos_ppm": 120
}
```

## # Citations

1. [Manual de Governança de Dados PowerupOKC] - Estabelece as regras de classificação de segurança e sensibilidade das informações corporativas e reguladas.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
