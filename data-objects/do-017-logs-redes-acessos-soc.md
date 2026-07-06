---
id: DO-017
name: "Logs de Redes e Acessos (SOC)"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Confidencial"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Corporativo"
  - "LeanIX-v4"
---

# Logs de Redes e Acessos (SOC) (ID: DO-017)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Logs de Redes e Acessos (SOC)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Histórico de acessos a servidores corporativos (TI) e fluxos de dados de switches de subestações de alta tensão (OT).

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, da CCEE e as regras nacionais de segurança da informação e privacidade de dados (LGPD), garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Capacidades de Negócio que Consomem/Produzem (Business Capabilities N3):**
    *   [/cap-l3-seguranca-cibernetica-tiot](Capacidade Seguranca Cibernetica Tiot)
    *   [/cap-l3-gestao-de-infraestrutura-e-operacoes-de-ti](Capacidade Gestao De Infraestrutura E Operacoes De Ti)
*   **Sistemas e Aplicações que Manipulam (Applications):**
    *   [/applications/app-grc-governanca-riscos](Aplicação Grc Governanca Riscos)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `id_log_evento` | String | ID exclusivo gerado pelo sistema de auditoria SIEM/SOC. |
| `ip_origem` | String | Endereço IP da máquina ou ponto que realizou a chamada de rede. |
| `usuario_autenticado` | String | ID do usuário do Active Directory que executou o login ou comando. |
| `severidade_risco` | String (Enum) | Criticidade do incidente de segurança (BAIXO, MEDIO, ALTO, CRITICO). |
| `mensagem_log` | Text | Texto descritivo técnico bruto do evento contido no log corporativo. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_log_evento": "EV-SOC-2026-99221",
  "ip_origem": "192.168.42.105",
  "usuario_autenticado": "USR_SCADA_OP_04",
  "severidade_risco": "ALTO",
  "mensagem_log": "Tentativa de login síncrono bem-sucedida em porta SCADA protegida fora do horário comercial habitual..."
}
```

## # Citations

1. [Manual de Governança de Dados PowerupOKC] - Estabelece as regras de classificação de segurança e sensibilidade das informações corporativas e reguladas.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
