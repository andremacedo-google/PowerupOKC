# Índice de Aplicações de Negócio (Business Applications) — PowerUp Open Knowledge Catalog

Este diretório contém os **Fact Sheets** das **Business Applications (Sistemas Transacionais Core)** da **PowerUp Open Knowledge Catalog (PowerupOKC)**. A taxonomia segue estritamente as regras de modelagem do metamodelo v4 da **SAP LeanIX**, separando os sistemas transacionais core (`Business Application`) dos agentes analíticos e copilotos cognitivos (`AI Agent`).

As aplicações são denominadas pelo seu **Nome Funcional/Padrão de Mercado** de forma a promover o desacoplamento de fornecedor, mapeando as tecnologias líderes disponíveis em uma coluna de atributos secundários.

---

## 1. Corporativo e Suporte ao Negócio

Esta camada engloba os sistemas que suportam os processos administrativos, financeiros, regulatórios, de suprimentos e de governança técnica que sustentam a resiliência corporativa do grupo.

### Gestão Estratégica e Financeira
*   [ERP - Gestão Financeira, Contábil e Controladoria](/applications/app-erp-gestao-financeira.md) (ID: **AP-001**) - Sistema central de registro contábil, apuração fiscal, contabilidade de custos e fechamento societário.
*   [ERP - Gestão de Tesouraria e Riscos Financeiros](/applications/app-erp-tesouraria.md) (ID: **AP-002**) - Controla a liquidez diária, posições bancárias e executa as estratégias de hedge financeiro e de energia.

### Gestão de Pessoas e Cultura
*   [HRIS - Sistema de Informações de Recursos Humanos](/applications/app-hris-sistema-rh.md) (ID: **AP-003**) - Governa a folha de pagamento, ciclos de avaliação de desempenho e controle de treinamentos obrigatórios (ex: NR10 de campo).

### Gestão Jurídica e de Compliance
*   [CLM - Gestão do Ciclo de Vida de Contratos](/applications/app-clm-gestao-contratos.md) (ID: **AP-004**) - Sistema de orquestração de minutas contratuais, workflows de aprovações e assinaturas jurídicas.
*   [GRC - Governança, Riscos e Conformidade](/applications/app-grc-governanca-riscos.md) (ID: **AP-005**) - Plataforma de gerenciamento de riscos corporativos, testes de controles internos (SOX) e auditoria.
*   [EHS - Gestão de Saúde, Segurança e Meio Ambiente](/applications/app-ehs-gestao-saude-seguranca.md) (ID: **AP-006**) - Controla acidentes de trabalho, permissões de segurança de campo e conformidade de licenças ambientais.

### Gestão de Tecnologia da Informação
*   [ITSM / ITOM - Gestão de Serviços de TI](/applications/app-itsm-itom-servicos-ti.md) (ID: **AP-007**) - Centraliza o gerenciamento de incidentes TI/OT, requisições de mudanças e o banco de dados de gerenciamento de configuração (CMDB).

### Gestão da Cadeia de Suprimentos
*   [SRM / Sourcing - Gestão de Compras e Suprimentos](/applications/app-srm-compras-sourcing.md) (ID: **AP-008**) - Gerencia requisições de compras, equalização de propostas comerciais e emissão de pedidos de compras.
*   [WMS / MRO - Gestão de Estoques e Almoxarifados](/applications/app-wms-mro-estoques.md) (ID: **AP-009**) - Controla o inventário físico de materiais sobressalentes de campo e a logística de movimentação de mercadorias.

---

## 2. Engajamento com o Cliente

Camada que mapeia os sistemas que apoiam a jornada de varejo elétrico, abrangendo desde o atendimento multicanal até o complexo ciclo Meter-to-Cash (medição ao caixa) para clientes livres e cativos.

### Gestão do Relacionamento com o Cliente
*   [CRM - Gestão de Relacionamento e Atendimento ao Cliente](/applications/app-crm-relacionamento-cliente.md) (ID: **AP-010**) - Fornece visão 360 do consumidor livre ou regulado, centralizando logs de ouvidoria e casos.

### Faturamento e Cobrança
*   [CIS - Sistema de Faturamento e Informações Comerciais](/applications/app-cis-faturamento-comercial.md) (ID: **AP-011**) - Motor transacional comercial para faturamento de tarifas da ANEEL e cálculo de compensação de geração distribuída (GD).
*   [MDM - Gestão de Dados de Medição](/applications/app-mdm-gestao-medicao.md) (ID: **AP-012**) - Repositório central de telemetria inteligente AMI focado na validação, edição e estimativa (VEE) de curvas de carga.
*   [Sub-razão de Cobrança e Contas a Receber](/applications/app-sub-razao-cobranca.md) (ID: **AP-013**) - Processa arrecadações volumosas, executa réguas de cobrança (dunning) e dispara ordens técnicas de corte por inadimplência.

---

## 3. Operações de Energia

Esta camada reúne as tecnologias industriais de Tecnologia da Operação (TO) e controle físico de rede, além dos sistemas de previsão meteorológica, planejamento offline e inteligência comercial de trading.

### Geração de Energia
*   [SCADA - Supervisão e Controle de Usinas](/applications/app-scada-supervisao-usinas.md) (ID: **AP-014**) - Sistema industrial para supervisão e controle remoto em tempo real de usinas geradoras síncronas.

### Transmissão de Energia
*   [EMS / SCADA - Gestão de Redes de Transmissão](/applications/app-ems-scada-transmissao.md) (ID: **AP-015**) - Plataforma de TO focada em estimativa de estado de rede, controle automático de geração (AGC) e estabilidade de alta tensão.

### Distribuição de Energia
*   [ADMS / OMS - Gestão de Redes de Distribuição](/applications/app-adms-gestao-redes-distribuicao.md) (ID: **AP-016**) - Orquestra recomposição automática (FLISR), otimização de tensão (VVO) e localização de falhas em média/baixa tensão.

### Trading de Energia e Gestão de Risco
*   [ETRM - Gestão de Comercialização de Energia e Risco](/applications/app-etrm-trading-risco.md) (ID: **AP-017**) - Plataforma de suporte à mesa de comercialização livre de energia, registrando contratos bilaterais e monitorando riscos de mercado (VaR).

### Gestão de Ativos e Rede
*   [EAM - Gestão e Desempenho Físico de Ativos](/applications/app-eam-engenharia-ativos.md) (ID: **AP-018**) - Controla o cadastro mestre e o ciclo de vida físico de transformadores, religadores e linhas (SAP PM / IBM Maximo).
*   [GIS - Sistema de Informação Geográfica de Redes](/applications/app-gis-georreferenciamento-redes.md) (ID: **AP-019**) - Base de dados topológica georreferenciada da rede física, servindo como fonte da verdade espacial de conectividade.

---

## Diretrizes de Utilização do Catálogo (OKF)
1. **Navegação Progressiva:** Ao explorar este catálogo, utilize este índice para obter uma visão geral funcional antes de navegar para os documentos de especificações individuais, os quais detalham os fluxos de dados (CRUD) e as integrações por API de cada barramento.
2. **Criação de Novas Aplicações:** Toda nova especificação adicionada a este diretório deve ser nomeada em conformidade com o padrão `app-{slug-do-sistema}.md` e declarada neste índice de forma idêntica.
3. **Mapeamento de APIs:** As conexões transacionais e interfaces físicas entre os sistemas listados acima estão detalhadas sob a pasta `/interfaces/` do repositório, garantindo conformidade com o metamodelo SAP LeanIX.