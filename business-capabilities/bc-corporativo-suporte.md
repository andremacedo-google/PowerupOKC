---
id: BC-CORP-SUPORTE
name: "Corporativo e Suporte ao Negócio"
type: "Business Capability"
subtype: "Level 1"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
strategicImportance: "parity"
maturity: "Level 4 - Managed"
tags:
  - "Setor Elétrico"
  - "Corporativo"
  - "Suporte"
  - "LeanIX-v4"
---

# Especificação Técnica: Corporativo e Suporte ao Negócio (ID: BC-CORP-SUPORTE)

Esta capacidade engloba todas as atividades administrativas, de governança e suporte necessárias para assegurar o funcionamento seguro, legal, financeiro e tecnológico da companhia elétrica. Ela atua como a infraestrutura de sustentação que permite que as operações finalísticas de energia (Geração, Transmissão e Distribuição) e o engajamento com o cliente ocorram de forma eficiente, em conformidade com as exigências regulatórias.

## 1. Sub-capacidades de Nível 2 e Atividades de Nível 3 Associadas
De acordo com o Mapa de Capacidades do Setor de Energia, as frentes de trabalho corporativas dividem-se em:

*   **Gestão Estratégica e Financeira:**
    *   *Planejamento Estratégico:* Define a visão de longo prazo, os objetivos e as iniciativas estratégicas da empresa para navegar na transição energética.
    *   *Gestão de Portfólio de Investimentos:* Analisa e gerencia o portfólio de investimentos em novos projetos, aquisições e modernização de ativos.
    *   *Contabilidade e Fechamento Financeiro:* Gerencia os registros contábeis, o fechamento fiscal e a elaboração de relatórios financeiros para stakeholders.
    *   *Gestão de Tesouraria:* Administra o fluxo de caixa, as relações com investidores e as estratégias de financiamento da companhia.
*   **Gestão de Pessoas e Cultura:**
    *   *Aquisição de Talentos:* Recruta e seleciona profissionais com as competências técnicas e comportamentais necessárias para a transformação do setor.
    *   *Desenvolvimento e Treinamento:* Implementa programas de capacitação para desenvolver as habilidades das equipes em novas tecnologias e modelos de negócio.
    *   *Remuneração e Benefícios:* Estrutura e gerencia os planos de remuneração, benefícios e incentivos para atrair e reter talentos.
    *   *Gestão da Experiência do Colaborador:* Fomenta o engajamento, bem-estar e cultura ágil organizacional.
*   **Gestão Jurídica e de Compliance:**
    *   *Gestão de Contratos:* Elabora, negocia e gerencia o ciclo de vida de contratos com fornecedores, parceiros e grandes clientes.
    *   *Conformidade Regulatória:* Garante que todas as operações da empresa estejam em conformidade com as normas da ANEEL, ONS, CCEE e demais agências reguladoras.
    *   *Gestão de Risco Corporativo:* Consolida inventários de riscos estratégicos, operacionais e regulatórios, desenvolvendo planos de resiliência e continuidade.
*   **Gestão de Tecnologia da Informação:**
    *   *Arquitetura de TI e de Dados:* Define e padroniza as topologias sistêmicas, governança de dados (Data Mesh) e infraestrutura de nuvem.
    *   *Segurança Cibernética (TI/OT):* Protege os sistemas corporativos e industriais contra ameaças digitais na convergência física/digital.
    *   *Gestão de Infraestrutura e Operações de TI:* Gerencia os recursos de processamento local, nuvem e conectividade da companhia.
*   **Gestão da Cadeia de Suprimentos:**
    *   *Gestão de Fornecedores:* Qualifica, seleciona e avalia a conformidade operacional e ESG dos parceiros comerciais.
    *   *Compras Estratégicas (Procurement):* Executa o processo de compra de bens e serviços de alta complexidade (Sourcing).
    *   *Gestão de Estoques e Logística:* Otimiza o armazenamento de componentes de reposição (MRO) e a logística de distribuição para as operações físicas.

## 2. Relações no Metamodelo LeanIX (Fact Sheets Relacionados)
*   **Supports (Apoia):** Todas as demais capacidades operacionais finalísticas e as metas corporativas da companhia.
*   **Supported by (Suportado por):** Plataformas corporativas de gerenciamento (ERP SAP S/4HANA, Salesforce CRM, ServiceNow ITSM/GRC, Jira Software) e agentes de IA especializados conectados a repositórios internos (ex: *Benefits Assistant*, *RFx Builder & Orchestrator*, *it-architecture-implementation-planner*).
*   **Data Objects (Objetos de Dados) Associados:** Contratos de Fornecedores, Dados Cadastrais de Colaboradores, Balanços Patrimoniais, Logs de Auditoria de Acesso e Metas de Sustentabilidade (ESG).

## 3. Avaliação de Maturidade e Importância Estratégica (Heatmap)
*   **Importância Estratégica:** `parity` (Commodity). Embora vital para a sustentabilidade operacional da companhia, esta capacidade não atua como o principal diferencial competitivo de mercado frente a concorrência.
*   **Maturidade Atual:** `Level 4 - Managed` (Processos automatizados, medidos e integrados em sua maioria através do Centro de Serviços Compartilhados).
*   **Diretriz de Investimentos em TI:** **Racionalização de custos** e **Automação de Alta Frequência**. Os investimentos em tecnologia de suporte devem focar no desacoplamento de legados, consolidação de instâncias de software redundantes (Application Rationalization) e implantação de inteligências artificiais com baixo custo operacional (Gemini Flash 3.5) para automatizar tarefas administrativas repetitivas (como leitura fiscal, triagem de logs e análise automatizada de propostas).
