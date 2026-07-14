---
id: IND-015
name: "DGC - Desempenho Global de Continuidade"
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

# DGC - Desempenho Global de Continuidade (ID: IND-015)

Este Fact Sheet descreve o indicador de desempenho **DGC** (Desempenho Global de Continuidade) integrado ao catálogo mestre da **PowerUp OKC (Open Knowledge Catalog)**. Ele atua como uma métrica de controle de governança em total conformidade com as diretrizes do metamodelo v4 da **SAP LeanIX**.

## 1. Descrição Geral e Metodologia de Medição
Indicador consolidado anual utilizado no Ranking de Continuidade das distribuidoras da ANEEL, que compara o DEC e FEC reais apurados contra os limites anuais estabelecidos.

A medição sistemática deste indicador é crucial para avaliar a eficiência operativa e conformidade setorial. A sua consolidação permite identificar perdas de receita, ineficiências em ativos físicos, transgressões de limites de infraestrutura e riscos de sanções regulatórias.

## 2. Limites e Padrões Regulatórios
*   **Limite Vigente:** `Menor ou igual a 1.0`
*   **Regulador / Framework Principal:** ANEEL (Ranking de Distribuidoras)
*   **Unidade de Medida:** `Índice`

O não atendimento aos limites acordados gera penalidades administrativas, compensações diretas em fatura aos consumidores afetados, cortes de RAP (Receita Anual Permitida) na transmissão, ou reduções de garantias fiscais na geração.

## 3. Relações no Metamodelo SAP LeanIX v4
Para garantir a rastreabilidade de ponta a ponta e a visibilidade de dependências operacionais, o indicador mantém as seguintes associações:

*   **Business Capability Medida (Nível 3):** [/cap-l3-conformidade-regulatoria](Conformidade Regulatória)
*   **System of Truth / Application de Suporte:** [BI / ERP Contábil-Regulatório](/business-applications/app-erp-gestao-financeira.md)
*   **Organização / Time Proprietário (Who):** [Regulação e Receita](/organizations/teams/org-tarifas-receita.md)
*   **Data Object de Entrada (What):** [Lançamento Contábil](/data-objects/do-160-lancamento-contabil.md)

## 4. Diretrizes de Governança e Metodologia TIME
Este indicador é fundamental para a tomada de decisão estratégica de investimentos de tecnologia conforme o TIME Framework (Tolerate, Invest, Migrate, Eliminate):

*   **Invest (Investir):** Desvios recorrentes e violações de limites deste indicador disparam a priorização de orçamentos para inovação e modernização analítica (ex: inteligência artificial para previsão e automação de manobras) nos sistemas SOT de suporte.
*   **Migrate (Migrar):** Caso as bases de dados ou sistemas transacionais fiquem lentos na consolidação deste KPI, planeja-se a migração das infraestruturas legadas on-premises correspondentes para nuvem.
