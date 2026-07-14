---
id: DO-145
name: "Leitura de Medição"
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
  - "Medição"
  - "LeanIX-v4"
---

# Leitura de Medição (DO-145)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Leitura de Medição** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Registro do consumo de energia de um medidor em um determinado momento. O MDM realiza o processo de VEE (Validação, Estimação e Edição) nesses dados antes de enviá-los ao CIS para faturamento.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Clientes / Medição
*   **Sistemas e Aplicações que Manipulam (Applications):** MDM (Oracle MDM), CIS
*   **Sistema de Registro Canônico (System of Truth):** MDM (Meter Data Management)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID da Leitura` | String (ID) | Atributo técnico representando o campo mestre 'ID da Leitura'. |
| `ID do Medidor` | String (ID) | Atributo técnico representando o campo mestre 'ID do Medidor'. |
| `Data/Hora (Timestamp)` | DateTime | Atributo técnico representando o campo mestre 'Data/Hora (Timestamp)'. |
| `Valor da Leitura (Ativa/Reativa)` | Float | Atributo técnico representando o campo mestre 'Valor da Leitura (Ativa/Reativa)'. |
| `Tipo de Leitura (Manual` | String (Enum) | Atributo técnico representando o campo mestre 'Tipo de Leitura (Manual'. |
| `Remota/AMI` | String | Atributo técnico representando o campo mestre 'Remota/AMI'. |
| `Autoleitura)` | String | Atributo técnico representando o campo mestre 'Autoleitura)'. |
| `Status da Validação (Válida` | String (ID) | Atributo técnico representando o campo mestre 'Status da Validação (Válida'. |
| `Estimada` | String | Atributo técnico representando o campo mestre 'Estimada'. |
| `Editada).` | String | Atributo técnico representando o campo mestre 'Editada).'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_da_leitura": "REF-DO-145-001",
  "id_do_medidor": "REF-DO-145-001",
  "data_hora_timestamp": "2026-07-14T06:55:00Z",
  "valor_da_leitura_ati": 150.45,
  "tipo_de_leitura_manu": "Active"
}
```

## # Citations

1. ANEEL: PRODIST Módulo 5
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
