---
id: DO-204
name: "Procedimentos de Rede do ONS"
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

# Procedimentos de Rede do ONS (DO-204)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança da base de conhecimento não estruturada **Procedimentos de Rede do ONS** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Regras, critérios, diretrizes e requisitos propostos pelo ONS e aprovados pela ANEEL que disciplinam a coordenação e o controle de instalações de geração e transmissão conectadas ao SIN.

Este objeto de dados não estruturado é de extrema importância para as regras de conformidade regulatória (conforme as diretrizes de regulação tarifária, fiscalização ou as instruções operacionais do SIN). Sua correta catalogação impede silos de conhecimento e vazamentos de informações classificadas.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade, linhagem e governança de dados no repositório corporativo da PowerUp, este Data Object mantém as seguintes conexões estáveis:

*   **Subdomínio de Dados (Nível 1):** Regulatório e Planejamento / Planejamento e Operação
*   **Sistemas e Aplicações Relacionadas (Applications):** Portal ONS, SharePoint de Operação e Manutenção (O&M), SCADA/EMS
*   **Repositório/Sistema de Registro Canônico (System of Truth):** Acervo Digital do ONS / MPO (Manual de Procedimentos da Operação)
*   **Capacidade de Negócio Relacionada:** Planejamento Operacional de Geração e Transmissão, Despacho Energético
*   **Documento de Referência (Mestre):** sim

## # Schema

Este ativo de dados não estruturados de referência é composto e regido pelos seguintes temas críticos e tipos de informações:

*   **Informações Críticas e Conteúdo Típico:** Critérios de projeto e requisitos mínimos para usinas e linhas (Mód. 2), sistemática de planejamento e estudos elétricos (Mód. 3), regras de programação (Mód. 4) e operação em tempo real (Mód. 5).
*   **Classificação de Privacidade e Sensibilidade (Compliance/LGPD):** Público

## # Examples

Abaixo está exemplificado um rascunho de metadados em formato estruturado representando o objeto documental, indicando as variáveis comumente contidas em seu fluxo de indexação:

```json
{"ons_submodulo_2_7": {"assunto": "Requisitos de Telecomunicações para Supervisão", "protocolo_sugerido": "IEC 60870-5-104 sobre TCP/IP"}}
```

## # Citations

1. [Manual de Governança de Informações Não Estruturadas PowerupOKC] - Rege os padrões de indexação, controle e privacidade das bases de conhecimento setoriais.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
