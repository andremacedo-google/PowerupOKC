---
id: AP-003
name: "HRIS - Sistema de Informações de Recursos Humanos"
type: "Application"
subtype: "Business Application"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
businessCriticality: "Business Critical"
functionalSuitability: "Excellent"
technicalSuitability: "Adequate"
tags:
  - "Setor Elétrico"
  - "Corporativo"
  - "Recursos Humanos"
  - "NR10"
  - "LeanIX-v4"
---

# HRIS - Sistema de Informações de Recursos Humanos (ID: AP-003)

O sistema de **Human Resources Information System (HRIS)** é responsável pela gestão unificada do ciclo de vida do colaborador corporativo e das equipes de campo no setor de utilidade elétrico.

## 1. Escopo Técnico e de Negócio
No setor elétrico, esta aplicação possui um papel de alta criticidade operacional, pois gerencia o cadastro de habilidades e as certificações técnicas obrigatórias de segurança (como as normas regulamentadoras **NR10**, **NR35** e **NR12**) necessárias para que eletricistas e engenheiros realizem manutenções em subestações e linhas energizadas [353]. Ele gerencia o recrutamento, onboarding, remuneração, benefícios e folha de pagamento.

## 2. Integrações e Fluxo de Dados (Data Objects)
*   **Inputs (Dados de Entrada):**
    *   `DO-015 Currículos e Perfis`: Dados cadastrais e acadêmicos de candidatos a vagas técnicas e operacionais.
*   **Outputs (Dados de Saída):**
    *   `DO-015 Currículos e Perfis (Registro do Colaborador)`: Dados mestre do empregado, cargo e centro de custo integrados ao ERP [353].
    *   `DO-016 Políticas de Benefícios`: Emissão de checklists de elegibilidade de planos de previdência e reembolsos corporativos.

## 3. Capacidades de Negócio Suportadas
*   `cap-l3-aquisicao-de-talentos` [338]
*   `cap-l3-desenvolvimento-e-treinamento` [338]
*   `cap-l3-remuneracao-e-beneficios` [338]

## 4. Exemplos de Soluções e Tecnologias de Mercado
*   **SAP SuccessFactors**: Plataforma amplamente adotada para gestão integrada de talentos, competências de segurança de campo e Employee Central [353].
*   **Workday Human Capital Management (HCM)**: Solução SaaS global para gestão unificada de RH.

## 5. Práticas de Governança e FinOps
*   **Conformidade LGPD:** Como processa PII (Personally Identifiable Information) de funcionários, possui regras restritas de acesso controlado baseado em papéis (RBAC).
