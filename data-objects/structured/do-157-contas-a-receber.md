---
id: DO-157
name: "Contas a Receber"
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

# Contas a Receber (DO-157)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Contas a Receber** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Representa os direitos de crédito da distribuidora, geradora ou comercializadora decorrentes do faturamento de faturas de energia (ciclo comercial Meter-to-Cash), fornecimento de serviços de rede (como TUSD/TE), ou venda de energia no Ambiente de Contratação Livre (ACL) e curto prazo (CCEE), que aguardam liquidação financeira por parte dos clientes ou contrapartes. No padrão CIM, está correlacionado à classe CustomerBill e integra-se à conta de compensação do sub-razão (FI-CA/FI-AR) e ao razão geral (FI-GL).

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Financeiro
*   **Sistemas e Aplicações que Manipulam (Applications):** CIS (SAP IS-U / CCS, Oracle Utilities CCS), ERP (SAP S/4HANA FI-AR/FI-CA), ETRM (para comercializadoras)
*   **Sistema de Registro Canônico (System of Truth):** CIS (SAP IS-U / FI-CA) para varejo/distribuição ou ERP (SAP S/4HANA FI-AR) para contratos bilaterais de comercialização e grandes consumidores (Grupo A)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Título` | String (ID) | Atributo técnico representando o campo mestre 'ID do Título'. |
| `Número da Fatura Associada` | String | Atributo técnico representando o campo mestre 'Número da Fatura Associada'. |
| `ID do Parceiro de Negócio (BP ID)` | String (ID) | Atributo técnico representando o campo mestre 'ID do Parceiro de Negócio (BP ID)'. |
| `ID da Conta Contrato` | String (ID) | Atributo técnico representando o campo mestre 'ID da Conta Contrato'. |
| `Valor Principal` | Float | Atributo técnico representando o campo mestre 'Valor Principal'. |
| `Valor de Juros/Multas por Atraso (Encargos de Mora)` | Float | Atributo técnico representando o campo mestre 'Valor de Juros/Multas por Atraso (Encargos de Mora)'. |
| `Impostos Retidos (ICMS` | String (ID) | Atributo técnico representando o campo mestre 'Impostos Retidos (ICMS'. |
| `PIS` | String | Atributo técnico representando o campo mestre 'PIS'. |
| `COFINS)` | String | Atributo técnico representando o campo mestre 'COFINS)'. |
| `Data de Emissão` | DateTime | Atributo técnico representando o campo mestre 'Data de Emissão'. |
| `Data de Vencimento` | DateTime | Atributo técnico representando o campo mestre 'Data de Vencimento'. |
| `Status de Cobrança (Em Aberto` | String (Enum) | Atributo técnico representando o campo mestre 'Status de Cobrança (Em Aberto'. |
| `Parcial` | String | Atributo técnico representando o campo mestre 'Parcial'. |
| `Liquidado)` | String (ID) | Atributo técnico representando o campo mestre 'Liquidado)'. |
| `Código de Barras / Linha Digitável.` | String | Atributo técnico representando o campo mestre 'Código de Barras / Linha Digitável.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_titulo": "REF-DO-157-001",
  "numero_da_fatura_ass": "Dados de Exemplo",
  "id_do_parceiro_de_ne": "REF-DO-157-001",
  "id_da_conta_contrato": "REF-DO-157-001",
  "valor_principal": 150.45
}
```

## # Citations

1. Ciclo comercial Meter-to-Cash (M2C), Contabilidade Financeira Societária (IFRS 9 / CPC 48 - Mensuração de Perdas de Crédito Esperadas), ANEEL PRODIST Módulo 6 (Informações Requeridas e Faturamento)
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
