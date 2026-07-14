---
id: IND-009
name: "DRC - Duração Relativa da Transgressão de Tensão Crítica"
type: "Business Indicator"
subtype: "Performance Indicator"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
tags:
  - "Setor Elétrico"
  - "Indicador de Desempenho"
  - "Qualidade do Produto"
  - "LeanIX-v4"
---

# DRC - Duração Relativa da Transgressão de Tensão Crítica (ID: IND-009)

Este Fact Sheet descreve o indicador de desempenho **DRC** (Duração Relativa da Transgressão de Tensão Crítica) integrado ao catálogo mestre da **PowerUp OKC (Open Knowledge Catalog)**. Ele atua como uma métrica de controle de governança em total conformidade com as diretrizes do metamodelo v4 da **SAP LeanIX**.

## 1. Descrição Geral e Metodologia de Medição
Percentual de tempo em que a tensão de regime permanente esteve na faixa crítica estabelecida no Módulo 8 do PRODIST, resultando em severas compensações financeiras regulatórias se violada.

A medição sistemática deste indicador é crucial para avaliar a eficiência operativa e conformidade setorial. A sua consolidação permite identificar perdas de receita, ineficiências em ativos físicos, transgressões de limites de infraestrutura e riscos de sanções regulatórias.

## 2. Limites e Padrões Regulatórios
*   **Limite Vigente:** `DRCLimite: 0.5%`
*   **Regulador / Framework Principal:** ANEEL (PRODIST Módulo 8)
*   **Unidade de Medida:** `%`

O não atendimento aos limites acordados gera penalidades administrativas, compensações diretas em fatura aos consumidores afetados, cortes de RAP (Receita Anual Permitida) na transmissão, ou reduções de garantias fiscais na geração.

## 3. Relações no Metamodelo SAP LeanIX v4
Para garantir a rastreabilidade de ponta a ponta e a visibilidade de dependências operacionais, o indicador mantém as seguintes associações:

*   **Business Capability Medida (Nível 3):** [/cap-l3-gestao-de-perdas](Gestão de Perdas)
*   **System of Truth / Application de Suporte:** [MDM (Meter Data Management)](/business-applications/app-mdm-gestao-medicao.md)
*   **Organização / Time Proprietário (Who):** [Departamento de Faturamento / Engenharia de Medição](/organizations/teams/org-departamento-faturamento.md)
*   **Data Object de Entrada (What):** [Leitura de Medição](/data-objects/do-145-leitura-de-medicao.md)

## 4. Diretrizes de Governança e Metodologia TIME
Este indicador é fundamental para a tomada de decisão estratégica de investimentos de tecnologia conforme o TIME Framework (Tolerate, Invest, Migrate, Eliminate):

*   **Invest (Investir):** Desvios recorrentes e violações de limites deste indicador disparam a priorização de orçamentos para inovação e modernização analítica (ex: inteligência artificial para previsão e automação de manobras) nos sistemas SOT de suporte.
*   **Migrate (Migrar):** Caso as bases de dados ou sistemas transacionais fiquem lentos na consolidação deste KPI, planeja-se a migração das infraestruturas legadas on-premises correspondentes para nuvem.
