---
id: DO-176
name: "Item de Configuração (CI)"
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

# Item de Configuração (CI) (DO-176)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Item de Configuração (CI)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Qualquer componente de infraestrutura tecnológica (físico ou lógico), software, rede ou serviço de TI/TO que necessita ser gerenciado para garantir a entrega de um serviço de energia. Representa a espinha dorsal do CMDB (Configuration Management Database), documentando atributos operacionais e dependências críticas na rede (como servidores SCADA/ADMS, RTUs, IEDs e switches industriais).

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Tecnologia da Informação
*   **Sistemas e Aplicações que Manipulam (Applications):** ServiceNow CMDB (ITOM Discovery / Service Mapping), Micro Focus UCMDB, Device42
*   **Sistema de Registro Canônico (System of Truth):** ServiceNow CMDB (Single Source of Truth de Configuração)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Item de Configuração (CI Name)` | String (ID) | Atributo técnico representando o campo mestre 'ID do Item de Configuração (CI Name)'. |
| `Classe de CI (Servidor` | String (ID) | Atributo técnico representando o campo mestre 'Classe de CI (Servidor'. |
| `PLC` | String | Atributo técnico representando o campo mestre 'PLC'. |
| `Banco de Dados` | String | Atributo técnico representando o campo mestre 'Banco de Dados'. |
| `Aplicação)` | String | Atributo técnico representando o campo mestre 'Aplicação)'. |
| `Status de Configuração (Ativo` | String (Enum) | Atributo técnico representando o campo mestre 'Status de Configuração (Ativo'. |
| `Inativo` | String | Atributo técnico representando o campo mestre 'Inativo'. |
| `Em Teste)` | String | Atributo técnico representando o campo mestre 'Em Teste)'. |
| `Versão do OS / Firmware` | Float | Atributo técnico representando o campo mestre 'Versão do OS / Firmware'. |
| `Endereço IP / MAC` | String | Atributo técnico representando o campo mestre 'Endereço IP / MAC'. |
| `Localização Física (Subestação / Data Center)` | DateTime | Atributo técnico representando o campo mestre 'Localização Física (Subestação / Data Center)'. |
| `CIs Relacionados (Pai/Filho)` | String | Atributo técnico representando o campo mestre 'CIs Relacionados (Pai/Filho)'. |
| `Criticidade Operacional (DORA Critical).` | String (ID) | Atributo técnico representando o campo mestre 'Criticidade Operacional (DORA Critical).'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_item_de_config": "REF-DO-176-001",
  "classe_de_ci_servido": "REF-DO-176-001",
  "plc": "Dados de Exemplo",
  "banco_de_dados": "Dados de Exemplo",
  "aplicacao": "Dados de Exemplo"
}
```

## # Citations

1. Gestão de Configuração e Ativos de Serviço (SACM / ITIL v4), Modelo Purdue de Segurança Industrial, Resolução Normativa ANEEL nº 964/2021 (Cibersegurança), DORA (Digital Operational Resilience Act).
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
