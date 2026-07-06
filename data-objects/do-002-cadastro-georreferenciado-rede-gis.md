---
id: DO-002
name: "Cadastro Georreferenciado de Rede (GIS)"
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

# Cadastro Georreferenciado de Rede (GIS) (ID: DO-002)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Cadastro Georreferenciado de Rede (GIS)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Modelo topológico e geográfico que representa fisicamente o sistema elétrico e os ativos de média e baixa tensão da distribuidora (postes, transformadores, subestações, vãos de rede).

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, da CCEE e as regras nacionais de segurança da informação e privacidade de dados (LGPD), garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Capacidades de Negócio que Consomem/Produzem (Business Capabilities N3):**
    *   [/cap-l3-gestao-de-dados-da-rede](Capacidade Gestao De Dados Da Rede)
    *   [/cap-l3-manutencao-de-redes-e-equipamentos](Capacidade Manutencao De Redes E Equipamentos)
*   **Sistemas e Aplicações que Manipulam (Applications):**
    *   [/applications/app-gis-georreferenciamento-redes](Aplicação Gis Georreferenciamento Redes)
    *   [/applications/app-adms-gestao-redes-distribuicao](Aplicação Adms Gestao Redes Distribuicao)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `id_ativo_gis` | String | Código identificador geográfico exclusivo do ativo físico elétrico de rede. |
| `tipo_equipamento` | String (Enum) | Tipo de ativo (Transformador, Poste, Religador, Seccionadora, Cabo). |
| `coordenadas_geo` | JSON | Vetor de latitude e longitude contendo a localização espacial do ativo (WGS84). |
| `tensao_nominal_kv` | Float | Nível de classe de tensão nominal do barramento (ex: 13.8kV, 34.5kV, 0.22kV). |
| `id_alimentador_pai` | String | Identificador do circuito alimentador que supre energeticamente este ponto da rede. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_ativo_gis": "TRAFO-GIS-L3421",
  "tipo_equipamento": "TRANSFORMADOR_DISTRIBUICAO",
  "coordenadas_geo": {
    "latitude": -25.4284,
    "longitude": -49.2733
  },
  "tensao_nominal_kv": 13.8,
  "id_alimentador_pai": "ALIM-SE-LESTE-04"
}
```

## # Citations

1. [Manual de Governança de Dados PowerupOKC] - Estabelece as regras de classificação de segurança e sensibilidade das informações corporativas e reguladas.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
