---
id: DO-015
name: "Currículos e Perfis de Cargos"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Restrito (LGPD - PII)"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Corporativo"
  - "LeanIX-v4"
---

# Currículos e Perfis de Cargos (ID: DO-015)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Currículos e Perfis de Cargos** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Arquivos em formato Word/PDF contendo o histórico profissional de candidatos e descritivos das atribuições técnicas dos cargos.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, da CCEE e as regras nacionais de segurança da informação e privacidade de dados (LGPD), garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Capacidades de Negócio que Consomem/Produzem (Business Capabilities N3):**
    *   [/cap-l3-aquisicao-de-talentos](Capacidade Aquisicao De Talentos)
    *   [/cap-l3-desenvolvimento-e-treinamento](Capacidade Desenvolvimento E Treinamento)
*   **Sistemas e Aplicações que Manipulam (Applications):**
    *   [/applications/app-hris-sistema-rh](Aplicação Hris Sistema Rh)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `id_candidato` | String | Identificador exclusivo do candidato no banco de Talent Acquisition. |
| `nome_candidato` | String | Nome completo do profissional avaliado. |
| `habilidades_chave` | Array of Strings | Lista de hard skills identificados no currículo (ex: GCP, BigQuery, Python). |
| `id_vaga_referencia` | String | ID do perfil do cargo ou vaga cadastrada em Position Management. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_candidato": "CAND-2026-443",
  "nome_candidato": "Carlos Augusto da Silva",
  "habilidades_chave": ["GCP", "Python", "Data Science", "BigQuery"],
  "id_vaga_referencia": "POS-ENG-DATA-SR"
}
```

## # Citations

1. [Manual de Governança de Dados PowerupOKC] - Estabelece as regras de classificação de segurança e sensibilidade das informações corporativas e reguladas.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
