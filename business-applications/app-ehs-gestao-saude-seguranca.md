---
id: AP-006
name: "EHS - Gestão de Saúde, Segurança e Meio Ambiente"
type: "Application"
subtype: "Business Application"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
businessCriticality: "Business Critical"
functionalSuitability: "Excellent"
technicalSuitability: "Excellent"
tags:
  - "Setor Elétrico"
  - "Corporativo"
  - "LeanIX-v4"
---

# EHS - Gestão de Saúde, Segurança e Meio Ambiente (ID: AP-006)

Este Fact Sheet de **Business Application** descreve no padrão de arquitetura empresarial da **SAP LeanIX v4** o escopo de atuação e barramento de dados do sistema **EHS - Gestão de Saúde, Segurança e Meio Ambiente** [13, 33]. Ele atua como um pilar fundamental da camada de aplicação e dados da companhia, estruturando as operações no Setor Elétrico Brasileiro [13, 34].

## 1. Escopo Técnico e de Negócio
No contexto das utilities de energia e da transição energética regulada pelas agências setoriais (como ANEEL e ONS), esta aplicação desempenha o papel de:
*   **Sistema para gestão de saúde ocupacional, conformidade ambiental (condicionantes de licenças de usinas/linhas) e gestão de permissões de trabalho (PT) de alto risco de eletricistas de campo.** [33, 438]

Ela é projetada para manter a consistência lógica, automatizar workflows operacionais síncronos e reduzir atritos nos processos core de negócios [34, 439].

## 2. Integrações e Fluxo de Dados (Data Objects)
No barramento de integração corporativo de TI/OT, esta aplicação atua como **System of Truth (SOT)** canônico ou consumidora nos seguintes fluxos de dados mestre [31, 456]:

*   **Inputs (Dados de Entrada consumidos):**
    *   `[/data-objects/do-014-resoluções-e-diretrizes-da-aneel.md](DO-014 Resoluções e Diretrizes da ANEEL)` [31, 34]
*   **Outputs (Dados de Saída fornecidos ou gravados):**
    *   `[/data-objects/do-017-logs-de-redes-e-acessos-incidentes-de-segurança-e-condicionantes-ambientais.md](DO-017 Logs de Redes e Acessos (Incidentes de Segurança e Condicionantes Ambientais))` [31, 34]

## 3. Capacidades de Negócio Suportadas
Este sistema apoia e habilita tecnologicamente a execução operacional das seguintes capacidades estratégicas de Nível 3 [21, 129]:
*   `[/business-capabilities/cap-l3-conformidade-regulatoria.md](Conformidade Regulatoria)` [21, 129]

## 4. Exemplos de Soluções e Tecnologias de Mercado
Como parte das melhores práticas da SAP LeanIX v4, o nome desta aplicação é desacoplado de marcas comerciais. Os principais pacotes de software COTS líderes de mercado que implementam este escopo de negócio são [35, 338]:
*   **SAP S/4HANA EHS, Intelex Environmental, Cority EHS** [35, 338]

## 5. Práticas de Governança e FinOps
*   **Modelagem de Hierarquias (LeanIX):** Recomenda-se modelar esta aplicação em nível lógico de Nível 1, estruturando seus módulos operacionais como filhos lógicos de Nível 2 apenas quando houver necessidade explícita de controle orçamentário segregado [43].
*   **FinOps & Licenciamento:** O monitoramento de custos de computação em nuvem deve isolar e alocar o consumo transacional de alto volume (como barramentos de mensageria de telemetria ou faturamento em massa) em relação aos fluxos de processamento administrativo sob o modelo de tags do provedor [49].
*   **Conformidade & Segurança:** A conformidade com a LGPD e as normas de cibersegurança da ANEEL (REN 964) exige criptografia ativa em repouso e em trânsito (AES-256 e TLS 1.3) para dados classificados como Restritos ou Confidenciais [152].

---

## # Citations
1. [SAP LeanIX - Best Practices Application Modeling Guidelines](https://www.leanix.net/) - Guia oficial de governança de Fact Sheets e modelagem enxuta do metamodelo v4.
2. [Procedimentos e Regras do Setor Elétrico Brasileiro] - Regulamentações de conformidade técnica e faturamento comercial.
