---
id: DO-146
name: "Medidor"
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

# Medidor (DO-146)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Medidor** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Equipamento físico instalado na UC que registra o consumo de energia elétrica. É um ativo da distribuidora.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Clientes / Medição
*   **Sistemas e Aplicações que Manipulam (Applications):** MDM, CIS, EAM
*   **Sistema de Registro Canônico (System of Truth):** CIS / MDM

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Medidor (Número de Série)` | String (ID) | Atributo técnico representando o campo mestre 'ID do Medidor (Número de Série)'. |
| `Modelo` | String | Atributo técnico representando o campo mestre 'Modelo'. |
| `Tipo (Eletrônico` | String (Enum) | Atributo técnico representando o campo mestre 'Tipo (Eletrônico'. |
| `Inteligente/AMI)` | String | Atributo técnico representando o campo mestre 'Inteligente/AMI)'. |
| `Localização Geográfica (via GIS)` | String | Atributo técnico representando o campo mestre 'Localização Geográfica (via GIS)'. |
| `Status (Ativo` | String (Enum) | Atributo técnico representando o campo mestre 'Status (Ativo'. |
| `Em estoque` | String | Atributo técnico representando o campo mestre 'Em estoque'. |
| `Retirado)` | String | Atributo técnico representando o campo mestre 'Retirado)'. |
| `Classe de Exatidão` | String (ID) | Atributo técnico representando o campo mestre 'Classe de Exatidão'. |
| `Fator de Calibração.` | String | Atributo técnico representando o campo mestre 'Fator de Calibração.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_medidor_numero": "REF-DO-146-001",
  "modelo": "Dados de Exemplo",
  "tipo_eletronico": "Active",
  "inteligente_ami": "Dados de Exemplo",
  "localizacao_geografi": "Dados de Exemplo"
}
```

## # Citations

1. ANEEL: PRODIST Módulo 5
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
