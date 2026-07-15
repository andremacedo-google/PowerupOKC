# Índice e Catálogo de Aplicações de Negócio (Business Applications)

Este arquivo de `index.md` atua como o portal de progressive disclosure (revelação progressiva) e inventário consolidado para o diretório `/business-applications/` da **PowerUp OKC (Open Knowledge Catalog)**, estruturado em estrita conformidade com as especificações do padrão **Open Knowledge Format (OKF) v0.1**.

Em total alinhamento às boas práticas de modelagem do metamodelo da **SAP LeanIX v4**, as aplicações tradicionais core da concessionária são catalogadas sob a classe de primeiro nível **Application (Subtipo: Business Application)**. Elas são nomeadas de acordo com suas funções lógicas padrão de mercado (desacoplando-as de marcas e soluções comerciais específicas de fornecedores), o que garante estabilidade conceitual e governança frente a futuros ciclos de migração técnica ou reestruturações de TI/TO.

Este catálogo consolida o portfólio de **16 aplicações de negócio lógicas** (Systems of Truth - SOT) responsáveis pela orquestração dos fluxos de dados estruturados da concessionária. Todos os Fact Sheets de aplicações estão localizados na mesma pasta raiz, em uma estrutura plana e sem subdivisão por subpastas corporativas, garantindo facilidade de governança e compatibilidade total com repositórios Git de integração contínua (CI/CD).

---

## 1. Portfólio de Sistemas de Registro e Operação (TI/TO)

Abaixo estão listadas as 16 Business Applications lógicas que compõem a espinha dorsal de sistemas e processos finalísticos do ecossistema de utilidades da PowerUp:

*   [app-erp-gestao-financeira](/business-applications/app-erp-gestao-financeira.md) - **(ID: AP-001)** {ERP} Sistema central de registro contábil, fiscal e controladoria corporativa. Responsável pela apropriação física de projetos de capital (CAPEX) e acompanhamento contábil societário (IFRS).
*   [app-erp-tesouraria](/business-applications/app-erp-tesouraria.md) - **(ID: AP-002)** {TRM} Gerenciador de liquidez, controle diário de fluxo de caixa e contabilização de posições financeiras de proteção (hedge) contra as flutuações de preços de mercado spot (PLD).
*   [app-hris-sistema-rh](/business-applications/app-hris-sistema-rh.md) - **(ID: AP-003)** {HCM} Plataforma mestre de recursos humanos (ciclo *Hire-to-Retire*), faturamento de folha de pagamento e gestão de certificações regulatórias técnicas e de segurança obrigatórias (NR-10, NR-35).
*   [app-clm-gestao-contratos](/business-applications/app-clm-gestao-contratos.md) - **(ID: AP-004)** {CLM} Repositório central de compliance jurídico para gestão do ciclo de vida de contratos EPC de engenharia, PPAs bilaterais de longo prazo, contratos de conexão física (CUSD/CUST) e limits de alçada.
*   [app-grc-governanca-riscos](/business-applications/app-grc-governanca-riscos.md) - **(ID: AP-005)** {GRC} Plataforma corporativa de gestão de riscos (ERM), testes e eficácia de controles internos para conformidade SOX e monitoramento centralizado de vulnerabilidades regulatórias da ANEEL.
*   [app-ehs-gestao-saude-seguranca](/business-applications/app-ehs-gestao-saude-seguranca.md) - **(ID: AP-006)** {EHS} Sistema focado em saúde ocupacional, conformidade ambiental, registro e causa raiz de incidentes de segurança de campo e controle síncrono de condicionantes de licenças de operação.
*   [app-itsm-gestao-servicos-ti](/business-applications/app-itsm-gestao-servicos-ti.md) - **(ID: AP-007)** {ITSM} Centralização de chamados de suporte técnico de TI, orquestração de requisições de mudança (Change), e gerenciamento do CMDB convergente de infraestrutura e rede industrial de TO.
*   [app-srm-gestao-compras-sourcing](/business-applications/app-srm-gestao-compras-sourcing.md) - **(ID: AP-008)** {BSM} Sourcing estratégico de compras corporativas, homologação fiscal-trabalhista de novos fornecedores e emissão de pedidos associados a Elementos PEP de investimento.
*   [app-wms-gestao-estoques-almoxarifado](/business-applications/app-wms-gestao-estoques-almoxarifado.md) - **(ID: AP-009)** {WMS} Gerenciamento avançado de estoques físicos e logística de suprimentos em almoxarifados para armazenamento e preservação técnica de peças sobressalentes de redes MRO.
*   [app-crm-relacionamento-cliente](/business-applications/app-crm-relacionamento-cliente.md) - **(ID: AP-010)** {CRM} Portal de engajamento do cliente e suporte omnichannel, responsável por prospecção B2B de mercado livre (ACL), onboarding de faturamento e registro de casos de reclamações.
*   [app-cis-faturamento-comercial](/business-applications/app-cis-faturamento-comercial.md) - **(ID: AP-011)** {CIS} Espinha dorsal comercial que executa faturamento massivo de tarifas elétricas reguladas (TUSD/TE), bandeiras da ANEEL, rateio síncrono de créditos de GD e ordens de cobrança e suspensão.
*   [app-mdm-gestao-medicao](/business-applications/app-mdm-gestao-medicao.md) - **(ID: AP-012)** {MDM} Motor analítico central para ingestão de telemetria inteligente de medidores AMI de prossumidores, executando síncronamente o motor de regras VEE antes do repasse ao CIS.
*   [app-adms-gestao-redes-distribuicao](/business-applications/app-adms-gestao-redes-distribuicao.md) - **(ID: AP-013)** {ADMS} Tecnologia da Operação (TO) em tempo real que reúne supervisão de rede (SCADA de média/baixa tensão), restabelecimento automatizado FLISR e apuração de indicadores de continuidade DEC/FEC.
*   [app-eam-engenharia-gestao-ativos](/business-applications/app-eam-engenharia-gestao-ativos.md) - **(ID: AP-014)** {EAM} Engenharia de confiabilidade e gestão do ciclo de vida físico de turbinas, geradores e transformadores. Rege as Ordens de Manutenção (OM) e os planos preventivos sistemáticos.
*   [app-gis-georreferenciamento-redes](/business-applications/app-gis-georreferenciamento-redes.md) - **(ID: AP-015)** {GIS} Fonte da verdade técnica *as-built* georreferenciada da infraestrutura física de postes, circuitos e vãos de linhas, atuando como barramento para a BDGD regulatória.
*   [app-etrm-gestao-trading-comercializacao](/business-applications/app-etrm-gestao-trading-comercializacao.md) - **(ID: AP-016)** {ETRM} Orquestração de middle e back-office para comercialização física e financeira de energia, precificação baseada em curvas futuras e cálculo estatístico de limites de risco (Value at Risk - VaR).

---

## 2. Princípios de Governança e Racionalização de Portfólio (Gartner TIME)

A integração destas Business Applications de primeiro nível com as capabilities e com as equipes proprietárias viabiliza ao comitê de arquitetura a aplicação do framework de tomada de decisão estratégica **Gartner TIME (Tolerate, Invest, Migrate, Eliminate)**:

1.  **INVEST (Investir - ex: MDM, ADMS, GIS):** Sistemas finalísticos de alto valor de negócio e alinhados à transição energética de redes inteligentes recebem prioridade de orçamento para modernização tecnológica contínua.
2.  **TOLERATE (Tolerar - ex: Ferramentas especialistas locais):** Aplicações que demonstram estabilidade técnica e baixo custo operacional são mantidas em operação normal de sustentação, sem necessidade de reengenharia.
3.  **MIGRATE (Migrar - ex: Sistemas Core Legados):** Aplicações importantes que residem sobre infraestruturas legadas e obsoletas que expõem a concessionária a riscos operacionais são elegíveis para migração em direção à nuvem (SaaS).
4.  **ELIMINATE (Eliminar - ex: Sistemas Redundantes):** Sistemas departamentais, em silos de dados ou com escopo duplicado, são desativados de forma planejada, concentrando a SOT (System of Truth) no barramento corporativo.

---

### # Citações e Fontes de Referência Normativas

1.  **SAP LeanIX Metamodel Best Practice Guidelines (v4):** Estabelece o padrão de portfólio de aplicações separando o escopo funcional da representação física de fornecedores e infraestrutura.
2.  **Open Knowledge Format (OKF) Specification v0.1:** Define a estrutura enxuta de progressive disclosure por meio de índices livres de YAML frontmatter com links absolutos de repositório.
3.  **Resolução Normativa ANEEL nº 964/2021 (Cibersegurança):** Rege as obrigações de segmentação lógica de barramentos de TI e TO na infraestrutura de utilities nacionais.
