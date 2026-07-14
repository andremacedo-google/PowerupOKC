---
id: DO-210
name: "Estatuto Social e Regimentos Internos"
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

# Estatuto Social e Regimentos Internos (DO-210)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança da base de conhecimento não estruturada **Estatuto Social e Regimentos Internos** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Documentos de governança corporativa de primeiro nível que estabelecem as regras de funcionamento da empresa, conselhos e comitês estatutários.

Este objeto de dados não estruturado é de extrema importância para as regras de conformidade regulatória (conforme as diretrizes de regulação tarifária, fiscalização ou as instruções operacionais do SIN). Sua correta catalogação impede silos de conhecimento e vazamentos de informações classificadas.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade, linhagem e governança de dados no repositório corporativo da PowerUp, este Data Object mantém as seguintes conexões estáveis:

*   **Subdomínio de Dados (Nível 1):** Corporativo e Governança / Governança Interna
*   **Sistemas e Aplicações Relacionadas (Applications):** Portal de Governança, SharePoint Jurídico e Compliance, GED de Governança
*   **Repositório/Sistema de Registro Canônico (System of Truth):** Junta Comercial do Estado / Secretaria Geral de Governança
*   **Capacidade de Negócio Relacionada:** Tomada de Decisão Estratégica, Compliance e Governança de Acionistas
*   **Documento de Referência (Mestre):** sim

## # Schema

Este ativo de dados não estruturados de referência é composto e regido pelos seguintes temas críticos e tipos de informações:

*   **Informações Críticas e Conteúdo Típico:** Composição e competência do Conselho de Administração e Diretoria, limites para decisões de investimentos (CAPEX) e endividamento, política de gestão de riscos (ERM), ética e compliance.
*   **Classificação de Privacidade e Sensibilidade (Compliance/LGPD):** Interno

## # Examples

Abaixo está exemplificado um rascunho de metadados em formato estruturado representando o objeto documental, indicando as variáveis comumente contidas em seu fluxo de indexação:

```json
{"estatuto_artigo_24": {"conselho_administracao": "Compete aprovar a aquisição de equipamentos pesados ou investimentos CAPEX que excedam R$ 10.000.000"}}
```

## # Citations

1. [Manual de Governança de Informações Não Estruturadas PowerupOKC] - Rege os padrões de indexação, controle e privacidade das bases de conhecimento setoriais.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
