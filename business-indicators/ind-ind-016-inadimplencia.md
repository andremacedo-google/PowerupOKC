---
id: IND-016
name: "Inadimplencia - Inadimplência de Faturamento"
type: "Business Indicator"
subtype: "Performance Indicator"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
tags:
  - "Setor Elétrico"
  - "Indicador de Desempenho"
  - "Comercial / Financeiro"
  - "LeanIX-v4"
---

# Inadimplencia - Inadimplência de Faturamento (ID: IND-016)

Este Fact Sheet descreve o indicador de desempenho **Inadimplencia** (Inadimplência de Faturamento) integrado ao catálogo mestre da **PowerUp OKC (Open Knowledge Catalog)**. Ele atua como uma métrica de controle de governança em total conformidade com as diretrizes do metamodelo v4 da **SAP LeanIX**.

## 1. Descrição Geral e Metodologia de Medição
Acompanhamento do aging list (atrasos de faturamento de energia) de consumidores por classe tarifária e subgrupo de fornecimento em relação ao faturamento bruto total.

A medição sistemática deste indicador é crucial para avaliar a eficiência operativa e conformidade setorial. A sua consolidação permite identificar perdas de receita, ineficiências em ativos físicos, transgressões de limites de infraestrutura e riscos de sanções regulatórias.

## 2. Limites e Padrões Regulatórios
*   **Limite Vigente:** `Limite interno corporativo`
*   **Regulador / Framework Principal:** Processo de Arrecadação e Cobrança
*   **Unidade de Medida:** `%`

O não atendimento aos limites acordados gera penalidades administrativas, compensações diretas em fatura aos consumidores afetados, cortes de RAP (Receita Anual Permitida) na transmissão, ou reduções de garantias fiscais na geração.

## 3. Relações no Metamodelo SAP LeanIX v4
Para garantir a rastreabilidade de ponta a ponta e a visibilidade de dependências operacionais, o indicador mantém as seguintes associações:

*   **Business Capability Medida (Nível 3):** [/cap-l3-gestao-de-inadimplencia](Gestão de Inadimplência)
*   **System of Truth / Application de Suporte:** [CIS / FI-CA (SAP Utilities)](/business-applications/app-cis-faturamento-comercial.md)
*   **Organização / Time Proprietário (Who):** [Departamento de Faturamento](/organizations/teams/org-departamento-faturamento.md)
*   **Data Object de Entrada (What):** [Contas a Receber](/data-objects/do-157-contas-a-receber.md)

## 4. Diretrizes de Governança e Metodologia TIME
Este indicador é fundamental para a tomada de decisão estratégica de investimentos de tecnologia conforme o TIME Framework (Tolerate, Invest, Migrate, Eliminate):

*   **Invest (Investir):** Desvios recorrentes e violações de limites deste indicador disparam a priorização de orçamentos para inovação e modernização analítica (ex: inteligência artificial para previsão e automação de manobras) nos sistemas SOT de suporte.
*   **Migrate (Migrar):** Caso as bases de dados ou sistemas transacionais fiquem lentos na consolidação deste KPI, planeja-se a migração das infraestruturas legadas on-premises correspondentes para nuvem.
