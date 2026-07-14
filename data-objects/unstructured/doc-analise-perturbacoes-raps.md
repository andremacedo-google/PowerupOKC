---
id: DO-214
name: "Relatórios de Análise de Perturbações (RAPs)"
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

# Relatórios de Análise de Perturbações (RAPs) (DO-214)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança da base de conhecimento não estruturada **Relatórios de Análise de Perturbações (RAPs)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Documento técnico detalhado elaborado após uma interrupção significativa ou blecaute no Sistema Interligado Nacional (SIN), para investigar as causas e recomendar ações de melhoria.

Este objeto de dados não estruturado é de extrema importância para as regras de conformidade regulatória (conforme as diretrizes de regulação tarifária, fiscalização ou as instruções operacionais do SIN). Sua correta catalogação impede silos de conhecimento e vazamentos de informações classificadas.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade, linhagem e governança de dados no repositório corporativo da PowerUp, este Data Object mantém as seguintes conexões estáveis:

*   **Subdomínio de Dados (Nível 1):** Técnico e Operacional / Operação do Sistema
*   **Sistemas e Aplicações Relacionadas (Applications):** SAGER (ONS), Sistema AOT (Análise de Ocorrências da Transmissão), SCADA
*   **Repositório/Sistema de Registro Canônico (System of Truth):** Acervo Digital do ONS / Auditoria de Perturbações
*   **Capacidade de Negócio Relacionada:** Engenharia de Proteção e Controle, Restabelecimento do Sistema, Gestão de Confiabilidade
*   **Documento de Referência (Mestre):** nao

## # Schema

Este ativo de dados não estruturados de referência é composto e regido pelos seguintes temas críticos e tipos de informações:

*   **Informações Críticas e Conteúdo Típico:** Cronologia exata do evento (Sequence of Events), dados de oscilografia coletados por relés, análise de causa raiz de atuação das proteções e recomendações corretivas vinculantes.
*   **Classificação de Privacidade e Sensibilidade (Compliance/LGPD):** Confidencial

## # Examples

Abaixo está exemplificado um rascunho de metadados em formato estruturado representando o objeto documental, indicando as variáveis comumente contidas em seu fluxo de indexação:

```json
{"rap_2026_07_04": {"interrupcao": "Atuação da proteção de distância da LT-138kV Leste-Centro", "causa": "Descarga atmosférica direta na torre 45", "recomendações": ["Substituir cabos para-raios da seção afetada", "Reajustar curvas de sobrecorrente do relé SEL-311C"]}}
```

## # Citations

1. [Manual de Governança de Informações Não Estruturadas PowerupOKC] - Rege os padrões de indexação, controle e privacidade das bases de conhecimento setoriais.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
