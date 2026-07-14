---
id: IND-017
name: "Perdas - Percentual de Perdas Não Técnicas"
type: "Business Indicator"
subtype: "Performance Indicator"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
tags:
  - "Setor Elétrico"
  - "Indicador de Desempenho"
  - "Distribuição / Comercial"
  - "LeanIX-v4"
---

# Perdas - Percentual de Perdas Não Técnicas (ID: IND-017)

Este Fact Sheet descreve o indicador de desempenho **Perdas** (Percentual de Perdas Não Técnicas) integrado ao catálogo mestre da **PowerUp OKC (Open Knowledge Catalog)**. Ele atua como uma métrica de controle de governança em total conformidade com as diretrizes do metamodelo v4 da **SAP LeanIX**.

## 1. Descrição Geral e Metodologia de Medição
Mapeia os volumes de perdas não técnicas elétricas (furtos de energia, desvios e erros de medição) calculados a partir do balanço entre a energia injetada na rede e o faturamento real.

A medição sistemática deste indicador é crucial para avaliar a eficiência operativa e conformidade setorial. A sua consolidação permite identificar perdas de receita, ineficiências em ativos físicos, transgressões de limites de infraestrutura e riscos de sanções regulatórias.

## 2. Limites e Padrões Regulatórios
*   **Limite Vigente:** `Limite regulatório definido pela ANEEL`
*   **Regulador / Framework Principal:** ANEEL (PRODIST Módulo 7)
*   **Unidade de Medida:** `%`

O não atendimento aos limites acordados gera penalidades administrativas, compensações diretas em fatura aos consumidores afetados, cortes de RAP (Receita Anual Permitida) na transmissão, ou reduções de garantias fiscais na geração.

## 3. Relações no Metamodelo SAP LeanIX v4
Para garantir a rastreabilidade de ponta a ponta e a visibilidade de dependências operacionais, o indicador mantém as seguintes associações:

*   **Business Capability Medida (Nível 3):** [/cap-l3-gestao-de-perdas](Gestão de Perdas)
*   **System of Truth / Application de Suporte:** [MDM (Meter Data Management)](/business-applications/app-mdm-gestao-medicao.md)
*   **Organização / Time Proprietário (Who):** [Departamento de Faturamento](/organizations/teams/org-departamento-faturamento.md)
*   **Data Object de Entrada (What):** [Balanço de Energia](/data-objects/do-103-balanco-de-energia.md)

## 4. Diretrizes de Governança e Metodologia TIME
Este indicador é fundamental para a tomada de decisão estratégica de investimentos de tecnologia conforme o TIME Framework (Tolerate, Invest, Migrate, Eliminate):

*   **Invest (Investir):** Desvios recorrentes e violações de limites deste indicador disparam a priorização de orçamentos para inovação e modernização analítica (ex: inteligência artificial para previsão e automação de manobras) nos sistemas SOT de suporte.
*   **Migrate (Migrar):** Caso as bases de dados ou sistemas transacionais fiquem lentos na consolidação deste KPI, planeja-se a migração das infraestruturas legadas on-premises correspondentes para nuvem.
