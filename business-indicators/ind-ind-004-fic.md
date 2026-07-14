---
id: IND-004
name: "FIC - Frequência de Interrupção Individual por Unidade Consumidora"
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

# FIC - Frequência de Interrupção Individual por Unidade Consumidora (ID: IND-004)

Este Fact Sheet descreve o indicador de desempenho **FIC** (Frequência de Interrupção Individual por Unidade Consumidora) integrado ao catálogo mestre da **PowerUp OKC (Open Knowledge Catalog)**. Ele atua como uma métrica de controle de governança em total conformidade com as diretrizes do metamodelo v4 da **SAP LeanIX**.

## 1. Descrição Geral e Metodologia de Medição
Mede a quantidade total de interrupções de longa duração ocorridas e sofridas individualmente por uma unidade consumidora específica no mês civil.

A medição sistemática deste indicador é crucial para avaliar a eficiência operativa e conformidade setorial. A sua consolidação permite identificar perdas de receita, ineficiências em ativos físicos, transgressões de limites de infraestrutura e riscos de sanções regulatórias.

## 2. Limites e Padrões Regulatórios
*   **Limite Vigente:** `Varia por classe de consumo (Tabelas do Anexo 8.B do PRODIST)`
*   **Regulador / Framework Principal:** ANEEL (PRODIST Módulo 8)
*   **Unidade de Medida:** `Interrupções`

O não atendimento aos limites acordados gera penalidades administrativas, compensações diretas em fatura aos consumidores afetados, cortes de RAP (Receita Anual Permitida) na transmissão, ou reduções de garantias fiscais na geração.

## 3. Relações no Metamodelo SAP LeanIX v4
Para garantir a rastreabilidade de ponta a ponta e a visibilidade de dependências operacionais, o indicador mantém as seguintes associações:

*   **Business Capability Medida (Nível 3):** [/cap-l3-processamento-de-faturas](Processamento de Faturas)
*   **System of Truth / Application de Suporte:** [CIS / Billing (SAP IS-U)](/business-applications/app-cis-faturamento-comercial.md)
*   **Organização / Time Proprietário (Who):** [Departamento de Faturamento / Atendimento](/organizations/teams/org-departamento-faturamento.md)
*   **Data Object de Entrada (What):** [Fatura (Conta de Energia)](/data-objects/do-144-fatura-conta-de-energia.md)

## 4. Diretrizes de Governança e Metodologia TIME
Este indicador é fundamental para a tomada de decisão estratégica de investimentos de tecnologia conforme o TIME Framework (Tolerate, Invest, Migrate, Eliminate):

*   **Invest (Investir):** Desvios recorrentes e violações de limites deste indicador disparam a priorização de orçamentos para inovação e modernização analítica (ex: inteligência artificial para previsão e automação de manobras) nos sistemas SOT de suporte.
*   **Migrate (Migrar):** Caso as bases de dados ou sistemas transacionais fiquem lentos na consolidação deste KPI, planeja-se a migração das infraestruturas legadas on-premises correspondentes para nuvem.
