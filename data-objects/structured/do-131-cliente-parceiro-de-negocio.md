---
id: DO-131
name: "Cliente (Parceiro de Negócio)"
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
  - "Clientes"
  - "Cadastro"
  - "LeanIX-v4"
---

# Cliente (Parceiro de Negócio) (DO-131)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Cliente (Parceiro de Negócio)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Entidade (pessoa física ou jurídica) que possui uma relação contratual com a distribuidora. No padrão CIM, é representado pela classe Customer.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Clientes / Cadastro
*   **Sistemas e Aplicações que Manipulam (Applications):** CIS (SAP IS-U), CRM
*   **Sistema de Registro Canônico (System of Truth):** CRM / CIS

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Cliente` | String (ID) | Atributo técnico representando o campo mestre 'ID do Cliente'. |
| `CPF/CNPJ` | String (ID) | Atributo técnico representando o campo mestre 'CPF/CNPJ'. |
| `Nome/Razão Social` | String | Atributo técnico representando o campo mestre 'Nome/Razão Social'. |
| `Contatos (Telefone` | String | Atributo técnico representando o campo mestre 'Contatos (Telefone'. |
| `E-mail)` | String | Atributo técnico representando o campo mestre 'E-mail)'. |
| `Endereço de Correspondência` | String | Atributo técnico representando o campo mestre 'Endereço de Correspondência'. |
| `Grupo de Faturamento.` | String | Atributo técnico representando o campo mestre 'Grupo de Faturamento.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_cliente": "REF-DO-131-001",
  "cpf_cnpj": "REF-DO-131-001",
  "nome_razao_social": "Dados de Exemplo",
  "contatos_telefone": "Dados de Exemplo",
  "e_mail": "Dados de Exemplo"
}
```

## # Citations

1. Processo 'Meter-to-Cash'
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
