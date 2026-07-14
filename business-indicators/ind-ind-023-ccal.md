---
id: IND-023
name: "CCAL - Controle de Carregamento de LTs"
type: "Business Indicator"
subtype: "Performance Indicator"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
tags:
  - "Setor Elétrico"
  - "Indicador de Desempenho"
  - "Confiabilidade de Transmissão"
  - "LeanIX-v4"
---

# CCAL - Controle de Carregamento de LTs (ID: IND-023)

Este Fact Sheet descreve o indicador de desempenho **CCAL** (Controle de Carregamento de LTs) integrado ao catálogo mestre da **PowerUp OKC (Open Knowledge Catalog)**. Ele atua como uma métrica de controle de governança em total conformidade com as diretrizes do metamodelo v4 da **SAP LeanIX**.

## 1. Descrição Geral e Metodologia de Medição
Monitoramento em tempo real do nível de carregamento e corrente elétrica das LTs para evitar que se ultrapasse os limites térmicos de segurança física dos condutores metálicos.

A medição sistemática deste indicador é crucial para avaliar a eficiência operativa e conformidade setorial. A sua consolidação permite identificar perdas de receita, ineficiências em ativos físicos, transgressões de limites de infraestrutura e riscos de sanções regulatórias.

## 2. Limites e Padrões Regulatórios
*   **Limite Vigente:** `Ampacidade física máxima do condutor`
*   **Regulador / Framework Principal:** ONS (Procedimentos de Rede)
*   **Unidade de Medida:** `% ou Amperes`

O não atendimento aos limites acordados gera penalidades administrativas, compensações diretas em fatura aos consumidores afetados, cortes de RAP (Receita Anual Permitida) na transmissão, ou reduções de garantias fiscais na geração.

## 3. Relações no Metamodelo SAP LeanIX v4
Para garantir a rastreabilidade de ponta a ponta e a visibilidade de dependências operacionais, o indicador mantém as seguintes associações:

*   **Business Capability Medida (Nível 3):** [/cap-l3-operacao-do-sistema-de-transmissao](Operação do Sistema de Transmissão)
*   **System of Truth / Application de Suporte:** [EMS (Energy Management System)](/business-applications/app-etrm-gestao-trading-comercializacao.md)
*   **Organização / Time Proprietário (Who):** [Centro de Operações da Transmissão (COT)](/organizations/teams/org-cot.md)
*   **Data Object de Entrada (What):** [Linha de Transmissão (LT)](/data-objects/do-117-linha-de-transmissao-lt.md)

## 4. Diretrizes de Governança e Metodologia TIME
Este indicador é fundamental para a tomada de decisão estratégica de investimentos de tecnologia conforme o TIME Framework (Tolerate, Invest, Migrate, Eliminate):

*   **Invest (Investir):** Desvios recorrentes e violações de limites deste indicador disparam a priorização de orçamentos para inovação e modernização analítica (ex: inteligência artificial para previsão e automação de manobras) nos sistemas SOT de suporte.
*   **Migrate (Migrar):** Caso as bases de dados ou sistemas transacionais fiquem lentos na consolidação deste KPI, planeja-se a migração das infraestruturas legadas on-premises correspondentes para nuvem.
