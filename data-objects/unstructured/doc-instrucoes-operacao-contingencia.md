---
id: DO-215
name: "Instruções de Operação (IO) e Planos de Contingência"
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

# Instruções de Operação (IO) e Planos de Contingência (DO-215)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança da base de conhecimento não estruturada **Instruções de Operação (IO) e Planos de Contingência** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Guias operacionais específicos que estabelecem os passo a passos para manobras normais e de emergência, bem como planos de resposta rápida para grandes eventos como tempestades ou quebras físicas.

Este objeto de dados não estruturado é de extrema importância para as regras de conformidade regulatória (conforme as diretrizes de regulação tarifária, fiscalização ou as instruções operacionais do SIN). Sua correta catalogação impede silos de conhecimento e vazamentos de informações classificadas.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade, linhagem e governança de dados no repositório corporativo da PowerUp, este Data Object mantém as seguintes conexões estáveis:

*   **Subdomínio de Dados (Nível 1):** Técnico e Operacional / Operação do Sistema
*   **Sistemas e Aplicações Relacionadas (Applications):** ADMS (OMS), SCADA, WFM, GIS, ServiceNow (planos)
*   **Repositório/Sistema de Registro Canônico (System of Truth):** Central de Operações da Distribuição (COD) / GED de Operações
*   **Capacidade de Negócio Relacionada:** Operação do Sistema de Distribuição, Atendimento a Emergências e Restabelecimento
*   **Documento de Referência (Mestre):** sim

## # Schema

Este ativo de dados não estruturados de referência é composto e regido pelos seguintes temas críticos e tipos de informações:

*   **Informações Críticas e Conteúdo Típico:** Fluxos de manobras para isolar redes defeituosas (FLISR), planos de recomposição, tabelas de prioridade de corte de carga, diretrizes de segurança (NR-10) e de isolamento de redes sob contingência.
*   **Classificação de Privacidade e Sensibilidade (Compliance/LGPD):** Confidencial

## # Examples

Abaixo está exemplificado um rascunho de metadados em formato estruturado representando o objeto documental, indicando as variáveis comumente contidas em seu fluxo de indexação:

```json
{"io_emergencia_distribuicao": {"plano": "Restauração em contingência após vendaval", "prioridades_restabelecimento": ["Hospitais e Unidades de Saúde críticas", "Sistemas de captação de água e saneamento", "Consumidores comerciais de alta relevância (Grupo A)"]}}
```

## # Citations

1. [Manual de Governança de Informações Não Estruturadas PowerupOKC] - Rege os padrões de indexação, controle e privacidade das bases de conhecimento setoriais.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
