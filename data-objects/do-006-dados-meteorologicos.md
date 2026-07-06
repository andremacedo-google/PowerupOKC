---
id: DO-006
name: "Dados Meteorológicos"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Público"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Operações"
  - "LeanIX-v4"
---

# Dados Meteorológicos (ID: DO-006)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Dados Meteorológicos** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Informações e séries temporais de variáveis meteorológicas históricas e preditivas essenciais para modelagem de vazão, despacho térmico, previsão solar e eólica.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, da CCEE e as regras nacionais de segurança da informação e privacidade de dados (LGPD), garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Capacidades de Negócio que Consomem/Produzem (Business Capabilities N3):**
    *   [/cap-l3-operacao-de-usinas](Capacidade Operacao De Usinas)
    *   [/cap-l3-gestao-de-combustiveis](Capacidade Gestao De Combustiveis)
    *   [/cap-l3-analise-de-mercado-de-energia](Capacidade Analise De Mercado De Energia)
*   **Sistemas e Aplicações que Manipulam (Applications):**
    *   [/applications/app-adms-gestao-redes-distribuicao](Aplicação Adms Gestao Redes Distribuicao)
    *   [/applications/app-gis-georreferenciamento-redes](Aplicação Gis Georreferenciamento Redes)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `coordenadas_estacao` | JSON | Latitude e longitude da estação de medição ou quadrícula de satélite. |
| `irradiacao_solar_wm2` | Float | Irradiação Global Horizontal (GHI) estimada ou medida (W/m²). |
| `velocidade_vento_ms` | Float | Velocidade do vento à altura do cubo do aerogerador (m/s). |
| `precipitacao_acumulada_mm` | Float | Chuva acumulada na bacia hidrográfica em 24h (mm). |
| `temperatura_ar_c` | Float | Temperatura ambiente medida (ºC). |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "coordenadas_estacao": {
    "lat": -22.9068,
    "lon": -47.0608
  },
  "irradiacao_solar_wm2": 850.2,
  "velocidade_vento_ms": 6.8,
  "precipitacao_acumulada_mm": 0.0,
  "temperatura_ar_c": 26.5
}
```

## # Citations

1. [Manual de Governança de Dados PowerupOKC] - Estabelece as regras de classificação de segurança e sensibilidade das informações corporativas e reguladas.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
