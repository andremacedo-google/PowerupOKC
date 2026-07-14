---
id: IND-010
name: "FD95 - Fator de Desequilíbrio de Tensão"
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

# FD95 - Fator de Desequilíbrio de Tensão (ID: IND-010)

Este Fact Sheet descreve o indicador de desempenho **FD95** (Fator de Desequilíbrio de Tensão) integrado ao catálogo mestre da **PowerUp OKC (Open Knowledge Catalog)**. Ele atua como uma métrica de controle de governança em total conformidade com as diretrizes do metamodelo v4 da **SAP LeanIX**.

## 1. Descrição Geral e Metodologia de Medição
Representa o desbalanceamento das amplitudes trifásicas superado em apenas 5% das leituras (95% do tempo o desequilíbrio é menor que o limite estabelecido).

A medição sistemática deste indicador é crucial para avaliar a eficiência operativa e conformidade setorial. A sua consolidação permite identificar perdas de receita, ineficiências em ativos físicos, transgressões de limites de infraestrutura e riscos de sanções regulatórias.

## 2. Limites e Padrões Regulatórios
*   **Limite Vigente:** `3.0% (Vn<=2.3kV) / 2.0% (>2.3kV)`
*   **Regulador / Framework Principal:** ANEEL (PRODIST Módulo 8)
*   **Unidade de Medida:** `%`

O não atendimento aos limites acordados gera penalidades administrativas, compensações diretas em fatura aos consumidores afetados, cortes de RAP (Receita Anual Permitida) na transmissão, ou reduções de garantias fiscais na geração.

## 3. Relações no Metamodelo SAP LeanIX v4
Para garantir a rastreabilidade de ponta a ponta e a visibilidade de dependências operacionais, o indicador mantém as seguintes associações:

*   **Business Capability Medida (Nível 3):** [/cap-l3-operacao-da-rede-de-distribuicao](Operação da Rede de Distribuição)
*   **System of Truth / Application de Suporte:** [ADMS (SCADA)](/business-applications/app-adms-gestao-redes-distribuicao.md)
*   **Organização / Time Proprietário (Who):** [COD (Centro de Operações da Distribuição)](/organizations/teams/org-cod.md)
*   **Data Object de Entrada (What):** [Modelo Topológico da Rede](/data-objects/do-102-modelo-topologico-da-rede.md)

## 4. Diretrizes de Governança e Metodologia TIME
Este indicador é fundamental para a tomada de decisão estratégica de investimentos de tecnologia conforme o TIME Framework (Tolerate, Invest, Migrate, Eliminate):

*   **Invest (Investir):** Desvios recorrentes e violações de limites deste indicador disparam a priorização de orçamentos para inovação e modernização analítica (ex: inteligência artificial para previsão e automação de manobras) nos sistemas SOT de suporte.
*   **Migrate (Migrar):** Caso as bases de dados ou sistemas transacionais fiquem lentos na consolidação deste KPI, planeja-se a migração das infraestruturas legadas on-premises correspondentes para nuvem.
