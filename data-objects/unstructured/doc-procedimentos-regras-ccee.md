---
id: DO-205
name: "Procedimentos e Regras de Comercialização da CCEE"
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

# Procedimentos e Regras de Comercialização da CCEE (DO-205)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança da base de conhecimento não estruturada **Procedimentos e Regras de Comercialização da CCEE** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Conjunto de módulos e cadernos normativos definidos pela CCEE que estabelecem as regras comerciais para faturamento e liquidação financeira das exposições no mercado spot.

Este objeto de dados não estruturado é de extrema importância para as regras de conformidade regulatória (conforme as diretrizes de regulação tarifária, fiscalização ou as instruções operacionais do SIN). Sua correta catalogação impede silos de conhecimento e vazamentos de informações classificadas.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade, linhagem e governança de dados no repositório corporativo da PowerUp, este Data Object mantém as seguintes conexões estáveis:

*   **Subdomínio de Dados (Nível 1):** Regulatório e Planejamento / Comercialização e Mercado
*   **Sistemas e Aplicações Relacionadas (Applications):** Portal CCEE, Sistema ETRM Interno, CliqCCEE, DRI
*   **Repositório/Sistema de Registro Canônico (System of Truth):** Acervo de Regras e Procedimentos de Comercialização da CCEE
*   **Capacidade de Negócio Relacionada:** Contabilização e Liquidação Financeira no Mercado de Curto Prazo (MCP)
*   **Documento de Referência (Mestre):** sim

## # Schema

Este ativo de dados não estruturados de referência é composto e regido pelos seguintes temas críticos e tipos de informações:

*   **Informações Críticas e Conteúdo Típico:** Diretrizes para o Módulo de Medição Física e Contábil, procedimentos de registro e validação de contratos bilaterais no ACL, regras de liquidação do mercado de curto prazo (MCP) e cálculo do PLD.
*   **Classificação de Privacidade e Sensibilidade (Compliance/LGPD):** Público

## # Examples

Abaixo está exemplificado um rascunho de metadados em formato estruturado representando o objeto documental, indicando as variáveis comumente contidas em seu fluxo de indexação:

```json
{"ccee_regras_comercializacao": {"modulo": "Medição Contábil", "dados_entrada": ["RAWCij", "RAWUGij"], "saida": "CONREC (Arquivos de Contabilização e Recontabilização)"}}
```

## # Citations

1. [Manual de Governança de Informações Não Estruturadas PowerupOKC] - Rege os padrões de indexação, controle e privacidade das bases de conhecimento setoriais.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
