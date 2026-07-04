---
id: BC-ENGAJAMENTO-CLIENTE
name: "Engajamento com o Cliente"
type: "Business Capability"
subtype: "Level 1"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
strategicImportance: "tier2"
maturity: "Level 3 - Defined"
tags:
  - "Setor Elétrico"
  - "Cliente"
  - "Comercialização"
  - "Mercado Livre"
  - "Prossumidor"
  - "LeanIX-v4"
---

# Especificação Técnica: Engajamento com o Cliente (ID: BC-ENGAJAMENTO-CLIENTE)

Esta capacidade representa a interface de atração, conversão, faturamento, relacionamento e autoatendimento entre a concessionária de utilidade pública e seus consumidores em múltiplos mercados (cativos regulados - ACR, consumidores livres de energia - ACL e prossumidores de geração distribuída). Ela é responsável pela fidelidade de marca, experiência digital omnichannel e a viabilização de novas réguas de relacionamento na transição energética.

## 1. Sub-capacidades de Nível 2 e Atividades de Nível 3 Associadas
De acordo com o Mapa de Capacidades do Setor de Energia, as frentes de relacionamento dividem-se em:

*   **Marketing e Desenvolvimento de Novos Negócios:**
    *   *Análise de Mercado:* Estuda as tendências setoriais (transição de portfólios, tarifas dinâmicas, mobilidade elétrica) e comportamento concorrencial.
    *   *Desenvolvimento de Produtos e Serviços:* Desenha novos produtos energéticos, pacotes agregados de serviços (Energy as a Service) e planos de fidelização.
    *   *Marketing Digital:* Executa estratégias em mídias online para geração de leads qualificados no mercado livre de energia.
*   **Vendas e Aquisição de Clientes:**
    *   *Gestão de Leads e Oportunidades:* Conduz a qualificação de potenciais compradores corporativos (B2B) através de inteligência analítica e funil comercial.
    *   *Contratação de Serviços:* Formaliza contratos bilaterais de compra e venda de energia no Ambiente de Contratação Livre (ACL).
    *   *Onboarding de Clientes:* Simplifica, acelera e digitaliza a entrada de novos usuários na carteira da empresa.
*   **Gestão do Relacionamento com o Cliente:**
    *   *Atendimento ao Cliente Multicanal:* Fornece suporte integrado de canais síncronos de atendimento de alta resolutividade (portais, apps, agentes virtuais).
    *   *Gestão de Reclamações:* Triagem e resolução ágil de intercorrências físicas ou financeiras da rede.
    *   *Programas de Fidelidade:* Cria incentivos e réguas de engajamento para retenção e fidelização em mercados competitivos.
*   **Faturamento e Cobrança:**
    *   *Medição e Coleta de Dados:* Gerencia o fluxo de coleta de dados de medidores convencionais e inteligentes (AMI) na borda da rede.
    *   *Processamento de Faturas:* Executa cálculos complexos de faturamento cobrindo múltiplos perfis horários (Tarifa Branca) e regras de compensação para geração distribuída (Net Metering).
    *   *Gestão de Inadimplência:* Estrutura réguas de cobrança automatizadas com base no score de risco do cliente.

## 2. Relações no Metamodelo LeanIX (Fact Sheets Relacionados)
*   **Supports (Apoia):** Objetivos de aumento de receita no varejo elétrico, redução de custos de atendimento telefônico reativo, e diminuição de churn corporativo.
*   **Supported by (Suportado por):** Sistemas de CRM (Salesforce Service/Sales), CIS (Customer Information System), plataformas unificadas de faturamento e canais de autoatendimento cognitivo (Gemini Enterprise for Customer Experience).
*   **Data Objects (Objetos de Dados) Associados:** Faturas de Consumo, Perfis de Medição AMI, Propostas de Contratos ACL, Leads Qualificados, e Registros de Reclamações de Ouvidoria.

## 3. Avaliação de Maturidade e Importância Estratégica (Heatmap)
*   **Importância Estratégica:** `tier2` (Differentiation). Com a aceleração da abertura do mercado de energia livre (ACL) de média e baixa tensão e a jornada do prossumidor, esta capacidade tornou-se vital para diferenciar a empresa frente aos novos entrantes (comercializadoras digitais).
*   **Maturidade Atual:** `Level 3 - Defined` (Sistemas de atendimento e faturamento padronizados, mas ainda em fase de migração para modelos totalmente ágeis e omnichannel baseados em dados ricos em tempo real).
*   **Diretriz de Investimentos em TI:** **Investir e Transformar**. O foco do roadmap de tecnologia de relacionamento deve ser a transformação estrutural dos canais. Os investimentos prioritários incluem a implantação de plataformas modernas de CX, integração de BigQuery com medidores inteligentes (AMI) para predição de faturamento e ofertas personalizadas, além do uso de agentes de IA Generativa para atuar de forma consultiva e proativa na venda de novos serviços.
