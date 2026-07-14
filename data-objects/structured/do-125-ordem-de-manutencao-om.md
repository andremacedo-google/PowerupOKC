---
id: DO-125
name: "Ordem de Manutenção (OM)"
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
  - "Manutenção"
  - "LeanIX-v4"
---

# Ordem de Manutenção (OM) (DO-125)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Ordem de Manutenção (OM)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Solicitação para execução de uma atividade de manutenção (preventiva ou corretiva), que atua como um coletor de custos de O&M e CAPEX.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Ativos / Manutenção
*   **Sistemas e Aplicações que Manipulam (Applications):** EAM, SAP PM, WFM
*   **Sistema de Registro Canônico (System of Truth):** EAM / SAP PM

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID da OM` | String (ID) | Atributo técnico representando o campo mestre 'ID da OM'. |
| `ID do Ativo` | String (ID) | Atributo técnico representando o campo mestre 'ID do Ativo'. |
| `Tipo de Manutenção` | String (Enum) | Atributo técnico representando o campo mestre 'Tipo de Manutenção'. |
| `Descrição do Serviço` | String | Atributo técnico representando o campo mestre 'Descrição do Serviço'. |
| `Status` | String (Enum) | Atributo técnico representando o campo mestre 'Status'. |
| `Custos Reais (Mão de Obra` | Float | Atributo técnico representando o campo mestre 'Custos Reais (Mão de Obra'. |
| `Peças).` | String | Atributo técnico representando o campo mestre 'Peças).'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_da_om": "REF-DO-125-001",
  "id_do_ativo": "REF-DO-125-001",
  "tipo_de_manutencao": "Active",
  "descricao_do_servico": "Dados de Exemplo",
  "status": "Active"
}
```

## # Citations

1. Processo de Manutenção (O&M)
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
