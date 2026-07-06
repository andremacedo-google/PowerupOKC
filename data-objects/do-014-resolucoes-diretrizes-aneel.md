---
id: DO-014
name: "Resoluções e Diretrizes da ANEEL"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Público"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Corporativo"
  - "LeanIX-v4"
---

# Resoluções e Diretrizes da ANEEL (ID: DO-014)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Resoluções e Diretrizes da ANEEL** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Compêndio de normas, despachos, resoluções normativas (ex: REN 1000, REN 482) publicadas pelas agências reguladoras do setor elétrico.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, da CCEE e as regras nacionais de segurança da informação e privacidade de dados (LGPD), garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Capacidades de Negócio que Consomem/Produzem (Business Capabilities N3):**
    *   [/cap-l3-conformidade-regulatoria](Capacidade Conformidade Regulatoria)
    *   [/cap-l3-gestao-de-risco-corporativo](Capacidade Gestao De Risco Corporativo)
*   **Sistemas e Aplicações que Manipulam (Applications):**
    *   [/applications/app-grc-governanca-riscos](Aplicação Grc Governanca Riscos)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `id_resolucao` | String | Identificador mestre da resolução ou diretriz normativa (ex: REN-1000). |
| `ano_publicacao` | Integer | Ano em que a norma foi homologada e publicada em Diário Oficial. |
| `orgao_emissor` | String | Entidade reguladora responsável (ANEEL, ONS, CCEE, MME). |
| `ementa_norma` | Text | Resumo descritivo simplificado e ementa do propósito legal da regra. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_resolucao": "ANEEL-REN-1000",
  "ano_publicacao": 2021,
  "orgao_emissor": "ANEEL",
  "ementa_norma": "Estabelece as Regras de Prestação do Serviço Público de Distribuição de Energia Elétrica..."
}
```

## # Citations

1. [Manual de Governança de Dados PowerupOKC] - Estabelece as regras de classificação de segurança e sensibilidade das informações corporativas e reguladas.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
