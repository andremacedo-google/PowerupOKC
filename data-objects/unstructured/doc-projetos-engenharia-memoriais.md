---
id: DO-213
name: "Documentos de Projetos de Engenharia (Memoriais, Plantas)"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Interno"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Não Estruturado"
  - "LeanIX-v4"
---

# Documentos de Projetos de Engenharia (Memoriais, Plantas) (DO-213)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança da base de conhecimento não estruturada **Documentos de Projetos de Engenharia (Memoriais, Plantas)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Conjunto de desenhos, textos e memórias que descrevem em detalhes todas as fases de construção, modernização ou reforço de uma subestação, usina ou linha de transmissão.

Este objeto de dados não estruturado é de extrema importância para as regras de conformidade regulatória (conforme as diretrizes de regulação tarifária, fiscalização ou as instruções operacionais do SIN). Sua correta catalogação impede silos de conhecimento e vazamentos de informações classificadas.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade, linhagem e governança de dados no repositório corporativo da PowerUp, este Data Object mantém as seguintes conexões estáveis:

*   **Subdomínio de Dados (Nível 1):** Técnico e Operacional / Engenharia e Projetos
*   **Sistemas e Aplicações Relacionadas (Applications):** AutoCAD, GED da Engenharia, SAP PS, WFM (obras)
*   **Repositório/Sistema de Registro Canônico (System of Truth):** Repositório Técnico de Engenharia (as-built)
*   **Capacidade de Negócio Relacionada:** Engenharia, Implantação de Projetos de CAPEX, Comissionamento e Unitização de Ativos
*   **Documento de Referência (Mestre):** sim

## # Schema

Este ativo de dados não estruturados de referência é composto e regido pelos seguintes temas críticos e tipos de informações:

*   **Informações Críticas e Conteúdo Típico:** Memorial descritivo (justificativa, critérios de dimensionamento), plantas baixas, diagramas unifilares/multifilares (CAD), rotas de cabos, e relatórios de comissionamento físico.
*   **Classificação de Privacidade e Sensibilidade (Compliance/LGPD):** Interno

## # Examples

Abaixo está exemplificado um rascunho de metadados em formato estruturado representando o objeto documental, indicando as variáveis comumente contidas em seu fluxo de indexação:

```json
{"memorial_descritivo_se": {"titulo": "Construção e Ampliação da Subestação Leste 138kV", "etapas": ["Terraplenagem e drenagem do terreno", "Instalação das malhas de aterramento", "Montagem de pórticos e fixação de barramentos"], "status": "Liberado para obras"}}
```

## # Citations

1. [Manual de Governança de Informações Não Estruturadas PowerupOKC] - Rege os padrões de indexação, controle e privacidade das bases de conhecimento setoriais.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
