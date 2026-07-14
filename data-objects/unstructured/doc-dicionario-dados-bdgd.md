---
id: DO-218
name: "Dicionário de Dados da ANEEL (DDA) para a BDGD"
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

# Dicionário de Dados da ANEEL (DDA) para a BDGD (DO-218)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança da base de conhecimento não estruturada **Dicionário de Dados da ANEEL (DDA) para a BDGD** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Guia técnico expedido pela ANEEL que padroniza os atributos, tabelas e codificações para envio das bases de dados georreferenciadas das distribuidoras de energia (BDGD).

Este objeto de dados não estruturado é de extrema importância para as regras de conformidade regulatória (conforme as diretrizes de regulação tarifária, fiscalização ou as instruções operacionais do SIN). Sua correta catalogação impede silos de conhecimento e vazamentos de informações classificadas.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade, linhagem e governança de dados no repositório corporativo da PowerUp, este Data Object mantém as seguintes conexões estáveis:

*   **Subdomínio de Dados (Nível 1):** Técnico e Operacional / TI / TO
*   **Sistemas e Aplicações Relacionadas (Applications):** GIS, Portal ANEEL (PRODIST Mód. 10), GED Regulatório
*   **Repositório/Sistema de Registro Canônico (System of Truth):** Sistema de Informação Geográfica Regulatório (SIG-R) da ANEEL
*   **Capacidade de Negócio Relacionada:** Planejamento e Expansão da Distribuição, Gestão de Dados da Rede, Envio Regulatório de Redes
*   **Documento de Referência (Mestre):** sim

## # Schema

Este ativo de dados não estruturados de referência é composto e regido pelos seguintes temas críticos e tipos de informações:

*   **Informações Críticas e Conteúdo Típico:** Estrutura das classes de feição (SED, CMT, SMT, PE), códigos para material de poste e condutor, tipos de fiação, e relações topológicas de conectividade de rede para modelagem no GIS.
*   **Classificação de Privacidade e Sensibilidade (Compliance/LGPD):** Público

## # Examples

Abaixo está exemplificado um rascunho de metadados em formato estruturado representando o objeto documental, indicando as variáveis comumente contidas em seu fluxo de indexação:

```json
{"bdgd_dicionario_atributos": {"classe": "UNTRMT (Unidade Transformadora de MT)", "atributos_obrigatorios": ["COD_ID", "DIST", "POT_NOM", "PER_FER", "SUB", "CONJ", "DAT_IMO"]}}
```

## # Citations

1. [Manual de Governança de Informações Não Estruturadas PowerupOKC] - Rege os padrões de indexação, controle e privacidade das bases de conhecimento setoriais.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
