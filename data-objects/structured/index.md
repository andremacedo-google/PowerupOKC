# Dicionário de Dados Estruturados (Structured Data Objects)

Este arquivo de `index.md` atua como o catálogo de navegação unificado e plano para o diretório `/data-objects/structured/` da **PowerUp OKC**, estruturado conforme as especificações de progressive disclosure do padrão **Open Knowledge Format (OKF) v0.1**.

Ele consolida em uma única lista plana as **81 entidades de dados estruturados** do grupo, mapeadas sob a faixa de IDs **`DO-101` a `DO-181`**, abrangendo as frentes de Tecnologia da Operação (TO), Comercial/Clientes e Suporte Corporativo. Todos os Fact Sheets encontram-se na mesma pasta, eliminando a dependência física de subdiretórios e facilitando a governança descentralizada de dados e integrações lógicas de IA.

---

## 1. Catálogo de Objetos de Dados Estruturados (IDs DO-101 a DO-181)

Abaixo estão listadas as especificações de cada objeto de dados estruturado do portfólio. Cada link aponta de forma absoluta e estável para o Fact Sheet correspondente:

*   [do-101-ativo-tecnico.md](/data-objects/structured/do-101-ativo-tecnico.md) - {Ativos} Representação física de equipamentos de campo, geradores e transformadores (SAP PM) [cite: 101].
*   [do-102-modelo-topologico-da-rede.md](/data-objects/structured/do-102-modelo-topologico-da-rede.md) - {Ativos} Relações geoespaciais de conectividade do GIS exportadas ao SCADA [cite: 102].
*   [do-103-balanco-de-energia.md](/data-objects/structured/do-103-balanco-de-energia.md) - {DIST} SAMP - Balanço mensal consolidado de perdas técnicas e comerciais da distribuidora [cite: 103].
*   [do-104-equipamento-distribuidora-ativo.md](/data-objects/structured/do-104-equipamento-distribuidora-ativo.md) - {DIST} Ativo físico associado à unidade técnica de placas regulatórias (MCPSE) [cite: 104].
*   [do-105-evento-de-interrupcao-dec-fec.md](/data-objects/structured/do-105-evento-de-interrupcao-dec-fec.md) - {DIST} Eventos de falta de energia para cálculo síncrono dos indicadores DEC/FEC [cite: 105].
*   [do-106-local-de-instalacao-distribuicao.md](/data-objects/structured/do-106-local-de-instalacao-distribuicao.md) - {DIST} Estrutura posicional hierárquica que atua como container técnico de ativos [cite: 106].
*   [do-107-perda-tecnica-de-energia.md](/data-objects/structured/do-107-perda-tecnica-de-energia.md) - {DIST} Simulação de perdas elétricas nos condutores e transformadores (OpenDSS) [cite: 107].
*   [do-108-ponto-notavel.md](/data-objects/structured/do-108-ponto-notavel.md) - {DIST} Pontos georreferenciados que localizam postes e torres de distribuição aérea [cite: 108].
*   [do-109-subestacao-da-distribuidora-instalacao.md](/data-objects/structured/do-109-subestacao-da-distribuidora-instalacao.md) - {DIST} Polígono de delimitação física de subestação rebaixadora (PRODIST Módulo 3) [cite: 109].
*   [do-110-unidade-geradora-distribuicao-instalacao.md](/data-objects/structured/do-110-unidade-geradora-distribuicao-instalacao.md) - {DIST} Ponto de conexão física de minigeração distribuída solar (Lei 14.300) [cite: 110].
*   [do-111-unidade-transformadora-instalacao.md](/data-objects/structured/do-111-unidade-transformadora-instalacao.md) - {DIST} Transformadores de distribuição aérea de média para baixa tensão [cite: 111].
*   [do-112-conjunto-de-usinas.md](/data-objects/structured/do-112-conjunto-de-usinas.md) - {G&T} Estrutura lógica ONS que consolida o despacho de eólicas e solares [cite: 112].
*   [do-113-curva-de-capacidade-eficiencia.md](/data-objects/structured/do-113-curva-de-capacidade-eficiencia.md) - {G&T} Curva de produtibilidade e eficiência hidráulica/mecânica de geradores [cite: 113].
*   [do-114-dado-hidrologico.md](/data-objects/structured/do-114-dado-hidrologico.md) - {G&T} Níveis e vazões físicas de reservatórios, vazão afluente e defluente (ONS) [cite: 114].
*   [do-115-fluxo-de-potencia.md](/data-objects/structured/do-115-fluxo-de-potencia.md) - {G&T} Telemetria de potência ativa e reativa enviadas síncronamente ao ONS [cite: 115].
*   [do-116-grupo-de-pequenas-usinas.md](/data-objects/structured/do-116-grupo-de-pequenas-usinas.md) - {G&T} Agrupador ONS para supervisão de carga e geração de PCHs no SIN [cite: 116].
*   [do-117-linha-de-transmissao-lt.md](/data-objects/structured/do-117-linha-de-transmissao-lt.md) - {G&T} Troncos de Rede Básica de alta tensão sob as metas contratuais de RAP [cite: 117].
*   [do-118-medicao-fasorial-sincronizada-pmu.md](/data-objects/structured/do-118-medicao-fasorial-sincronizada-pmu.md) - {G&T} Dados síncronos de alta frequência (ângulo e magnitude de fase) de PMUs [cite: 118].
*   [do-119-programa-despacho-de-geracao.md](/data-objects/structured/do-119-programa-despacho-de-geracao.md) - {G&T} Diretrizes e despachos lógicos horários programados para usinas do SIN [cite: 119].
*   [do-120-reservatorio-hidraulico.md](/data-objects/structured/do-120-reservatorio-hidraulico.md) - {G&T} Reservatório de acumulação associado a usinas para coordenação hidráulica [cite: 120].
*   [do-121-subestacao-da-rede-basica-instalacao.md](/data-objects/structured/do-121-subestacao-da-rede-basica-instalacao.md) - {G&T} Concentração física de barras e conexões de alta tensão de Rede Básica [cite: 121].
*   [do-122-transformador-de-potencia-equipamento.md](/data-objects/structured/do-122-transformador-de-potencia-equipamento.md) - {G&T} Grandes transformadores responsáveis pelo rebaixamento de transmissão (CCAT) [cite: 122].
*   [do-123-unidade-geradora-equipamento.md](/data-objects/structured/do-123-unidade-geradora-equipamento.md) - {G&T} Turbinas e geradores individuais (Procedimentos de Rede Submódulo 9.2) [cite: 123].
*   [do-124-usina-de-geracao-instalacao.md](/data-objects/structured/do-124-usina-de-geracao-instalacao.md) - {G&T} Cadastro de usina em todas as fases regulatórias perante a ANEEL (SIGA) [cite: 124].
*   [do-125-ordem-de-manutencao-om.md](/data-objects/structured/do-125-ordem-de-manutencao-om.md) - {Manutenção} Ordem transacional de serviços (PM) e apropriação de despesas operacionais [cite: 125].
*   [do-126-plano-de-manutencao.md](/data-objects/structured/do-126-plano-de-manutencao.md) - {Manutenção} Cronograma preventivo de manutenção baseados em ciclos sistemáticos [cite: 126].
*   [do-127-pagamento.md](/data-objects/structured/do-127-pagamento.md) - {Arrecadação} Registro síncrono de quitação de títulos fiscais integrados a bancos (FI-CA) [cite: 127].
*   [do-128-ordem-de-servico-comercial.md](/data-objects/structured/do-128-ordem-de-servico-comercial.md) - {Atendimento} Ordens técnicas comerciais de campo (novas ligações, religações, cortes) [cite: 128].
*   [do-129-reclamacao-de-cliente.md](/data-objects/structured/do-129-reclamacao-de-cliente.md) - {Atendimento} Registro de contestações, falta de energia e desvios comerciais de faturamento [cite: 129].
*   [do-130-area-de-atuacao.md](/data-objects/structured/do-130-area-de-atuacao.md) - {Cadastro} Polígonos de georreferenciamento de área de concessão regulada (ARAT) [cite: 130].
*   [do-131-cliente-parceiro-de-negocio.md](/data-objects/structured/do-131-cliente-parceiro-de-negocio.md) - {Cadastro} Dados cadastrais, endereço e CNPJ de parceiros de faturamento comercial (BP) [cite: 131].
*   [do-132-conjunto-de-consumidores.md](/data-objects/structured/do-132-conjunto-de-consumidores.md) - {Cadastro} Agrupamento geopolítico de consumidores base para apuração de DEC/FEC [cite: 132].
*   [do-133-contrato-de-fornecimento.md](/data-objects/structured/do-133-contrato-de-fornecimento.md) - {Cadastro} Contrato comercial ativo ligando Parceiro de Negócio à Unidade Consumidora (UC) [cite: 133].
*   [do-134-unidade-consumidora-uc.md](/data-objects/structured/do-134-unidade-consumidora-uc.md) - {Cadastro} Unidades de consumo faturáveis (código único de 15 dígitos) da BDGD [cite: 134].
*   [do-135-agente.md](/data-objects/structured/do-135-agente.md) - {CCEE} Registro cadastral de empresas geradoras/comercializadoras registradas na CCEE [cite: 135].
*   [do-136-conta-centralizada-de-liquidacao.md](/data-objects/structured/do-136-conta-centralizada-de-liquidacao.md) - {CCEE} Saldos de contas, adimplementos e garantias de liquidação do MCP [cite: 136].
*   [do-137-contrato-de-compra-e-venda.md](/data-objects/structured/do-137-contrato-de-compra-e-venda.md) - {CCEE} Contratos bilaterais físicos e de longo prazo (PPAs) homologados no SCL [cite: 137].
*   [do-138-contrato-de-reserva-cer.md](/data-objects/structured/do-138-contrato-de-reserva-cer.md) - {CCEE} Custos, encargos e repasses fiscais resultantes de energia de reserva (EER) [cite: 138].
*   [do-139-garantia-fisica.md](/data-objects/structured/do-139-garantia-fisica.md) - {CCEE} Capacidade máxima comercializável homologada e lastro contábil do gerador [cite: 139].
*   [do-140-posicao-mensal.md](/data-objects/structured/do-140-posicao-mensal.md) - {CCEE} Diferença lógica e exposições multilaterais a liquidar ao PLD no curto prazo [cite: 140].
*   [do-141-preco-de-liquidacao-das-diferencas-pld.md](/data-objects/structured/do-141-preco-de-liquidacao-das-diferencas-pld.md) - {CCEE} Preço spot horário publicado pela CCEE por submercado de energia [cite: 141].
*   [do-142-resposta-de-demanda-rd.md](/data-objects/structured/do-142-resposta-de-demanda-rd.md) - {CCEE} Ofertas de redução voluntária de consumo para fins de segurança (ONS) [cite: 142].
*   [do-143-venda-de-excedentes-mcsd-mve.md](/data-objects/structured/do-143-venda-de-excedentes-mcsd-mve.md) - {CCEE} Cessões de energia excedente e sobras contratuais entre distribuidoras [cite: 143].
*   [do-144-fatura-conta-de-energia.md](/data-objects/structured/do-144-fatura-conta-de-energia.md) - {Faturamento} Conta de luz detalhando consumo ativo/reativo, TE, TUSD e GD [cite: 144].
*   [do-145-leitura-de-medicao.md](/data-objects/structured/do-145-leitura-de-medicao.md) - {Medição} Curvas de leitura brutas higienizadas e validadas por motor de regras VEE [cite: 145].
*   [do-146-medidor.md](/data-objects/structured/do-146-medidor.md) - {Medição} Cadastro de medidores de energia físicos de campo (Poste, Unidade de Consumo) [cite: 146].
*   [do-147-contrato-de-comercializacao.md](/data-objects/structured/do-147-contrato-de-comercializacao.md) - {CCEE} Instrumento de formalização de comercialização síncrona no mercado livre [cite: 147].
*   [do-148-medicao-para-faturamento-smf.md](/data-objects/structured/do-148-medicao-para-faturamento-smf.md) - {CCEE} Dados brutos SCDE ("caixa registradora" de MWh de usinas) [cite: 148].
*   [do-149-preco-de-liquidacao-das-diferencas.md](/data-objects/structured/do-149-preco-de-liquidacao-das-diferencas.md) - {CCEE} Preço de liquidação spot de curto prazo em bases horárias [cite: 149].
*   [do-150-resultado-da-liquidacao-mcp.md](/data-objects/structured/do-150-resultado-da-liquidacao-mcp.md) - {CCEE} Resultado financeiro final multilateral (débito/crédito) homologado [cite: 150].
*   [do-151-ativo-fixo-contabil.md](/data-objects/structured/do-151-ativo-fixo-contabil.md) - {Finanças} Ativos fixos e imobilizados contábeis (IFRS) criados em FI-AA [cite: 151].
*   [do-152-ativo-regulatorio-brr.md](/data-objects/structured/do-152-ativo-regulatorio-brr.md) - {Finanças} Cadastro e valorização de ativos na Base de Remuneração Regulatória (BRR) da ANEEL [cite: 152].
*   [do-153-business-partner.md](/data-objects/structured/do-153-business-partner.md) - {Suporte} Unifica o cadastro mestre de clientes, fornecedores e parceiros comerciais no ERP [cite: 153].
*   [do-154-centro-de-custo.md](/data-objects/structured/do-154-centro-de-custo.md) - {Finanças} Centro de custo CO para apropriação e rateio das despesas operacionais OPEX [cite: 154].
*   [do-155-centro-de-lucro.md](/data-objects/structured/do-155-centro-de-lucro.md) - {Finanças} Rastreia receitas e resultados por segmentos de negócio do grupo (G, T, D, C) [cite: 155].
*   [do-156-contas-a-pagar.md](/data-objects/structured/do-156-contas-a-pagar.md) - {Finanças} Títulos de obrigações financeiras com fornecedores e terceiros (FI-AP) [cite: 156].
*   [do-157-contas-a-receber.md](/data-objects/structured/do-157-contas-a-receber.md) - {Finanças} Contas a receber lógicas geradas pelo faturamento síncrono comercial e trading [cite: 157].
*   [do-158-entidade-legal.md](/data-objects/structured/do-158-entidade-legal.md) - {Finanças} Cadastro societário legal das subsidiárias com Company Code mapeados em SAP [cite: 158].
*   [do-159-fiscal-period.md](/data-objects/structured/do-159-fiscal-period.md) - {Finanças} Períodos fiscais ordinários e especiais para fechamentos periódicos [cite: 159].
*   [do-160-lancamento-contabil.md](/data-objects/structured/do-160-lancamento-contabil.md) - {Finanças} Registro contábil e apropriações salvas no Diário Universal ACDOCA [cite: 160].
*   [do-161-plano-de-contas.md](/data-objects/structured/do-161-plano-de-contas.md) - {Finanças} Plano de contas societário unificado integrado ao Plano de Contas Auxiliar da ANEEL [cite: 161].
*   [do-162-programa.md](/data-objects/structured/do-162-programa.md) - {Finanças} Estruturas hierárquicas de agrupamentos lógicos de investimentos em CAPEX [cite: 162].
*   [do-163-wbs-element.md](/data-objects/structured/do-163-wbs-element.md) - {Finanças} Elemento PEP do SAP PS para acumulação de custos em projetos físicos de rede [cite: 163].
*   [do-164-projeto-de-investimento.md](/data-objects/structured/do-164-projeto-de-investimento.md) - {Finanças} Projeto estruturado de capital que gerencia a expansão física de subestações [cite: 164].
*   [do-165-colaboradores-externos.md](/data-objects/structured/do-165-colaboradores-externos.md) - {RH} Cadastro de pessoal terceirizado e empreiteiras de campo (Fieldglass) [cite: 165].
*   [do-166-funcionario.md](/data-objects/structured/do-166-funcionario.md) - {RH} Mestre de empregados clt ativos com dados organizacionais de reporte (SuccessFactors) [cite: 166].
*   [do-167-time.md](/data-objects/structured/do-167-time.md) - {RH} Grupos funcionais, gerências e squads operacionais da holding e regionais [cite: 167].
*   [do-168-fornecedor.md](/data-objects/structured/do-168-fornecedor.md) - {Suprimentos} Cadastro mestre de dados fiscais e certidões negativas de fornecedores homologados [cite: 168].
*   [do-169-invoice.md](/data-objects/structured/do-169-invoice.md) - {Suprimentos} Faturas enviadas por fornecedores para conciliação física de 3 vias (Coupa/SAP) [cite: 169].
*   [do-170-mestre-de-materiais.md](/data-objects/structured/do-170-mestre-de-materiais.md) - {Suprimentos} Catálogo corporativo de materiais e componentes técnicos regulados de rede (TUC) [cite: 170].
*   [do-171-pedido-de-compra.md](/data-objects/structured/do-171-pedido-de-compra.md) - {Suprimentos} Pedido de compra MM que formaliza e emite a obrigação com o fornecedor [cite: 171].
*   [do-172-purchase-order.md](/data-objects/structured/do-172-purchase-order.md) - {Suprimentos} Pedido de Compra (PO Number) gerado e enviado de forma síncrona [cite: 172].
*   [do-173-purchase-requisition.md](/data-objects/structured/do-173-purchase-requisition.md) - {Suprimentos} Requisições internas (PR Number) de compras de sobressalentes [cite: 173].
*   [do-174-artigo-de-solucao.md](/data-objects/structured/do-174-artigo-de-solucao.md) - {TI} Base de erros conhecidos, runbooks de TI/TO e guias de troubleshooting (ServiceNow) [cite: 174].
*   [do-175-ativo-de-ti-asset.md](/data-objects/structured/do-175-ativo-de-ti-asset.md) - {TI} Ciclo de vida financeiro, garantias e licenças de software e computadores [cite: 175].
*   [do-176-item-de-configuracao-ci.md](/data-objects/structured/do-176-item-de-configuracao-ci.md) - {TI} Itens do CMDB convergente (servidores SCADA, religadores, PLCs) [cite: 176].
*   [do-177-item-de-servico.md](/data-objects/structured/do-177-item-de-servico.md) - {TI} Itens pré-aprovados do catálogo de solicitação de acessos e recursos de rede [cite: 177].
*   [do-178-lancamento-release.md](/data-objects/structured/do-178-lancamento-release.md) - {TI} Coordenação e empacotamento de novos patches de segurança em sistemas industriais [cite: 178].
*   [do-179-mudanca-change.md](/data-objects/structured/do-179-mudanca-change.md) - {TI} Workflows de mudanças aprovadas (RFC) para mitigar riscos de apagões sistêmicos [cite: 179].
*   [do-180-problema-problem.md](/data-objects/structured/do-180-problema-problem.md) - {TI} Análise de causa raiz (RCA) sobre incidentes repetitivos na telemetria [cite: 180].
*   [do-181-ticket-incidente-requisicao-de-servico.md](/data-objects/structured/do-181-ticket-incidente-requisicao-de-servico.md) - {TI} Chamados individuais de TI/TO (incidentes ou requisições de acessos) [cite: 181].

---

## 2. Diretrizes de Governança de Dados (LeanIX v4 & OKF v0.1)

De acordo com as boas práticas de Arquitetura de Dados aplicadas ao setor de utilidades elétricas:

1.  **Abstração Enxuta (Breadth over Depth):** Modelamos dados conceitualmente em uma hierarquia simples de até 2 níveis (Domínio -> Objeto de Dados lógicos) para evitar a complexidade cadastral e custos de manutenção insustentáveis.
2.  **Único Sistema da Verdade (SOT):** Cada objeto de dados importante possui um único sistema proprietário encarregado de sua gravação mestre com a relação de escrita/criação ("Provides" ou "Writes" em SAP LeanIX), atuando as demais aplicações em modo de consumo ("Consumes" ou Leitura).
3.  **Estabilidade Temporal de Negócio:** Os termos de negócio (como *Unidade Consumidora* ou *Fatura*) permanecem os mesmos ao longo do tempo, independentemente de trocas físicas ou atualizações em sistemas core (como a transição do SAP ECC para o SAP S/4HANA Cloud).
4.  **Enquadramento de Risco e Segurança (LGPD):** Os objetos estão marcados de acordo com os níveis de sensibilidade para garantir conformidade em estudos de segurança (DORA e REN ANEEL 964).
