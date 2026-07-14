---
id: IND-012
name: "FER - Frequência Equivalente de Reclamação por 1.000 UCs"
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

# FER - Frequência Equivalente de Reclamação por 1.000 UCs (ID: IND-012)

Este Fact Sheet descreve o indicador de desempenho **FER** (Frequência Equivalente de Reclamação por 1.000 UCs) integrado ao catálogo mestre da **PowerUp OKC (Open Knowledge Catalog)**. Ele atua como uma métrica de controle de governança em total conformidade com as diretrizes do metamodelo v4 da **SAP LeanIX**.

## 1. Descrição Geral e Metodologia de Medição
Frequência com que são registradas reclamações procedentes de usuários a cada 1.000 unidades consumidoras faturadas ao longo de uma base anual de acompanhamento.

A medição sistemática deste indicador é crucial para avaliar a eficiência operativa e conformidade setorial. A sua consolidação permite identificar perdas de receita, ineficiências em ativos físicos, transgressões de limites de infraestrutura e riscos de sanções regulatórias.

## 2. Limites e Padrões Regulatórios
*   **Limite Vigente:** `Definido por grupo de distribuidoras pela ANEEL`
*   **Regulador / Framework Principal:** ANEEL (Qualidade Comercial)
*   **Unidade de Medida:** `Reclamações / 1.000 UCs`

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
