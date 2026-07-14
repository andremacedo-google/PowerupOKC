---
id: IND-007
name: "DISE - Duração de Interrupção em Situação de Emergência"
type: "Business Indicator"
subtype: "Performance Indicator"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
tags:
  - "Setor Elétrico"
  - "Indicador de Desempenho"
  - "Qualidade do Serviço"
  - "LeanIX-v4"
---

# DISE - Duração de Interrupção em Situação de Emergência (ID: IND-007)

Este Fact Sheet descreve o indicador de desempenho **DISE** (Duração de Interrupção em Situação de Emergência) integrado ao catálogo mestre da **PowerUp OKC (Open Knowledge Catalog)**. Ele atua como uma métrica de controle de governança em total conformidade com as diretrizes do metamodelo v4 da **SAP LeanIX**.

## 1. Descrição Geral e Metodologia de Medição
Acompanha o tempo acumulado de interrupção ocorrida individualmente em que o consumidor final foi afetado por Situações de Emergência oficiais declaradas na rede operativa de distribuição.

A medição sistemática deste indicador é crucial para avaliar a eficiência operativa e conformidade setorial. A sua consolidação permite identificar perdas de receita, ineficiências em ativos físicos, transgressões de limites de infraestrutura e riscos de sanções regulatórias.

## 2. Limites e Padrões Regulatórios
*   **Limite Vigente:** `24 horas (Urbana) ou 48h (Não Urbana)`
*   **Regulador / Framework Principal:** ANEEL (PRODIST Módulo 8)
*   **Unidade de Medida:** `Horas`

O não atendimento aos limites acordados gera penalidades administrativas, compensações diretas em fatura aos consumidores afetados, cortes de RAP (Receita Anual Permitida) na transmissão, ou reduções de garantias fiscais na geração.

## 3. Relações no Metamodelo SAP LeanIX v4
Para garantir a rastreabilidade de ponta a ponta e a visibilidade de dependências operacionais, o indicador mantém as seguintes associações:

*   **Business Capability Medida (Nível 3):** [/cap-l3-operacao-da-rede-de-distribuicao](Operação da Rede de Distribuição)
*   **System of Truth / Application de Suporte:** [ADMS (OMS)](/business-applications/app-adms-gestao-redes-distribuicao.md)
*   **Organização / Time Proprietário (Who):** [COD (Centro de Operações da Distribuição)](/organizations/teams/org-cod.md)
*   **Data Object de Entrada (What):** [Evento de Interrupção (DEC/FEC)](/data-objects/do-105-evento-de-interrupcao-dec-fec.md)

## 4. Diretrizes de Governança e Metodologia TIME
Este indicador é fundamental para a tomada de decisão estratégica de investimentos de tecnologia conforme o TIME Framework (Tolerate, Invest, Migrate, Eliminate):

*   **Invest (Investir):** Desvios recorrentes e violações de limites deste indicador disparam a priorização de orçamentos para inovação e modernização analítica (ex: inteligência artificial para previsão e automação de manobras) nos sistemas SOT de suporte.
*   **Migrate (Migrar):** Caso as bases de dados ou sistemas transacionais fiquem lentos na consolidação deste KPI, planeja-se a migração das infraestruturas legadas on-premises correspondentes para nuvem.
