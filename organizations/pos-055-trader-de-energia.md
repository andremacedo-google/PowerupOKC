---
id: "POS-055"
name: "Trader de Energia"
type: "Position"
subtype: "Subscription Role"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Confidencial"
tags:
  - "Comercializadora"
  - "Trading"
  - "Operacional"
  - "Setor Elétrico"
  - "LeanIX-v4"
---

# Trader de Energia (ID: POS-055)

Este Fact Sheet de **Position** descreve conceitualmente a estrutura, responsabilidade, atribuições e sistemas integrados associados à posição típica de **Trader de Energia** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
O cargo de **Trader de Energia** desempenha um papel central dentro da área funcional da companhia. No contexto do setor elétrico brasileiro, esta posição é fundamental para garantir a estabilidade operacional, conformidade regulatória com as normas da ANEEL, CCEE ou do ONS, e apoiar a transição e automação de processos.

## 2. Atividades e Responsabilidades Principais
*   Negociar e fechar contratos bilaterais de compra e venda física/futura de energia elétrica no mercado livre (ACL).
*   Colaboração síncrona com equipes internas para mitigação de riscos regulatórios e operacionais.
*   Zelar pela integridade das transações e segurança das informações no dia a dia técnico-comercial.

## 3. Relações no Metamodelo LeanIX (Who/How/What)

Para fins de rastreabilidade de governança e segurança, o cargo possui as seguintes conexões lógicas no metamodelo:

*   **Organização de Pertencimento (Parent Team/BU):** [/organizations/teams/team-mesa-trading.md](Mesa de Operações (Trading))
*   **Sistemas e Aplicações Utilizados (How):** ETRM, BBCE Portal
*   **Papel de Governança (Subscription Role):** Responsible / Technical Contact

## 4. Diretrizes de Treinamento e Segurança (Compliance)
*   **Conformidade de Acesso:** O acesso aos dados e sistemas deve respeitar estritamente a política de segurança de privilégios mínimos.
*   **Segurança Física e Lógica:** Treinamento obrigatório nas normas regulamentadoras aplicáveis ao escopo do cargo (ex: NR-10 para campo, ou políticas de sigilo para mesa de trading).
*   **Proteção de Dados:** Conformidade rígida com as diretrizes da LGPD para manuseio de dados de consumo e cadastrais de clientes.

## # Citations

1. [Manual de Governança Organizacional PowerupOKC] - Estabelece as regras de classificação de cargos, atribuições e papéis de subscrição corporativos.
2. [SAP LeanIX - Organization and Subscription Guidelines](https://www.leanix.net/) - Padrões de modelagem para gerenciamento de posições integradas ao metamodelo de arquitetura empresarial.
