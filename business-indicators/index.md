# Catálogo Unificado de Indicadores de Desempenho (Business Indicators)

Este arquivo de `index.md` funciona como o portal mestre de navegação e revelação progressiva (*progressive disclosure*) para o diretório `/business-indicators/` da **PowerUp OKC (Open Knowledge Catalog)**. Ele está estruturado estritamente de acordo com as especificações do padrão **Open Knowledge Format (OKF) v0.1** [cite: 18].

Em total conformidade com as regras do metamodelo da **SAP LeanIX v4**, todas as **25 especificações lógicas de indicadores** (IDs `IND-001` a `IND-025`) estão hospedadas de forma plana nesta mesma pasta, sem qualquer divisão física em subpastas [cite: 13, 24]. Este índice mapeia as métricas finalísticas corporativas e de Tecnologia da Operação (TO) que qualificam e monitoram a performance das capacidades críticas do setor elétrico brasileiro (regulados pela ANEEL, ONS e CCEE) [cite: 8, 10, 11].

---

## 1. Qualidade e Continuidade do Serviço de Distribuição (ANEEL)
Indicadores e metas mensais e anuais exigidos pelos Procedimentos de Distribuição (PRODIST Módulo 8) para apurar os tempos e frequências de interrupções de energia elétrica aos consumidores finais [cite: 9, 11].

*   [ind-ind-001-dec.md](/business-indicators/ind-ind-001-dec.md) - (DEC) Duração Equivalente de Interrupção por Unidade Consumidora (limites da ANEEL) [cite: 9].
*   [ind-ind-002-fec.md](/business-indicators/ind-ind-002-fec.md) - (FEC) Frequência Equivalente de Interrupção por Unidade Consumidora (limites da ANEEL) [cite: 9].
*   [ind-ind-003-dic.md](/business-indicators/ind-ind-003-dic.md) - (DIC) Duração de Interrupção Individual sofrida por unidade consumidora [cite: 9].
*   [ind-ind-004-fic.md](/business-indicators/ind-ind-004-fic.md) - (FIC) Frequência de Interrupção Individual sofrida por unidade consumidora [cite: 9].
*   [ind-ind-005-dmic.md](/business-indicators/ind-ind-005-dmic.md) - (DMIC) Duração Máxima de uma única interrupção contínua individual [cite: 9].
*   [ind-ind-006-dicri.md](/business-indicators/ind-ind-006-dicri.md) - (DICRI) Duração de interrupção individual em Dia Crítico na distribuidora [cite: 9].
*   [ind-ind-007-dise.md](/business-indicators/ind-ind-007-dise.md) - (DISE) Duração de interrupção individual em Situação de Emergência oficial [cite: 9].
*   [ind-ind-012-fer.md](/business-indicators/ind-ind-012-fer.md) - (FER) Frequência equivalente de reclamações procedentes de clientes por 1.000 UCs [cite: 9, 11].
*   [ind-ind-013-der.md](/business-indicators/ind-ind-013-der.md) - (DER) Tempo médio de solução definitiva para reclamações comerciais [cite: 9, 11].
*   [ind-ind-014-ins.md](/business-indicators/ind-ind-014-ins.md) - (INS) Nível de serviço de teleatendimento de call center (atendimentos em até 30s) [cite: 9].

---

## 2. Qualidade do Produto e Níveis de Tensão (Distribuição)
Monitoramento estatístico de transgressões de níveis de tensão elétrica contratual em regime permanente, desbalanço trifásico e distorções de harmônicos (PRODIST Módulo 8) [cite: 9].

*   [ind-ind-008-drp.md](/business-indicators/ind-ind-008-drp.md) - (DRP) Duração relativa da transgressão de tensão de faixa precária (limite 3.0%) [cite: 9, 11].
*   [ind-ind-009-drc.md](/business-indicators/ind-ind-009-drc.md) - (DRC) Duração relativa da transgressão de tensão de faixa crítica (limite 0.5%) [cite: 9, 11].
*   [ind-ind-010-fd95.md](/business-indicators/ind-ind-010-fd95.md) - (FD95%) Fator de desbalanceamento de fases elétricas medido em barras e transformadores [cite: 9].
*   [ind-ind-011-dtt95.md](/business-indicators/ind-ind-011-dtt95.md) - (DTT95%) Distorção harmônica total acumulada da onda senoidal de tensão no SIN [cite: 9].

---

## 3. Operação, Confiabilidade e Desempenho de G&T (ONS)
Indicadores operativos que monitoram a estabilidade sistêmica da frequência do Sistema Interligado Nacional (SIN), taxas de disponibilidade e indisponibilidade de usinas, ampacidade térmica de LTs e pontualidade regulatória [cite: 10].

*   [ind-ind-018-dispf.md](/business-indicators/ind-ind-018-dispf.md) - (DISPF) Disponibilidade física ativa de unidades geradoras instaladas no SIN [cite: 10].
*   [ind-ind-019-teifa.md](/business-indicators/ind-ind-019-teifa.md) - (TEIFa) Taxa equivalente de indisponibilidade forçada (por falha) de geradores [cite: 10].
*   [ind-ind-020-teip.md](/business-indicators/ind-ind-020-teip.md) - (TEIP) Taxa equivalente de indisponibilidade programada (planejada) de geradores [cite: 10].
*   [ind-ind-021-disp_lt.md](/business-indicators/ind-ind-021-disp_lt.md) - (DISP_LT) Taxa de disponibilidade operativa de Linhas de Transmissão de alta tensão [cite: 10].
*   [ind-ind-022-ccat.md](/business-indicators/ind-ind-022-ccat.md) - (CCAT) Controle de sobrecarga e carregamento térmico de grandes transformadores [cite: 10].
*   [ind-ind-023-ccal.md](/business-indicators/ind-ind-023-ccal.md) - (CCAL) Controle de carregamento e ampacidade física de condutores de LTs [cite: 10].
*   [ind-ind-024-dfp.md](/business-indicators/ind-ind-024-dfp.md) - (DFP) Desempenho da frequência elétrica sistêmica em regime permanente (SIN) [cite: 10].
*   [ind-ind-025-pcpa.md](/business-indicators/ind-ind-025-pcpa.md) - (PCPA) Pontualidade das distribuidoras no cumprimento de providências pós-distúrbios [cite: 10].

---

## 4. Eficiência Comercial, Financeira e Perdas (CCEE / ANEEL)
Avaliação comparativa da qualidade das distribuidoras perante o ranking de continuidade anual da ANEEL, saúde financeira de arrecadação contra inadimplência de varejo e controle de perdas comerciais (furtos/desvios) [cite: 11].

*   [ind-ind-015-dgc.md](/business-indicators/ind-ind-015-dgc.md) - (DGC) Desempenho Global de Continuidade da distribuidora perante o ranking da ANEEL [cite: 11].
*   [ind-ind-016-inadimplencia.md](/business-indicators/ind-ind-016-inadimplencia.md) - (Inadimplência) Aging list de faturas em atraso contra o faturamento comercial bruto [cite: 11].
*   [ind-ind-017-perdas.md](/business-indicators/ind-ind-017-perdas.md) - (Perdas) Percentual de perdas não técnicas (fraudes e desvios) calculadas por balanço [cite: 11].

---

## 5. Diretrizes de Governança Integrada (Metamodelo LeanIX v4)
A integração desse portfólio de indicadores no SAP LeanIX v4 permite correlacionar o desempenho de negócios à eficácia tecnológica. Cada um dos 25 indicadores acima mapeia de forma síncrona [cite: 632]:

1.  **Business Capability (Nível 3):** A capacidade de negócio que o indicador qualifica e mede diretamente (ex: `[/business-capabilities/2-engajamento-cliente/cap-l3-gestao-de-perdas.md]`) [cite: 60, 622].
2.  **System of Truth (Application):** O sistema transacional core de TI/TO responsável pelo cálculo síncrono oficial (ex: `[/business-applications/app-mdm-gestao-medicao.md]`) [cite: 619, 632].
3.  **Ownership (Organization):** A equipe ou squad tática encarregada pelo acompanhamento e cumprimento do limite regulatório (ex: `[/organizations/teams/org-cod.md]`) [cite: 625, 628, 632].
4.  **Data Object (What):** Os objetos de dados de entrada que alimentam a série temporal do indicador (ex: `[/data-objects/structured/do-105-evento-de-interrupcao-dec-fec.md]`) [cite: 40, 632].

### # Referências Normativas
1.  **PRODIST Módulo 8 (Qualidade do Fornecimento de Energia Elétrica - ANEEL):** Estabelece os limites de DEC, FEC, DIC, FIC, DMIC, DRP e DRC das distribuidoras brasileiras.
2.  **Procedimentos de Rede do ONS (Submódulo 9.2 - Avaliação de Desempenho):** Dispõe sobre os critérios de cálculo de disponibilidade física (DISPF) e indisponibilidades (TEIFa, TEIP) de ativos elétricos do SIN.
3.  **Manual de Contabilidade do Setor Elétrico (MCSE - ANEEL):** Dispõe sobre o controle patrimonial, apropriação de despesas de O&M e unitização contábil regulatória na Base de Remuneração (BRR).
