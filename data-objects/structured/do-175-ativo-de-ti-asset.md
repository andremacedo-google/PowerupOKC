---
id: DO-175
name: "Ativo de TI (Asset)"
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

# Ativo de TI (Asset) (DO-175)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Ativo de TI (Asset)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Objeto de dados que foca no ciclo de vida financeiro, contratual e administrativo de um bem de tecnologia da informação ou operação (hardware, licença de software, dispositivo de rede). Gerencia aspectos de custos, fornecedores, depreciação e propriedade, em vez de relações operacionais em tempo real.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Tecnologia da Informação
*   **Sistemas e Aplicações que Manipulam (Applications):** ServiceNow ITAM (Asset Management), SAP S/4HANA (FI-AA / MM)
*   **Sistema de Registro Canônico (System of Truth):** ServiceNow ITAM / ERP (SAP S/4HANA)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Ativo de TI` | String (ID) | Atributo técnico representando o campo mestre 'ID do Ativo de TI'. |
| `Tipo de Ativo (Hardware` | String (Enum) | Atributo técnico representando o campo mestre 'Tipo de Ativo (Hardware'. |
| `Software` | String | Atributo técnico representando o campo mestre 'Software'. |
| `Dispositivo)` | String | Atributo técnico representando o campo mestre 'Dispositivo)'. |
| `Número de Série` | String | Atributo técnico representando o campo mestre 'Número de Série'. |
| `Fornecedor (ID do Fornecedor)` | String (ID) | Atributo técnico representando o campo mestre 'Fornecedor (ID do Fornecedor)'. |
| `Custo de Aquisição` | Float | Atributo técnico representando o campo mestre 'Custo de Aquisição'. |
| `Data de Compra` | DateTime | Atributo técnico representando o campo mestre 'Data de Compra'. |
| `Data de Garantia` | DateTime | Atributo técnico representando o campo mestre 'Data de Garantia'. |
| `Status do Ciclo de Vida (Em Estoque` | String (ID) | Atributo técnico representando o campo mestre 'Status do Ciclo de Vida (Em Estoque'. |
| `Em Uso` | String | Atributo técnico representando o campo mestre 'Em Uso'. |
| `Descartado)` | String | Atributo técnico representando o campo mestre 'Descartado)'. |
| `Centro de Custo Relacionado` | Float | Atributo técnico representando o campo mestre 'Centro de Custo Relacionado'. |
| `Proprietário (Owner).` | String | Atributo técnico representando o campo mestre 'Proprietário (Owner).'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_ativo_de_ti": "REF-DO-175-001",
  "tipo_de_ativo_hardwa": "Active",
  "software": "Dados de Exemplo",
  "dispositivo": "Dados de Exemplo",
  "numero_de_serie": "Dados de Exemplo"
}
```

## # Citations

1. Gestão de Ativos de TI (ITAM / ITIL v4), Gestão de Custos e Rastreabilidade de TI, Conformidade de Licenciamento de Software.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
