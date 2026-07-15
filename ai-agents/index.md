# Índice e Catálogo de Agentes de IA

Este arquivo de `index.md` funciona como o portal mestre de navegação e revelação progressiva (*progressive disclosure*) para o diretório `/applications/ai-agents/` da **PowerUp OKC (Open Knowledge Catalog)**, estruturado de acordo com as especificações do padrão **Open Knowledge Format (OKF) v0.1**.

Em total alinhamento às boas práticas de modelagem do metamodelo da **SAP LeanIX v4**, os Agentes de Inteligência Artificial da companhia são catalogados como Fact Sheets do tipo **Application (Subtipo: AI Agent)**, herdando todas as suas relações lógicas e de dependências técnicas, enquanto seus respectivos modelos fundacionais (LLMs) são abstraídos como **IT Components (Subtipo: AI Model)**.

Abaixo, os **71 Agentes de IA** estão agrupados por seus respectivos domínios corporativos e de Tecnologia da Operação (TO). Cada link aponta para sua especificação técnica OKF individual (contendo System Instructions detalhadas, configurações do Agent Studio, linhagem de dados e estimativas de valor de negócios).

---

## 1. Tecnologia da Informação (TI)
Grupo funcional de assistentes cognitivos focados em suporte de chamados (ITSM), descoberta e mapeamento automático de dependências físicas e lógicas de rede (ITOM/CMDB), FinOps e governança de código de software (Git).

*   [/applications/ai-agents/agent-consultor-de-inventario-de-hardware-e-software.md](IAA-001: Consultor de Inventário de Hardware e Software) - Realiza consultas rápidas e busca em linguagem natural sobre o inventário ativo de hardware e licenças no CMDB.
*   [/applications/ai-agents/agent-lancador-automatico-de-chamados.md](IAA-002: Lançador Automático de Chamados) - Cria e classifica automaticamente chamados de suporte de primeiro nível (N1) no sistema ITSM a partir de formulários.
*   [/applications/ai-agents/agent-monitor-de-cotas-e-custos-de-cloud-finops.md](IAA-003: Monitor de Cotas e Custos de Cloud (FinOps)) - Rastreia e monitora o consumo financeiro e cotas de processamento em nuvem pública (GCP), emitindo alertas automatizados.
*   [/applications/ai-agents/agent-reconciliador-de-topologia-de-rede-e-ativos.md](IAA-004: Reconciliador de Topologia de Rede e Ativos) - Realiza o batimento estruturado e reconciliação semanal entre os dados de TI no CMDB e os ativos técnicos georreferenciados no GIS.
*   [/applications/ai-agents/agent-assistente-de-documentacao-e-playbooks-de-dados.md](IAA-005: Assistente de Documentação e Playbooks de Dados) - Proporciona RAG semântico estruturado sobre as normas, padrões e arquitetura para responder a dúvidas técnicas de desenvolvedores.
*   [/applications/ai-agents/agent-mapeador-de-fact-sheets-para-o-leanix.md](IAA-006: Mapeador de Fact Sheets para o LeanIX) - Interpreta especificações de novos sistemas e códigos de IaC para mapear dependências e sugerir ou criar Fact Sheets no LeanIX.
*   [/applications/ai-agents/agent-gerador-automatico-de-especificacoes-e-apis.md](IAA-007: Gerador Automático de Especificações e APIs) - Interpreta requisitos funcionais escritos em linguagem natural para gerar especificações OpenAPI/Swagger e esqueleto de ETLs.
*   [/applications/ai-agents/agent-assistente-de-auditoria-de-codigo-e-seguranca.md](IAA-008: Assistente de Auditoria de Código e Segurança) - Analisa de forma estática repositórios de código-fonte (Git) em busca de vulnerabilidades, credenciais vazadas ou desvios de diretrizes.
*   [/applications/ai-agents/agent-analisador-de-logs-e-causa-raiz-de-incidentes.md](IAA-009: Analisador de Logs e Causa Raiz de Incidentes) - Processa e analisa logs lógicos textuais não estruturados do ERP e do CIS para correlacionar falhas de integração.
*   [/applications/ai-agents/agent-triador-cognitivo-de-chamados-por-chat.md](IAA-010: Triador Cognitivo de Chamados por Chat) - Interage com os colaboradores via canais corporativos por chatbot, interpretando a intenção de incidentes de TI.
*   [/applications/ai-agents/agent-consultor-funcional-sap.md](IAA-011: Consultor Funcional SAP) - Explica rotas de transações SAP, guia na parametrização de módulos (FI, CO, MM, PM) e apoia equipes na migração conceitual.
*   [/applications/ai-agents/agent-analisador-de-codigo-abap.md](IAA-012: Analisador de Código ABAP) - Realiza análise estática e revisão de código personalizado em linguagem ABAP (Z-programs), garantindo padrão Clean Core.
*   [/applications/ai-agents/agent-gerador-de-documentacao-de-sistemas.md](IAA-013: Gerador de Documentação de Sistemas) - Gera de forma automatizada documentação técnica, especificações de APIs (OpenAPI/Swagger) e dicionários de tabelas.
*   [/applications/ai-agents/agent-gerador-de-manuais-de-usuarios.md](IAA-014: Gerador de Manuais de Usuários) - Elabora guias passo a passo, tutoriais de utilização e manuais de operação de sistemas para usuários finais.

---

## 2. Recursos Humanos, Saúde e Segurança
Grupo funcional de agentes responsáveis por cadastro e registro admissional digital, conciliação de ponto de equipes técnicas, elegibilidade de benefícios corporativos, análise de acordos e convenções de sindicatos e auditoria de segurança (EPI/EPR).

*   [/applications/ai-agents/agent-consultor-de-cadastro-de-colaboradores.md](IAA-015: Consultor de Cadastro de Colaboradores) - Realiza busca semântica em linguagem natural e consulta instantânea de informações cadastrais diretas do ERP.
*   [/applications/ai-agents/agent-revisor-de-registro-admisionario.md](IAA-016: Revisor de Registro Admissional) - Automatiza a criação, inserção de cadastro e provisionamento inicial de perfis de novos funcionários no ERP.
*   [/applications/ai-agents/agent-atualizador-de-certificacoes-e-nrs.md](IAA-017: Atualizador de Certificações e NRs) - Sincroniza e insere atualizações e revalidações de certificações técnicas regulatórias obrigatórias (NR-10, NR-35).
*   [/applications/ai-agents/agent-conciliador-de-registro-de-ponto.md](IAA-018: Conciliador de Registro de Ponto) - Valida as marcações do espelho de ponto das equipes técnicas de rede, cruzando dados de telemetria e escalas.
*   [/applications/ai-agents/agent-assistente-de-beneficios.md](IAA-019: Assistente de Benefícios) - Consulta elegibilidade de planos de previdência, saúde e coparticipações, gerando extratos automáticos de reembolso.
*   [/applications/ai-agents/agent-otimizador-de-descricoes-de-cargos.md](IAA-020: Otimizador de Descrições de Cargos) - Auxilia na redação e padronização inclusiva de descrições de cargo livres de vieses de linguagem.
*   [/applications/ai-agents/agent-triador-de-curriculos-e-perfis.md](IAA-021: Triador de Currículos e Perfis) - Processa e extrai entidades de currículos recebidos via OCR/NLP, realizando triagem técnica e ranqueamento.
*   [/applications/ai-agents/agent-mentor-cognitivo-de-pdis-dinamicos.md](IAA-022: Mentor Cognitivo de PDIs Dinâmicos) - Identifica gaps de capacitação cruzando feedbacks e avaliação de desempenho para sugerir trilhas baseadas em 70-20-10.
*   [/applications/ai-agents/agent-passaporte-digital-de-seguranca.md](IAA-023: Passaporte Digital de Segurança) - Audita via visão computacional a utilização correta de EPIs por eletricistas antes de iniciar ordens de manutenção em campo.
*   [/applications/ai-agents/agent-analisador-de-acordos-e-leis-trabalhistas.md](IAA-024: Analisador de Acordos e Leis Trabalhistas) - Realiza buscas semânticas em convenções coletivas de trabalho (CCT) e legislação trabalhista para subsidiar o DHO.
*   [/applications/ai-agents/agent-analisador-de-pesquisas-de-clima.md](IAA-025: Analisador de Pesquisas de Clima) - Analisa e sintetiza respostas em formato de texto livre de pesquisas de clima institucionais, mapeando sentimentos.

---

## 3. Suprimentos, Logística e Sourcing
Grupo de agentes focados na eficiência da cadeia de suprimentos (*Procure-to-Pay*), monitoramento de estoque técnico MRO, preenchimento assistido de requisições de compras, monitoramento de vigência de contratos e compliance ESG de fornecedores.

*   [/applications/ai-agents/agent-consultor-de-catalogo-e-saldo-de-materiais.md](IAA-026: Consultor de Catálogo e Saldo de Materiais) - Realiza consulta em tempo real de especificações técnicas e saldos físicos de estoque de rede nos almoxarifados.
*   [/applications/ai-agents/agent-assistente-de-requisicao-de-compra-e-md.md](IAA-027: Assistente de Requisição de Compra e MD) - Apoia o requisitante no preenchimento de campos de requisições de compras e na padronização de metadados.
*   [/applications/ai-agents/agent-monitor-de-saldo-e-vigencia-de-contratos.md](IAA-028: Monitor de Saldo e Vigência de Contratos) - Rastreia o consumo financeiro (saldo) e prazos de vigência de contratos, emitindo alertas de renegociação prévia.
*   [/applications/ai-agents/agent-sincronizador-de-fichas-de-fornecedores.md](IAA-029: Sincronizador de Fichas de Fornecedores) - Consulta certidões de regularidade e restrições em APIs públicas federais/estaduais, atualizando dados fiscais no ERP.
*   [/applications/ai-agents/agent-lancador-de-recebimento-de-materiais.md](IAA-030: Lançador de Recebimento de Materiais) - Executa lançamento automático de entrada física de materiais (transação MIGO) após o cruzamento com o pedido.
*   [/applications/ai-agents/agent-conciliador-transacional-de-faturas.md](IAA-031: Conciliador Transacional de Faturas) - Realiza a conciliação automática básica de três vias (3-Way Matching) cruzando XML, pedido e recebimento técnico.
*   [/applications/ai-agents/agent-assistente-de-elaboracao-de-editais-de-sourcing.md](IAA-032: Assistente de Elaboração de Editais de Sourcing) - Redige minutas de RFI/RFP, auditando e sugerindo alternativas para evitar cláusulas de exclusividade técnica.
*   [/applications/ai-agents/agent-analisador-de-clausulas-e-riscos-contratuais.md](IAA-033: Analisador de Cláusulas e Riscos Contratuais) - Analisa minutas contra diretrizes de compliance internas, gerando sumários de Red Flags em SLAs de O&M e penalidades.
*   [/applications/ai-agents/agent-validador-de-cadastro-e-homologacao-de-fornecedores.md](IAA-034: Validador de Cadastro e Homologação de Fornecedores) - Extrai dados cadastrais via OCR/NLP de documentos digitalizados recebidos para apoiar o fluxo de pré-qualificação.
*   [/applications/ai-agents/agent-auditor-de-riscos-esg-de-fornecedores.md](IAA-035: Auditor de Riscos ESG de Fornecedores) - Varre portais de notícias, diários oficiais e relatórios ambientais públicos para alimentar scorecards socioambientais de terceiros.
*   [/applications/ai-agents/agent-analisador-de-divergencias-e-disputas-de-faturamento.md](IAA-036: Analisador de Divergências e Disputas de Faturamento) - Avalia dados históricos de interações por e-mail e anexos contendo contestações de faturamento fiscal.

---

## 4. Jurídico, Contratos e Regulação
Conjunto de assistentes encarregados do acompanhamento de andamentos jurídicos do contencioso, triagem inteligente de petições e multas, outorga de procurações societárias, auditoria regulatória de diários oficiais (ANEEL) e controle de prazos contratuais.

*   [/applications/ai-agents/agent-consultor-de-metadados-de-contratos.md](IAA-037: Consultor de Metadados de Contratos) - Realiza consultas rápidas e busca em linguagem natural sobre vigências, partes, valores e reajustes no SAP CLM.
*   [/applications/ai-agents/agent-sincronizador-de-processos-judiciais.md](IAA-038: Sincronizador de Processos Judiciais) - Registra de forma automatizada novos processos recebidos e atualiza os andamentos estruturados no módulo legal.
*   [/applications/ai-agents/agent-sincronizador-de-procuracoes-e-poderes.md](IAA-039: Sincronizador de Procurações e Poderes) - Automatiza o registro, controle de vigências e limites financeiros das procurações de diretores e gerentes.
*   [/applications/ai-agents/agent-lancador-de-depositos-e-custas-judiciais.md](IAA-040: Lançador de Depósitos e Custas Judiciais) - Gera requisições de pagamento de custas e depósitos recursais no contas a pagar após andamentos de TO.
*   [/applications/ai-agents/agent-monitor-de-provisoes-e-garantias.md](IAA-041: Monitor de Provisões e Garantias) - Consulta e consolida o saldo das provisões contábeis de perdas do contencioso (provável, possível, remota) no ERP.
*   [/applications/ai-agents/agent-conciliador-de-despesas-de-escritorios.md](IAA-042: Conciliador de Despesas de Escritórios) - Realiza a conciliação transacional estruturada entre as faturas físicas (time-sheets) de escritórios terceiros e os limites.
*   [/applications/ai-agents/agent-assistente-de-elaboracao-de-minutas.md](IAA-043: Assistente de Elaboração de Minutas) - Gera rascunhos iniciais de minutas de contratos e aditivos padronizados utilizando a biblioteca de cláusulas aprovadas.
*   [/applications/ai-agents/agent-analisador-de-clausulas-e-riscos.md](IAA-044: Analisador de Cláusulas e Riscos) - Analisa minutas de contratos complexos de terceiros contra o playbook interno, identificando limites de responsabilidade.
*   [/applications/ai-agents/agent-triador-de-peticoes-e-contencioso.md](IAA-045: Triador de Petições e Contencioso) - Lê petições iniciais digitalizadas, resume os pleitos, extrai os valores envolvidos e indica subsídios técnicos locais.
*   [/applications/ai-agents/agent-auditor-de-normas-e-jurisprudencia.md](IAA-046: Auditor de Normas e Jurisprudência) - Monitora continuamente resoluções, despachos e diários oficiais de órgãos reguladores (ANEEL, CCEE, ONS), sintetizando impactos.
*   [/applications/ai-agents/agent-monitor-de-prazos-e-obrigacoes.md](IAA-047: Monitor de Prazos e Obrigações) - Extrai obrigações de fazer, marcos lógicos, metas regulatórias e termos de prorrogação contidos no texto livre de contratos.
*   [/applications/ai-agents/agent-analisador-de-acordos-e-sentencas.md](IAA-048: Analisador de Acordos e Sentenças) - Processa sentenças de tribunais em texto livre, avaliando probabilidade de êxito e sugerindo conciliações baseadas em ROI.

---

## 5. Finanças, Controladoria e Tesouraria
Frente de força de trabalho digital voltada à simplificação de rotinas contábeis societárias (IFRS) e regulatórias (Manual de Contabilidade do Setor Elétrico - MCSE da ANEEL), conciliação bancária, monitoramento de caixa e unitização física-financeira patrimonial (BRR).

*   [/applications/ai-agents/agent-consultor-de-lancamentos-e-saldos-contabeis.md](IAA-049: Consultor de Lançamentos e Saldos Contábeis) - Realiza consultas rápidas e busca em linguagem natural sobre lançamentos em contas do Razão e saldos por centros de custo.
*   [/applications/ai-agents/agent-sincronizador-de-contas-a-pagar-e-faturas.md](IAA-050: Sincronizador de Contas a Pagar e Faturas) - Registra e atualiza automaticamente faturas de fornecedores aprovadas e dados de contas a pagar no ERP contábil.
*   [/applications/ai-agents/agent-lancador-de-provisoes-de-fechamento.md](IAA-051: Lançador de Provisões de Fechamento) - Executa lançamentos automáticos de provisões e acréscimos recorrentes de fechamento no Livro Razão Geral.
*   [/applications/ai-agents/agent-sincronizador-de-conciliacao-bancaria.md](IAA-052: Sincronizador de Conciliação Bancária) - Sincroniza a conciliação de lançamentos contábeis no ERP após validar arquivos de extrato com alta similaridade.
*   [/applications/ai-agents/agent-monitor-de-saldos-e-limites-de-caixa.md](IAA-053: Monitor de Saldos e Limites de Caixa) - Rastreia e monitora continuamente os saldos e limites mínimos operacionais de contas bancárias corporativas da holding.
*   [/applications/ai-agents/agent-sincronizador-de-ativos-imobilizados.md](IAA-054: Sincronizador de Ativos Imobilizados) - Atualiza automaticamente o cadastro de ativos imobilizados no módulo contábil do ERP após a unitização patrimonial.
*   [/applications/ai-agents/agent-assistente-de-triagem-de-faturas-em-pdf.md](IAA-055: Assistente de Triagem de Faturas em PDF) - Processa faturas recebidas por e-mail, extraindo metadados críticos via OCR/NLP para validação prévia de contas.
*   [/applications/ai-agents/agent-analisador-de-covenants-e-contratos-de-divida.md](IAA-056: Analisador de Covenants e Contratos de Dívida) - Lê contratos de dívida em PDF para identificar cláusulas restritivas financeiras, cruzando-as com balanços contábeis.
*   [/applications/ai-agents/agent-orquestrador-de-unitizacao-e-brr.md](IAA-057: Orquestrador de Unitização e BRR) - Interpreta o Manual do MCPSE e o PRORET, apoiando a capitalização de despesas e unitização na BRR perante a ANEEL.
*   [/applications/ai-agents/agent-consultor-de-relatorios-financeiros-e-dre-conversacional.md](IAA-058: Consultor de Relatórios Financeiros e DRE Conversacional) - Provê análises de balanço, DRE e DFC via perguntas em linguagem natural (traduzindo para queries SQL).
*   [/applications/ai-agents/agent-preditor-de-fluxo-de-caixa-e-cotacoes-do-setor.md](IAA-059: Preditor de Fluxo de Caixa e Cotações do Setor) - Projeta as curvas de fluxo de caixa diárias com modelos de ML, integrando dados do ERP, PLD horário e clima.
*   [/applications/ai-agents/agent-simulador-de-exposicao-cambial-e-derivativos.md](IAA-060: Simulador de Exposição Cambial e Derivativos) - Realiza simulações de Monte Carlo e cálculos de Value at Risk (VaR) para recomendar estratégias de hedge cambial.

---

## 6. Marketing, Vendas e Relacionamento (CRM)
Grupo focado na experiência de atendimento do consumidor de energia (cativo no ACR e livre no ACL), triagem e análise de sentimentos em contestações de faturamento (REN ANEEL 1.000), prospecção comercial e simulação de economia tarifária B2B.

*   [/applications/ai-agents/agent-consultor-de-consumo-e-perfil-do-cliente.md](IAA-061: Consultor de Consumo e Perfil do Cliente) - Consulta de forma ágil o histórico de consumo acumulado, perfil tarifário e informações da UC no CIS.
*   [/applications/ai-agents/agent-sincronizador-de-campanhas-e-interacoes.md](IAA-062: Sincronizador de Campanhas e Interações) - Atualiza e cria novos registros de campanhas, interações de e-mail e status de oportunidades no CRM.
*   [/applications/ai-agents/agent-monitor-de-conversao-e-leads-de-vendas.md](IAA-063: Monitor de Conversão e Leads de Vendas) - Analisa a taxa de avanço e conversão de oportunidades no funil de vendas, calculando tempos de permanência.
*   [/applications/ai-agents/agent-calculador-de-churn-e-risco-de-evasao.md](IAA-064: Calculador de Churn e Risco de Evasão) - Rastreia indicadores comerciais e faturamentos em aberto, gravando scores de risco diretamente no CRM.
*   [/applications/ai-agents/agent-atualizador-de-contratos-de-vendas.md](IAA-065: Atualizador de Contratos de Vendas) - Registra a formalização e os parâmetros contratuais de novas adesões no Ambiente de Contratação Livre (ACL).
*   [/applications/ai-agents/agent-gerador-de-conteudo-e-campanhas-multicanal.md](IAA-066: Gerador de Conteúdo e Campanhas Multicanal) - Redige textos promocionais, e-mails de marketing e pushes personalizados baseando-se no tom de voz da marca.
*   [/applications/ai-agents/agent-analisador-de-sentimento-e-interacoes-de-clientes.md](IAA-067: Analisador de Sentimento e Interações de Clientes) - Processa reclamações de faturamento, transcrições de SAC e mídias sociais para identificar dores frequentes.
*   [/applications/ai-agents/agent-assistente-de-prospeccao-e-simulacao-de-economia.md](IAA-068: Assistente de Prospecção e Simulação de Economia) - Consome faturas de concorrentes e tarifas da ANEEL para elaborar simulações de viabilidade de migração ao ACL.
*   [/applications/ai-agents/agent-gerador-de-imagens-e-layouts-publicitarios.md](IAA-069: Gerador de Imagens e Layouts Publicitários) - Cria esboços conceituais, banners de campanhas de eficiência energética e ilustrações sob manual estético.
*   [/applications/ai-agents/agent-consultor-de-portfolio-de-servicos-e-eficiencia.md](IAA-070: Consultor de Portfólio de Serviços e Eficiência) - RAG conversacional treinado no portfólio de Eficiência Energética, carregamento de veículos elétricos (VEM) e EaaS.
*   [/applications/ai-agents/agent-auditor-de-conformidade-de-pecas-publicitarias.md](IAA-071: Auditor de Conformidade de Peças Publicitárias) - Analisa textos e criativos antes da veiculação, verificando conformidade contra CONAR e resoluções da ANEEL.
