---
id: DO-018
name: "Catálogo de APIs e Dependências"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Interno"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Corporativo"
  - "LeanIX-v4"
---

# Catálogo de APIs e Dependências (ID: DO-018)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Catálogo de APIs e Dependências** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Documentação Swagger/OpenAPI e diagramas mestre que registram a integração e comunicação entre sistemas de TI e OT.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, da CCEE e as regras nacionais de segurança da informação e privacidade de dados (LGPD), garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Capacidades de Negócio que Consomem/Produzem (Business Capabilities N3):**
    *   [/cap-l3-arquitetura-de-ti-e-de-dados](Capacidade Arquitetura De Ti E De Dados)
*   **Sistemas e Aplicações que Manipulam (Applications):**
    *   [/applications/app-grc-governanca-riscos](Aplicação Grc Governanca Riscos)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `id_endpoint` | String | ID do endpoint cadastrado no catálogo mestre de APIs. |
| `path_url` | String | Caminho relativo do serviço de integração (ex: /v1/telemetria/ami). |
| `metodo_http` | String (Enum) | Verbo HTTP utilizado na transação (GET, POST, PUT, DELETE). |
| `autenticacao_tipo` | String | Protocolo ativo de autenticação de segurança (ex: OAuth2.0, API-Key). |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_endpoint": "API-AMI-TELEMETRIA",
  "path_url": "/api/v1/telemetria/ami",
  "metodo_http": "POST",
  "autenticacao_tipo": "OAuth2.0"
}
```

## # Citations

1. [Manual de Governança de Dados PowerupOKC] - Estabelece as regras de classificação de segurança e sensibilidade das informações corporativas e reguladas.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
