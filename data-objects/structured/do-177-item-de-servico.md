---
id: DO-177
name: "Item de Serviço"
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
  - "Corporativo"
  - "Tecnologia da Informação"
  - "LeanIX-v4"
---

# Item de Serviço (DO-177)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Item de Serviço** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Representação conceitual e comercial de um serviço ou produto de tecnologia pré-aprovado (como solicitação de novos laptops, licenças de software SAP/GIS ou concessão de acesso a sistemas críticos de TO) disponibilizado no portal de autoatendimento para solicitação por colaboradores. Quando solicitado, gera de forma automatizada uma Requisição de Serviço (Ticket).

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Tecnologia da Informação
*   **Sistemas e Aplicações que Manipulam (Applications):** ServiceNow Service Catalog, Jira Service Management Catalog
*   **Sistema de Registro Canônico (System of Truth):** ServiceNow Service Catalog (Catálogo de Serviços de TI)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Item de Serviço` | String (ID) | Atributo técnico representando o campo mestre 'ID do Item de Serviço'. |
| `Nome do Serviço` | String | Atributo técnico representando o campo mestre 'Nome do Serviço'. |
| `Descrição do Serviço` | String | Atributo técnico representando o campo mestre 'Descrição do Serviço'. |
| `Categoria do Catálogo` | String | Atributo técnico representando o campo mestre 'Categoria do Catálogo'. |
| `Preço / Custo Estimado (se houver)` | Float | Atributo técnico representando o campo mestre 'Preço / Custo Estimado (se houver)'. |
| `Tempo de Entrega Estimado (SLA)` | String | Atributo técnico representando o campo mestre 'Tempo de Entrega Estimado (SLA)'. |
| `Fluxo de Aprovação Requerido (Workflow)` | String (ID) | Atributo técnico representando o campo mestre 'Fluxo de Aprovação Requerido (Workflow)'. |
| `CIs de Serviço Relacionados` | String | Atributo técnico representando o campo mestre 'CIs de Serviço Relacionados'. |
| `Status de Disponibilidade.` | String (ID) | Atributo técnico representando o campo mestre 'Status de Disponibilidade.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_item_de_servic": "REF-DO-177-001",
  "nome_do_servico": "Dados de Exemplo",
  "descricao_do_servico": "Dados de Exemplo",
  "categoria_do_catalog": "Dados de Exemplo",
  "preco_custo_estimado": 150.45
}
```

## # Citations

1. Gestão de Catálogo de Serviços (ITIL v4), Processo de Provisionamento de Acessos e Recursos corporativos.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
