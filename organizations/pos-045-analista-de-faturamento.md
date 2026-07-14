---
id: "POS-045"
name: "Analista de Faturamento"
type: "Position"
subtype: "Subscription Role"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Restrito (LGPD)"
tags:
  - "Distribuidora"
  - "Faturamento"
  - "Operacional"
  - "Setor Elétrico"
  - "LeanIX-v4"
---

# Analista de Faturamento (ID: POS-045)

Este Fact Sheet de **Position** descreve conceitualmente a estrutura, responsabilidade, atribuições e sistemas integrados associados à posição típica de **Analista de Faturamento** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
O cargo de **Analista de Faturamento** desempenha um papel central dentro da área funcional da companhia. No contexto do setor elétrico brasileiro, esta posição é fundamental para garantir a estabilidade operacional, conformidade regulatória com as normas da ANEEL, CCEE ou do ONS, e apoiar a transição e automação de processos.

## 2. Atividades e Responsabilidades Principais
*   Executar processos em lote de faturamento elétrico, aplicar tarifas homologadas, auditar exceções de leitura de medidores.
*   Colaboração síncrona com equipes internas para mitigação de riscos regulatórios e operacionais.
*   Zelar pela integridade das transações e segurança das informações no dia a dia técnico-comercial.

## 3. Relações no Metamodelo LeanIX (Who/How/What)

Para fins de rastreabilidade de governança e segurança, o cargo possui as seguintes conexões lógicas no metamodelo:

*   **Organização de Pertencimento (Parent Team/BU):** [/organizations/teams/team-departamento-faturamento.md](Departamento de Faturamento)
*   **Sistemas e Aplicações Utilizados (How):** SAP IS-U
*   **Papel de Governança (Subscription Role):** Responsible / Technical Contact

## 4. Diretrizes de Treinamento e Segurança (Compliance)
*   **Conformidade de Acesso:** O acesso aos dados e sistemas deve respeitar estritamente a política de segurança de privilégios mínimos.
*   **Segurança Física e Lógica:** Treinamento obrigatório nas normas regulamentadoras aplicáveis ao escopo do cargo (ex: NR-10 para campo, ou políticas de sigilo para mesa de trading).
*   **Proteção de Dados:** Conformidade rígida com as diretrizes da LGPD para manuseio de dados de consumo e cadastrais de clientes.

## # Citations

1. [Manual de Governança Organizacional PowerupOKC] - Estabelece as regras de classificação de cargos, atribuições e papéis de subscrição corporativos.
2. [SAP LeanIX - Organization and Subscription Guidelines](https://www.leanix.net/) - Padrões de modelagem para gerenciamento de posições integradas ao metamodelo de arquitetura empresarial.
