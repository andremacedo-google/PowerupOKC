---
id: DO-203
name: "PRORET - Procedimentos de Regulação Tarifária"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Público"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Não Estruturado"
  - "LeanIX-v4"
---

# PRORET - Procedimentos de Regulação Tarifária (DO-203)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança da base de conhecimento não estruturada **PRORET - Procedimentos de Regulação Tarifária** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Normas consolidadas pela ANEEL que definem a metodologia de cálculo e revisão de tarifas e receitas garantidas das concessionárias de distribuição, transmissão e geração.

Este objeto de dados não estruturado é de extrema importância para as regras de conformidade regulatória (conforme as diretrizes de regulação tarifária, fiscalização ou as instruções operacionais do SIN). Sua correta catalogação impede silos de conhecimento e vazamentos de informações classificadas.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade, linhagem e governança de dados no repositório corporativo da PowerUp, este Data Object mantém as seguintes conexões estáveis:

*   **Subdomínio de Dados (Nível 1):** Regulatório e Planejamento / Regulação Tarifária
*   **Sistemas e Aplicações Relacionadas (Applications):** Portal ANEEL, SharePoint Financeiro, SAP S/4HANA (FI-AA)
*   **Repositório/Sistema de Registro Canônico (System of Truth):** Biblioteca Reguladora da ANEEL
*   **Capacidade de Negócio Relacionada:** Revisão Tarifária Periódica (RTP) e Reajuste Tarifário Anual (RTA)
*   **Documento de Referência (Mestre):** sim

## # Schema

Este ativo de dados não estruturados de referência é composto e regido pelos seguintes temas críticos e tipos de informações:

*   **Informações Críticas e Conteúdo Típico:** Procedimentos para as Revisões Tarifárias Periódicas (RTP), critérios para cálculo da Base de Remuneração Regulatória (BRR), despesas eficientes de PMSO (OPEX), taxa WACC e cálculo do Fator X.
*   **Classificação de Privacidade e Sensibilidade (Compliance/LGPD):** Público

## # Examples

Abaixo está exemplificado um rascunho de metadados em formato estruturado representando o objeto documental, indicando as variáveis comumente contidas em seu fluxo de indexação:

```json
{"proret_submodulo_2_2": {"titulo": "Custo de PMSO Eficiente", "itens": ["Pessoal", "Material", "Serviços de Terceiros", "Outros"]}}
```

## # Citations

1. [Manual de Governança de Informações Não Estruturadas PowerupOKC] - Rege os padrões de indexação, controle e privacidade das bases de conhecimento setoriais.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
