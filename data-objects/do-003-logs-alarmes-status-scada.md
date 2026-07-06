---
id: DO-003
name: "Logs de Alarmes e Status (SCADA)"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Confidencial (Infraestrutura Crítica)"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Operações"
  - "LeanIX-v4"
---

# Logs de Alarmes e Status (SCADA) (ID: DO-003)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Logs de Alarmes e Status (SCADA)** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Mensagens de eventos industriais síncronos e telemetria síncrona contendo o estado físico de dispositivos de manobra (aberto/fechado), proteções e alarmes de subestações de alta/média tensão.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, da CCEE e as regras nacionais de segurança da informação e privacidade de dados (LGPD), garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Capacidades de Negócio que Consomem/Produzem (Business Capabilities N3):**
    *   [/cap-l3-operacao-da-rede-de-distribuicao](Capacidade Operacao Da Rede De Distribuicao)
    *   [/cap-l3-operacao-do-sistema-de-transmissao](Capacidade Operacao Do Sistema De Transmissao)
*   **Sistemas e Aplicações que Manipulam (Applications):**
    *   [/applications/app-adms-gestao-redes-distribuicao](Aplicação Adms Gestao Redes Distribuicao)
    *   [/applications/app-gis-georreferenciamento-redes](Aplicação Gis Georreferenciamento Redes)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `id_ponto_scada` | String | Identificador único do ponto de dados no protocolo de TO (ex: DNP3/IEC 104 address). |
| `timestamp_evento` | DateTime (ISO 8601) | Data, hora e milissegundo exato do disparo ou variação do ponto de telemetria. |
| `status_dispositivo` | String (Enum) | Estado operativo do equipamento (ABERTO, FECHADO, TRANSICAO, FALHA). |
| `valor_analogico_kv` | Float | Leitura analógica em tempo real de tensão medida no barramento. |
| `alarme_critico` | Boolean | Sinalizador ativo em caso de sobrecorrente, atuação de relé de proteção ou temperatura crítica. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_ponto_scada": "BFA_SE_LESTE_CB_52_1",
  "timestamp_evento": "2026-07-06T14:15:02.124Z",
  "status_dispositivo": "ABERTO",
  "valor_analogico_kv": 13.78,
  "alarme_critico": true
}
```

## # Citations

1. [Manual de Governança de Dados PowerupOKC] - Estabelece as regras de classificação de segurança e sensibilidade das informações corporativas e reguladas.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
