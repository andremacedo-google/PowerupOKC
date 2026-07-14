---
id: DO-161
name: "Plano de Contas"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Confidencial (Financeiro)"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Nível 3"
  - "Corporativo"
  - "Financeiro"
  - "LeanIX-v4"
---

# Plano de Contas (DO-161)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Plano de Contas** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Estrutura lógica e unificada que organiza as contas do razão (Chart of Accounts) para o registro padronizado de eventos societários (IFRS) e regulatórios da distribuidora ou geradora. No setor elétrico brasileiro, o Plano de Contas é alinhado de forma integrada ao Plano de Contas Auxiliar da ANEEL, conforme estabelecido no Manual de Contabilidade do Setor Elétrico (MCSE).

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Financeiro
*   **Sistemas e Aplicações que Manipulam (Applications):** ERP (SAP S/4HANA FI-GL), Sistemas de Reporte Regulatório
*   **Sistema de Registro Canônico (System of Truth):** ERP (SAP S/4HANA FI)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `Código da Conta Contábil (G/L Account Code)` | String (ID) | Atributo técnico representando o campo mestre 'Código da Conta Contábil (G/L Account Code)'. |
| `Nome/Descrição da Conta` | String | Atributo técnico representando o campo mestre 'Nome/Descrição da Conta'. |
| `Tipo de Conta (Ativo` | String (Enum) | Atributo técnico representando o campo mestre 'Tipo de Conta (Ativo'. |
| `Passivo` | String | Atributo técnico representando o campo mestre 'Passivo'. |
| `Patrimônio Líquido` | String (ID) | Atributo técnico representando o campo mestre 'Patrimônio Líquido'. |
| `Receita` | String | Atributo técnico representando o campo mestre 'Receita'. |
| `Despesa)` | String | Atributo técnico representando o campo mestre 'Despesa)'. |
| `Grupo de Contas` | String | Atributo técnico representando o campo mestre 'Grupo de Contas'. |
| `Código de Mapeamento Regulatório (ANEEL TUC)` | String | Atributo técnico representando o campo mestre 'Código de Mapeamento Regulatório (ANEEL TUC)'. |
| `Status (Ativo` | String (Enum) | Atributo técnico representando o campo mestre 'Status (Ativo'. |
| `Bloqueado)` | String | Atributo técnico representando o campo mestre 'Bloqueado)'. |
| `Variante de Plano de Contas.` | String | Atributo técnico representando o campo mestre 'Variante de Plano de Contas.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "codigo_da_conta_cont": "REF-DO-161-001",
  "nome_descricao_da_co": "Dados de Exemplo",
  "tipo_de_conta_ativo": "Active",
  "passivo": "Dados de Exemplo",
  "patrimonio_liquido": "REF-DO-161-001"
}
```

## # Citations

1. Contabilidade Geral, Consolidação Financeira Societária (IFRS), ANEEL: Manual de Contabilidade do Setor Elétrico (MCSE) / Fechamento Contábil.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
