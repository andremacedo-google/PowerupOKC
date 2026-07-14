---
id: DO-219
name: "Contratos de Compra e Venda de Energia (PPAs)"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Confidencial"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Não Estruturado"
  - "LeanIX-v4"
---

# Contratos de Compra e Venda de Energia (PPAs) (DO-219)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança da base de conhecimento não estruturada **Contratos de Compra e Venda de Energia (PPAs)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Acordos jurídicos e comerciais de longo prazo celebrados entre geradoras/comercializadoras e compradores de energia, no ambiente regulado (ACR) ou livre (ACL).

Este objeto de dados não estruturado é de extrema importância para as regras de conformidade regulatória (conforme as diretrizes de regulação tarifária, fiscalização ou as instruções operacionais do SIN). Sua correta catalogação impede silos de conhecimento e vazamentos de informações classificadas.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade, linhagem e governança de dados no repositório corporativo da PowerUp, este Data Object mantém as seguintes conexões estáveis:

*   **Subdomínio de Dados (Nível 1):** Jurídico e Contratual / Contratos Estratégicos
*   **Sistemas e Aplicações Relacionadas (Applications):** SAP CLM, ETRM Interno, GED Jurídico, CCEE (SCL)
*   **Repositório/Sistema de Registro Canônico (System of Truth):** Arquivo Contratual Corporativo / SAP CLM
*   **Capacidade de Negócio Relacionada:** Comercialização de Energia, Trading, Gestão de Riscos de Preço e Faturamento
*   **Documento de Referência (Mestre):** nao

## # Schema

Este ativo de dados não estruturados de referência é composto e regido pelos seguintes temas críticos e tipos de informações:

*   **Informações Críticas e Conteúdo Típico:** Montante de suprimento contratado (MWm), flexibilidades de sazonalização, fórmulas de reajuste (IPCA/IGPM), garantias financeiras, penalidades por atraso em comissionamento e inadimplência.
*   **Classificação de Privacidade e Sensibilidade (Compliance/LGPD):** Confidencial

## # Examples

Abaixo está exemplificado um rascunho de metadados em formato estruturado representando o objeto documental, indicando as variáveis comumente contidas em seu fluxo de indexação:

```json
{"ppa_contrato_exemplo": {"tipo_contrato": "CCEAR (Contrato de Comercialização no Ambiente Regulado)", "vendedor": "PowerUp Geração Renovável S.A.", "volume_mwm": 25.4, "indexador": "IPCA", "limite_garantia": "Fiança Bancária de 5% do valor do contrato"}}
```

## # Citations

1. [Manual de Governança de Informações Não Estruturadas PowerupOKC] - Rege os padrões de indexação, controle e privacidade das bases de conhecimento setoriais.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
