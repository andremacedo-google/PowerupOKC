---
id: DO-223
name: "Roteiros (Scripts) de Atendimento e FAQ de Clientes"
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

# Roteiros (Scripts) de Atendimento e FAQ de Clientes (DO-223)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança da base de conhecimento não estruturada **Roteiros (Scripts) de Atendimento e FAQ de Clientes** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Roteiros e guias estruturados que auxiliam os agentes de atendimento (call center, digital, chat) a responderem a dúvidas comerciais e abrirem ordens de serviço.

Este objeto de dados não estruturado é de extrema importância para as regras de conformidade regulatória (conforme as diretrizes de regulação tarifária, fiscalização ou as instruções operacionais do SIN). Sua correta catalogação impede silos de conhecimento e vazamentos de informações classificadas.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade, linhagem e governança de dados no repositório corporativo da PowerUp, este Data Object mantém as seguintes conexões estáveis:

*   **Subdomínio de Dados (Nível 1):** Relacionamento com Cliente / Atendimento
*   **Sistemas e Aplicações Relacionadas (Applications):** Salesforce CRM (Knowledge), Base de Conhecimento do Call Center
*   **Repositório/Sistema de Registro Canônico (System of Truth):** CRM / Central de Relacionamento de Clientes
*   **Capacidade de Negócio Relacionada:** Atendimento ao Cliente Multicanal, Gestão de Reclamações, Ouvidoria
*   **Documento de Referência (Mestre):** sim

## # Schema

Este ativo de dados não estruturados de referência é composto e regido pelos seguintes temas críticos e tipos de informações:

*   **Informações Críticas e Conteúdo Típico:** Árvore de decisão para tipificação (falta de energia, conta alta), scripts obrigatórios por regulação (REN ANEEL 1.000), orientações de prazos para novos serviços e checklists de segurança.
*   **Classificação de Privacidade e Sensibilidade (Compliance/LGPD):** Interno

## # Examples

Abaixo está exemplificado um rascunho de metadados em formato estruturado representando o objeto documental, indicando as variáveis comumente contidas em seu fluxo de indexação:

```json
{"script_faturamento_alto": {"tipificacao": "Reclamação de Consumo Excessivo", "procedimento_SLA": "Abertura de chamado de verificação para medidor de campo (SLA: 5 dias úteis)", "scripts": ["Verificar primeiro se há alteração recente no número de eletrodomésticos", "Oferecer opções de parcelamento amigável"]}}
```

## # Citations

1. [Manual de Governança de Informações Não Estruturadas PowerupOKC] - Rege os padrões de indexação, controle e privacidade das bases de conhecimento setoriais.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
