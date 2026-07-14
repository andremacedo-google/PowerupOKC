---
id: DO-220
name: "Contratos de Uso (CUST/CUSD) e Conexão (CCT/CCD)"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Confidencial"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Não Estruturado"
  - "LeanIX-v4"
---

# Contratos de Uso (CUST/CUSD) e Conexão (CCT/CCD) (DO-220)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança da base de conhecimento não estruturada **Contratos de Uso (CUST/CUSD) e Conexão (CCT/CCD)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Contratos jurídicos que regulam a conexão física e o uso das redes elétricas de transmissão (Rede Básica) ou distribuição entre o agente (usina ou consumidor) e o operador (ONS ou distribuidora).

Este objeto de dados não estruturado é de extrema importância para as regras de conformidade regulatória (conforme as diretrizes de regulação tarifária, fiscalização ou as instruções operacionais do SIN). Sua correta catalogação impede silos de conhecimento e vazamentos de informações classificadas.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade, linhagem e governança de dados no repositório corporativo da PowerUp, este Data Object mantém as seguintes conexões estáveis:

*   **Subdomínio de Dados (Nível 1):** Jurídico e Contratual / Contratos de Concessão e Uso
*   **Sistemas e Aplicações Relacionadas (Applications):** SAP CLM, GED Regulatório, ONS (Módulo 8), CIS (Faturamento)
*   **Repositório/Sistema de Registro Canônico (System of Truth):** Arquivo de Contratos Regulatórios / SAP CLM
*   **Capacidade de Negócio Relacionada:** Acesso ao Sistema de Geração/Transmissão, Faturamento de Serviços de Rede
*   **Documento de Referência (Mestre):** nao

## # Schema

Este ativo de dados não estruturados de referência é composto e regido pelos seguintes temas críticos e tipos de informações:

*   **Informações Críticas e Conteúdo Típico:** Montante de Uso do Sistema (MUST/MUSD) contratado em kW, tarifas reguladas aplicáveis (TUSD/TUST), direitos de conexão, ponto físico de entrega e penalidades por ultrapassagem.
*   **Classificação de Privacidade e Sensibilidade (Compliance/LGPD):** Confidencial

## # Examples

Abaixo está exemplificado um rascunho de metadados em formato estruturado representando o objeto documental, indicando as variáveis comumente contidas em seu fluxo de indexação:

```json
{"cusd_contrato_exemplo": {"partes": ["Distribuição Energia S.A.", "Grande Consumidor Industrial X"], "musd_contratado_kw": 5000, "ponto_de_entrega": "Subestação Leste 13.8kV"}}
```

## # Citations

1. [Manual de Governança de Informações Não Estruturadas PowerupOKC] - Rege os padrões de indexação, controle e privacidade das bases de conhecimento setoriais.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
