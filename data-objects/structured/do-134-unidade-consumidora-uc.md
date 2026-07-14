---
id: DO-134
name: "Unidade Consumidora (UC)"
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

# Unidade Consumidora (UC) (DO-134)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Unidade Consumidora (UC)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Conjunto de instalações e equipamentos elétricos caracterizado pelo recebimento de energia em um só ponto de entrega, com medição individualizada. Conecta os dados técnicos aos comerciais. No CIM, é modelado pelas classes ServiceLocation, ServiceDeliveryPoint e UsagePoint.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Clientes / Cadastro
*   **Sistemas e Aplicações que Manipulam (Applications):** CIS, GIS, MDM
*   **Sistema de Registro Canônico (System of Truth):** CIS (Customer Information System)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID da UC (código único de 15 dígitos)` | String (ID) | Atributo técnico representando o campo mestre 'ID da UC (código único de 15 dígitos)'. |
| `Endereço da Instalação` | String | Atributo técnico representando o campo mestre 'Endereço da Instalação'. |
| `Classe/Subclasse de Consumo (UCBT.CNAE)` | String | Atributo técnico representando o campo mestre 'Classe/Subclasse de Consumo (UCBT.CNAE)'. |
| `Grupo Tarifário (A/B)` | String | Atributo técnico representando o campo mestre 'Grupo Tarifário (A/B)'. |
| `Carga Instalada (UCBT.CAR_INST)` | String | Atributo técnico representando o campo mestre 'Carga Instalada (UCBT.CAR_INST)'. |
| `Roteiro de Leitura` | String | Atributo técnico representando o campo mestre 'Roteiro de Leitura'. |
| `Tensão de Conexão.` | String | Atributo técnico representando o campo mestre 'Tensão de Conexão.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_da_uc_codigo_unic": "REF-DO-134-001",
  "endereco_da_instalac": "Dados de Exemplo",
  "classe_subclasse_de_": "Dados de Exemplo",
  "grupo_tarifario_a_b": "Dados de Exemplo",
  "carga_instalada_ucbt": "Dados de Exemplo"
}
```

## # Citations

1. ANEEL: PRODIST Módulo 3, BDGD
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
