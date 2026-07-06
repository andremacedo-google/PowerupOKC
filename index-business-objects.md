# Dicionário e Índice de Data Objects (Objetos de Dados)

Este arquivo de `index.md` atua como o catálogo e portal de revelação progressiva (*progressive disclosure*) para o diretório `/data-objects/` da **PowerUp Open Knowledge Catalog (PowerupOKC)**, estruturado conforme o padrão **Open Knowledge Format (OKF) v0.1** [569].

Ele lista de forma unificada os **20 Data Objects mestre** mapeados nas operações de TI corporativo e Tecnologia da Operação (TO) de campo do Setor Elétrico Brasileiro. Cada Objeto de Dados listado abaixo possui uma especificação detalhada em formato OKF, ligando-o diretamente às suas respectivas capacidades de negócio no LeanIX e às aplicações transacionais que o consomem ou produzem [52].

---

## 1. Domínio: Operações de Geração, Transmissão, Distribuição e Comercialização (OT)

Grupo funcional de objetos que trafegam entre as redes industriais de supervisão em tempo real (SCADA/EMS/ADMS), plataformas de georreferenciamento de ativos (GIS), sensores de Internet das Coisas (IoT) de campo e o portal de liquidação do mercado de energia (CCEE) [225, 235].

*   [/data-objects/do-001-leituras-telemetria-ami.md](DO-001: Leituras de Telemetria (AMI)) - {AMI}
*   [/data-objects/do-002-cadastro-georreferenciado-rede-gis.md](DO-002: Cadastro Georreferenciado de Rede (GIS)) - {GIS}
*   [/data-objects/do-003-logs-alarmes-status-scada.md](DO-003: Logs de Alarmes e Status (SCADA)) - {SCADA}
*   [/data-objects/do-004-dados-sensores-ativos-iot.md](DO-004: Dados de Sensores de Ativos (IoT)) - {IoT}
*   [/data-objects/do-005-precos-liquidacao-diferencas-pld.md](DO-005: Preços de Liquidação de Diferenças (PLD)) - {PLD}
*   [/data-objects/do-006-dados-meteorologicos.md](DO-006: Dados Meteorológicos) - {MET}

---

## 2. Domínio: Relacionamento, Medição de Consumo e Faturamento (Clientes)

Grupo de objetos de dados focados na jornada comercial de varejo "Meter-to-Cash" (da medição ao caixa) no Ambiente de Contratação Regulada (ACR), no faturamento de créditos tarifários de prossumidores de Geração Distribuída (GD) e na atração e onboarding de clientes livres no ACL [244, 250].

*   [/data-objects/do-007-cadastro-cliente-livre.md](DO-007: Cadastro de Cliente Livre) - {CLIENT}
*   [/data-objects/do-008-cadastro-prossumidor.md](DO-008: Cadastro de Prossumidor) - {PROSSUMER}
*   [/data-objects/do-009-historico-consumo-geracao.md](DO-009: Histórico de Consumo e Geração) - {CONSUMO}
*   [/data-objects/do-010-fatura-energia-cis.md](DO-010: Fatura de Energia (Conta de Luz)) - {BILLING}
*   [/data-objects/do-011-historico-ouvidoria-tickets.md](DO-011: Histórico de Ouvidoria e Tickets) - {CRM}

---

## 3. Domínio: Finanças, Jurídico, Suprimentos e Recursos Humanos (Suporte Corporativo)

Conjunto de objetos de dados mestres e transacionais que dão suporte aos fluxos de retaguarda da companhia (ERP, CLM, HRIS e ITSM), garantindo a estabilidade jurídica, apropriações contábeis e controladoria, gestão de estoque e governança de tecnologia [258, 260].

*   [/data-objects/do-012-lancamentos-contabeis-razao.md](DO-012: Lançamentos Contábeis e Razão) - {ERP}
*   [/data-objects/do-013-minutas-termos-contratuais.md](DO-013: Minutas e Termos Contratuais) - {CLM}
*   [/data-objects/do-014-resolucoes-diretrizes-aneel.md](DO-014: Resoluções e Diretrizes da ANEEL) - {REG}
*   [/data-objects/do-015-curriculos-perfis-cargos.md](DO-015: Currículos e Perfis de Cargos) - {HR}
*   [/data-objects/do-016-politicas-beneficios-rewards.md](DO-016: Políticas de Benefícios e Total Rewards) - {HR}
*   [/data-objects/do-017-logs-redes-acessos-soc.md](DO-017: Logs de Redes e Acessos (SOC)) - {SEC}
*   [/data-objects/do-018-catalogo-apis-dependencias.md](DO-018: Catálogo de APIs e Dependências) - {ARCH}
*   [/data-objects/do-019-inventario-pecas-mro.md](DO-019: Inventario de Peças Sobressalentes (MRO)) - {LOG}
*   [/data-objects/do-020-cadastro-fornecedores.md](DO-020: Cadastro de Fornecedores) - {PROCUR}
