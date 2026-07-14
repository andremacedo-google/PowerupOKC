---
id: DO-101
name: "Ativo (Técnico)"
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
  - "Cadastro de Ativos"
  - "LeanIX-v4"
---

# Ativo (Técnico) (DO-101)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Ativo (Técnico)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Representação de um equipamento da rede (ex: Poste, Transformador) ou usina. No SAP, é o Equipamento/Local de Instalação (PM) que se conecta ao Ativo Fixo (FI-AA). No CIM, mapeia-se para classes como PowerTransformer, ACLineSegment, Structure.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Ativos / Cadastro de Ativos
*   **Sistemas e Aplicações que Manipulam (Applications):** EAM/SAP PM, GIS, ERP
*   **Sistema de Registro Canônico (System of Truth):** GIS (Cadastro Técnico) / EAM

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Ativo` | String (ID) | Atributo técnico representando o campo mestre 'ID do Ativo'. |
| `Tipo` | String (Enum) | Atributo técnico representando o campo mestre 'Tipo'. |
| `Localização Geográfica (GIS)` | String | Atributo técnico representando o campo mestre 'Localização Geográfica (GIS)'. |
| `Dados de Placa` | String | Atributo técnico representando o campo mestre 'Dados de Placa'. |
| `Parâmetros Elétricos` | String | Atributo técnico representando o campo mestre 'Parâmetros Elétricos'. |
| `Garantia Física (usinas)` | String | Atributo técnico representando o campo mestre 'Garantia Física (usinas)'. |
| `Código do Ativo no ONS/CCEE.` | String | Atributo técnico representando o campo mestre 'Código do Ativo no ONS/CCEE.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_ativo": "REF-DO-101-001",
  "tipo": "Active",
  "localizacao_geografi": "Dados de Exemplo",
  "dados_de_placa": "Dados de Exemplo",
  "parametros_eletricos": "Dados de Exemplo"
}
```

## # Citations

1. ANEEL (BDGD), ONS (Submódulo 2.1), CCEE (Cadastro)
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
