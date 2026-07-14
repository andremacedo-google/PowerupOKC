---
id: DO-209
name: "Formulário de Referência (FRE)"
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

# Formulário de Referência (FRE) (DO-209)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança da base de conhecimento não estruturada **Formulário de Referência (FRE)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Relatório anual exigido pela CVM para companhias abertas, oferecendo um diagnóstico detalhado da empresa sobre aspectos de finanças, governança e fatores de risco.

Este objeto de dados não estruturado é de extrema importância para as regras de conformidade regulatória (conforme as diretrizes de regulação tarifária, fiscalização ou as instruções operacionais do SIN). Sua correta catalogação impede silos de conhecimento e vazamentos de informações classificadas.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade, linhagem e governança de dados no repositório corporativo da PowerUp, este Data Object mantém as seguintes conexões estáveis:

*   **Subdomínio de Dados (Nível 1):** Corporativo e Governança / Divulgação Pública
*   **Sistemas e Aplicações Relacionadas (Applications):** Sistema de Divulgação da CVM, Canal de Relação com Investidores (RI), SAP CLM
*   **Repositório/Sistema de Registro Canônico (System of Truth):** Canal de Comunicação com a CVM / Portal de RI
*   **Capacidade de Negócio Relacionada:** Relação com Investidores, Reporte Governamental e Mercado de Capitais
*   **Documento de Referência (Mestre):** nao

## # Schema

Este ativo de dados não estruturados de referência é composto e regido pelos seguintes temas críticos e tipos de informações:

*   **Informações Críticas e Conteúdo Típico:** Descrição detalhada dos negócios de energia (G-T-D-C), matriz qualitativa de fatores de risco (climáticos/hidrológicos), comentários dos administradores, disputas regulatórias e relatórios ASG.
*   **Classificação de Privacidade e Sensibilidade (Compliance/LGPD):** Público

## # Examples

Abaixo está exemplificado um rascunho de metadados em formato estruturado representando o objeto documental, indicando as variáveis comumente contidas em seu fluxo de indexação:

```json
{"fre_secao_riscos": {"risco_hidrologico": "A exposição financeira do portfólio hídrico no mercado de curto prazo devido ao fator de escala do MRE", "risco_regulatorio": "Alterações nas regras de ressarcimento por perturbações"}}
```

## # Citations

1. [Manual de Governança de Informações Não Estruturadas PowerupOKC] - Rege os padrões de indexação, controle e privacidade das bases de conhecimento setoriais.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
