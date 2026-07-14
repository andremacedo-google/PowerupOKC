---
id: DO-139
name: "Garantia Física"
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
  - "Comercialização"
  - "LeanIX-v4"
---

# Garantia Física (DO-139)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Garantia Física** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Montante máximo de energia comercializável que uma usina geradora está autorizada a transacionar sob contratos no ACL/ACR, baseado na produtibilidade de longo prazo homologada pelo MME/ANEEL.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Clientes / Comercialização
*   **Sistemas e Aplicações que Manipulam (Applications):** Sistemas CCEE, ETRM
*   **Sistema de Registro Canônico (System of Truth):** CCEE / ANEEL

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ceg` | String | Atributo técnico representando o campo mestre 'ceg'. |
| `val_garantia_fisica (MWh)` | Float | Atributo técnico representando o campo mestre 'val_garantia_fisica (MWh)'. |
| `val_lastro_contratado` | Float | Atributo técnico representando o campo mestre 'val_lastro_contratado'. |
| `val_cota_alocada` | Float | Atributo técnico representando o campo mestre 'val_cota_alocada'. |
| `fator_escala_mre.` | String | Atributo técnico representando o campo mestre 'fator_escala_mre.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "ceg": "Dados de Exemplo",
  "val_garantia_fisica_": 150.45,
  "val_lastro_contratad": 150.45,
  "val_cota_alocada": 150.45,
  "fator_escala_mre": "Dados de Exemplo"
}
```

## # Citations

1. CCEE: Regras de Comercialização (Módulo 3)
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
