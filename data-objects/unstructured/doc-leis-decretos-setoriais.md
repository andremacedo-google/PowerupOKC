---
id: DO-201
name: "Leis e Decretos Setoriais (Concessões, Comercialização)"
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

# Leis e Decretos Setoriais (Concessões, Comercialização) (DO-201)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança da base de conhecimento não estruturada **Leis e Decretos Setoriais (Concessões, Comercialização)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Conjunto de leis federais e decretos que definem o regime jurídico do setor de energia elétrica, incluindo as diretrizes de outorga, divisão de mercados, concessão pública e o marco legal da GD.

Este objeto de dados não estruturado é de extrema importância para as regras de conformidade regulatória (conforme as diretrizes de regulação tarifária, fiscalização ou as instruções operacionais do SIN). Sua correta catalogação impede silos de conhecimento e vazamentos de informações classificadas.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade, linhagem e governança de dados no repositório corporativo da PowerUp, este Data Object mantém as seguintes conexões estáveis:

*   **Subdomínio de Dados (Nível 1):** Regulatório e Planejamento / Arcabouço Legal
*   **Sistemas e Aplicações Relacionadas (Applications):** Portal da Legislação (Planalto), GED de Regulação, SharePoint Jurídico
*   **Repositório/Sistema de Registro Canônico (System of Truth):** Diário Oficial da União (DOU) / Biblioteca da ANEEL
*   **Capacidade de Negócio Relacionada:** Conformidade Regulatória e Planejamento Estratégico de Longo Prazo do Grupo
*   **Documento de Referência (Mestre):** sim

## # Schema

Este ativo de dados não estruturados de referência é composto e regido pelos seguintes temas críticos e tipos de informações:

*   **Informações Críticas e Conteúdo Típico:** Diretrizes de outorga de serviços públicos, divisão setorial entre ACR e ACL (Lei 10.848), regras de modicidade tarifária, direitos dos consumidores de energia e incentivos para renováveis (Lei 14.300).
*   **Classificação de Privacidade e Sensibilidade (Compliance/LGPD):** Público

## # Examples

Abaixo está exemplificado um rascunho de metadados em formato estruturado representando o objeto documental, indicando as variáveis comumente contidas em seu fluxo de indexação:

```json
{"lei_14300": {"titulo": "Marco Legal da Micro e Minigeração Distribuída", "ano": 2022, "regra_transicao": "Regras de compensação de créditos e faturamento da TUSD Fio B para geração local"}, "lei_10848": {"titulo": "Divisão entre ACR e ACL", "ano": 2004}}
```

## # Citations

1. [Manual de Governança de Informações Não Estruturadas PowerupOKC] - Rege os padrões de indexação, controle e privacidade das bases de conhecimento setoriais.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
