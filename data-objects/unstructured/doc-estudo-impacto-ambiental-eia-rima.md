---
id: DO-222
name: "Estudo de Impacto Ambiental (EIA) e Relatório (RIMA)"
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

# Estudo de Impacto Ambiental (EIA) e Relatório (RIMA) (DO-222)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança da base de conhecimento não estruturada **Estudo de Impacto Ambiental (EIA) e Relatório (RIMA)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Estudos e relatórios de conformidade sócio-ambiental de altíssima densidade, necessários para a obtenção de licenças prévias, de instalação e operação de novas usinas e linhas de transmissão.

Este objeto de dados não estruturado é de extrema importância para as regras de conformidade regulatória (conforme as diretrizes de regulação tarifária, fiscalização ou as instruções operacionais do SIN). Sua correta catalogação impede silos de conhecimento e vazamentos de informações classificadas.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade, linhagem e governança de dados no repositório corporativo da PowerUp, este Data Object mantém as seguintes conexões estáveis:

*   **Subdomínio de Dados (Nível 1):** Jurídico e Contratual / Licenciamento Ambiental
*   **Sistemas e Aplicações Relacionadas (Applications):** Órgãos Ambientais (IBAMA / Estaduais), GED Ambiental, PMO (Projetos)
*   **Repositório/Sistema de Registro Canônico (System of Truth):** Repositório de Sustentabilidade e Engenharia Sócio-Ambiental
*   **Capacidade de Negócio Relacionada:** Desenvolvimento de Engenharia de Projetos de Expansão, Licenciamento Ambiental
*   **Documento de Referência (Mestre):** sim

## # Schema

Este ativo de dados não estruturados de referência é composto e regido pelos seguintes temas críticos e tipos de informações:

*   **Informações Críticas e Conteúdo Típico:** Diagnóstico ambiental da área de influência (fauna, flora, hidrologia), avaliação de impactos potenciais (assoreamento, ruído), medidas mitigadoras e plano de monitoramento ambiental.
*   **Classificação de Privacidade e Sensibilidade (Compliance/LGPD):** Interno

## # Examples

Abaixo está exemplificado um rascunho de metadados em formato estruturado representando o objeto documental, indicando as variáveis comumente contidas em seu fluxo de indexação:

```json
{"eia_rima_solar_parque": {"parque_id": "UFV-SOLAR-OESTE-150MW", "licenca_ambiental_prioritaria": "LP-2026-015", "medidas_mitigadoras_obrigatorias": ["Recomposição florestal de reserva permanente", "Resgate de fauna terrestre antes de supressão vegetal"]}}
```

## # Citations

1. [Manual de Governança de Informações Não Estruturadas PowerupOKC] - Rege os padrões de indexação, controle e privacidade das bases de conhecimento setoriais.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
