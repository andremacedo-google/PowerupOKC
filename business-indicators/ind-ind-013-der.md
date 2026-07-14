---
id: IND-013
name: "DER - Duração Equivalente de Reclamação"
type: "Business Indicator"
subtype: "Performance Indicator"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
tags:
  - "Setor Elétrico"
  - "Indicador de Desempenho"
  - "Qualidade Comercial"
  - "LeanIX-v4"
---

# DER - Duração Equivalente de Reclamação (ID: IND-013)

Este Fact Sheet descreve o indicador de desempenho **DER** (Duração Equivalente de Reclamação) integrado ao catálogo mestre da **PowerUp OKC (Open Knowledge Catalog)**. Ele atua como uma métrica de controle de governança em total conformidade com as diretrizes do metamodelo v4 da **SAP LeanIX**.

## 1. Descrição Geral e Metodologia de Medição
Mapeia o tempo médio ponderado necessário para que a distribuidora apresente a solução definitiva para as reclamações procedentes de clientes faturados.

A medição sistemática deste indicador é crucial para avaliar a eficiência operativa e conformidade setorial. A sua consolidação permite identificar perdas de receita, ineficiências em ativos físicos, transgressões de limites de infraestrutura e riscos de sanções regulatórias.

## 2. Limites e Padrões Regulatórios
*   **Limite Vigente:** `Parâmetro de monitoramento pela ANEEL`
*   **Regulador / Framework Principal:** ANEEL (Qualidade Comercial)
*   **Unidade de Medida:** `Horas`

O não atendimento aos limites acordados gera penalidades administrativas, compensações diretas em fatura aos consumidores afetados, cortes de RAP (Receita Anual Permitida) na transmissão, ou reduções de garantias fiscais na geração.

## 3. Relações no Metamodelo SAP LeanIX v4
Para garantir a rastreabilidade de ponta a ponta e a visibilidade de dependências operacionais, o indicador mantém as seguintes associações:

*   **Business Capability Medida (Nível 3):** [/cap-l3-gestao-de-reclamacoes](Gestão de Reclamações)
*   **System of Truth / Application de Suporte:** [CRM (Customer Relationship Management)](/business-applications/app-crm-relacionamento-cliente.md)
*   **Organização / Time Proprietário (Who):** [Atendimento e Relacionamento com Clientes](/organizations/teams/org-comunicacao-corporativa.md)
*   **Data Object de Entrada (What):** [Reclamação de Cliente](/data-objects/do-129-reclamacao-de-cliente.md)

## 4. Diretrizes de Governança e Metodologia TIME
Este indicador é fundamental para a tomada de decisão estratégica de investimentos de tecnologia conforme o TIME Framework (Tolerate, Invest, Migrate, Eliminate):

*   **Invest (Investir):** Desvios recorrentes e violações de limites deste indicador disparam a priorização de orçamentos para inovação e modernização analítica (ex: inteligência artificial para previsão e automação de manobras) nos sistemas SOT de suporte.
*   **Migrate (Migrar):** Caso as bases de dados ou sistemas transacionais fiquem lentos na consolidação deste KPI, planeja-se a migração das infraestruturas legadas on-premises correspondentes para nuvem.
