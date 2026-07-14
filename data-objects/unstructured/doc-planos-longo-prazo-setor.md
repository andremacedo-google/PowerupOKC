---
id: DO-208
name: "Planos de Longo Prazo do Setor (PNE / PDE / PAR / PEL)"
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

# Planos de Longo Prazo do Setor (PNE / PDE / PAR / PEL) (DO-208)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança da base de conhecimento não estruturada **Planos de Longo Prazo do Setor (PNE / PDE / PAR / PEL)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Estudos estratégicos de planejamento decenal (PDE) e nacional (PNE) de expansão de energia elétrica e planos de transmissão (PAR) de médio prazo com foco no SIN.

Este objeto de dados não estruturado é de extrema importância para as regras de conformidade regulatória (conforme as diretrizes de regulação tarifária, fiscalização ou as instruções operacionais do SIN). Sua correta catalogação impede silos de conhecimento e vazamentos de informações classificadas.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade, linhagem e governança de dados no repositório corporativo da PowerUp, este Data Object mantém as seguintes conexões estáveis:

*   **Subdomínio de Dados (Nível 1):** Regulatório e Planejamento / Planejamento e Operação
*   **Sistemas e Aplicações Relacionadas (Applications):** Portal da EPE, Portal do MME, Acervo Digital do ONS
*   **Repositório/Sistema de Registro Canônico (System of Truth):** Biblioteca Digital da EPE / ONS
*   **Capacidade de Negócio Relacionada:** Planejamento de Portfólio, Expansão de Ativos e CAPEX de Longo Prazo
*   **Documento de Referência (Mestre):** sim

## # Schema

Este ativo de dados não estruturados de referência é composto e regido pelos seguintes temas críticos e tipos de informações:

*   **Informações Críticas e Conteúdo Típico:** Premissas macroeconômicas de crescimento de demanda, metas indicativas de expansão da matriz por fonte (3Ds), obras de reforço e limites de intercâmbio, e desafios de novas cargas (data centers).
*   **Classificação de Privacidade e Sensibilidade (Compliance/LGPD):** Público

## # Examples

Abaixo está exemplificado um rascunho de metadados em formato estruturado representando o objeto documental, indicando as variáveis comumente contidas em seu fluxo de indexação:

```json
{"pde_2035": {"entidade_editora": "EPE", "foco": "Estudos de expansão decenal da geração e transmissão sob as táticas de descarbonização", "data_publicacao": "2026-02-15"}}
```

## # Citations

1. [Manual de Governança de Informações Não Estruturadas PowerupOKC] - Rege os padrões de indexação, controle e privacidade das bases de conhecimento setoriais.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
