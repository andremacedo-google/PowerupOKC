---
id: DO-165
name: "Colaboradores Externos"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Restrito (LGPD)"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Nível 3"
  - "Corporativo"
  - "Recursos Humanos"
  - "LeanIX-v4"
---

# Colaboradores Externos (DO-165)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Colaboradores Externos** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Profissionais de prestadores de serviço externos, empreiteiras de campo ou temporários (Extended Workers) que necessitam de credenciamento e validação de NRs (NR-10, NR-35) para atuar na rede.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Recursos Humanos
*   **Sistemas e Aplicações que Manipulam (Applications):** HCM (SAP SuccessFactors / Fieldglass), ServiceNow
*   **Sistema de Registro Canônico (System of Truth):** HCM / VMS (Vendor Management System)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Colaborador Externo` | String (ID) | Atributo técnico representando o campo mestre 'ID do Colaborador Externo'. |
| `Nome` | String | Atributo técnico representando o campo mestre 'Nome'. |
| `CPF` | String (ID) | Atributo técnico representando o campo mestre 'CPF'. |
| `Empresa Prestadora (Fornecedor ID)` | String (ID) | Atributo técnico representando o campo mestre 'Empresa Prestadora (Fornecedor ID)'. |
| `Certificações Operacionais (NRs)` | String | Atributo técnico representando o campo mestre 'Certificações Operacionais (NRs)'. |
| `Status de Acesso.` | String (Enum) | Atributo técnico representando o campo mestre 'Status de Acesso.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_colaborador_ex": "REF-DO-165-001",
  "nome": "Dados de Exemplo",
  "cpf": "REF-DO-165-001",
  "empresa_prestadora_f": "Dados de Exemplo",
  "certificacoes_operac": "Dados de Exemplo"
}
```

## # Citations

1. Gestão de Mão de Obra de Terceiros, Normas Regulamentadoras (NR-10, NR-35)
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
