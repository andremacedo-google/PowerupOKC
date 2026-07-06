---
id: AP-010
name: "GIS - Sistema de Informação Geográfica de Redes"
type: "Application"
subtype: "Business Application"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
businessCriticality: "Mission Critical"
functionalSuitability: "Excellent"
technicalSuitability: "Excellent"
tags:
  - "Setor Elétrico"
  - "Operações"
  - "Distribuição"
  - "Geográfico"
  - "LeanIX-v4"
---

# GIS - Sistema de Informação Geográfica de Redes (ID: AP-010)

O sistema de **Geographic Information System (GIS)** gerencia e exibe a modelagem cadastral georreferenciada e a topologia física espacial de todos os ativos fixos da concessionária de energia.

## 1. Escopo Técnico e de Negócio
O GIS é o cadastro geográfico único da verdade que mapeia a localização espacial e as conectividades elétricas de postes, transformadores, cabos, ramais de ligação e subestações do setor de distribuição elétrico brasileiro [411]. Ele apoia o planejamento da expansão de rede e serve de base para o envio de relatórios regulatórios cadastrais exigidos pela ANEEL, além de subsidiar as equipes de campo na localização física de equipamentos para manutenção [405].

## 2. Integrações e Fluxo de Dados (Data Objects)
*   **Inputs (Dados de Entrada):**
    *   `DO-002 Cadastro de Rede (GIS)`: Dados coletados em vistorias físicas de obras ou levantamentos espaciais.
*   **Outputs (Dados de Saída):**
    *   `DO-002 Cadastro de Rede (GIS)`: Exportação do modelo topológico de rede geográfica que alimenta síncronamente o motor de topologia do ADMS e do sistema de planejamento de expansão [411].

## 3. Capacidades de Negócio Suportadas
*   `cap-l3-gestao-de-dados-da-rede` [338]
*   `cap-l3-planejamento-da-expansao-da-rede` [338]

## 4. Exemplos de Soluções e Tecnologias de Mercado
*   **Esri ArcGIS Utility Network**: Padrão líder absoluto para a modelagem complexa georreferenciada de redes inteligentes e ativos elétricos espaciais.
*   **GE Smallworld GIS**: Plataforma corporativa robusta amplamente adotada em grandes empresas de utilities de energia.

## 5. Práticas de Governança e FinOps
*   Como base geográfica de alta precisão, o GIS exige auditorias constantes de consistência topológica (connectivity audit) para impedir anomalias de conexões cadastrais elétricas que possam gerar acidentes físicos de campo.
