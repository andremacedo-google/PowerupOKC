---
id: DO-216
name: "Procedimentos Operacionais Padrão (POPs) e Instruções de Trabalho (ITs)"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Interno"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Não Estruturado"
  - "LeanIX-v4"
---

# Procedimentos Operacionais Padrão (POPs) e Instruções de Trabalho (ITs) (DO-216)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança da base de conhecimento não estruturada **Procedimentos Operacionais Padrão (POPs) e Instruções de Trabalho (ITs)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Documentos granulares que orientam os eletricistas e técnicos de campo sobre como realizar tarefas operacionais com segurança técnica e eficácia, seguindo as normas regulamentadoras.

Este objeto de dados não estruturado é de extrema importância para as regras de conformidade regulatória (conforme as diretrizes de regulação tarifária, fiscalização ou as instruções operacionais do SIN). Sua correta catalogação impede silos de conhecimento e vazamentos de informações classificadas.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade, linhagem e governança de dados no repositório corporativo da PowerUp, este Data Object mantém as seguintes conexões estáveis:

*   **Subdomínio de Dados (Nível 1):** Técnico e Operacional / Operações de Campo
*   **Sistemas e Aplicações Relacionadas (Applications):** WFM (Mobile), SAP PM, SharePoint de Segurança (EHS)
*   **Repositório/Sistema de Registro Canônico (System of Truth):** Departamento de Manutenção de Campo (Engenharia e EHS)
*   **Capacidade de Negócio Relacionada:** Serviços Técnicos de Campo, Manutenção Preventiva/Corretiva de Redes
*   **Documento de Referência (Mestre):** sim

## # Schema

Este ativo de dados não estruturados de referência é composto e regido pelos seguintes temas críticos e tipos de informações:

*   **Informações Críticas e Conteúdo Típico:** Checklists de segurança de EPIs/EPCs, sequência física de desenergização e aterramento (regras de ouro), procedimentos de substituição de transformadores, religação e manobras locais.
*   **Classificação de Privacidade e Sensibilidade (Compliance/LGPD):** Interno

## # Examples

Abaixo está exemplificado um rascunho de metadados em formato estruturado representando o objeto documental, indicando as variáveis comumente contidas em seu fluxo de indexação:

```json
{"pop_manutencao_substituicao_trafo": {"procedimento_id": "POP-MT-042", "passos_seguranca": ["Abertura da chave fusível e seccionadora lateral", "Verificação de ausência de tensão na média tensão", "Instalação de conjunto de aterramento temporário rápido (regras de ouro)"]}}
```

## # Citations

1. [Manual de Governança de Informações Não Estruturadas PowerupOKC] - Rege os padrões de indexação, controle e privacidade das bases de conhecimento setoriais.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
