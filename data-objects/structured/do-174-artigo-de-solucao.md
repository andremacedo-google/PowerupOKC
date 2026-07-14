---
id: DO-174
name: "Artigo de Solução"
type: "Data Object"
subtype: "Conceptual Data Object"
lifecycle:
  status: "Active"
  startDate: "2026-01-01"
dataSensitivity: "Interno"
tags:
  - "Setor Elétrico"
  - "Governança de Dados"
  - "Nível 3"
  - "Corporativo"
  - "Tecnologia da Informação"
  - "LeanIX-v4"
---

# Artigo de Solução (DO-174)

Este Fact Sheet de **Data Object** descreve conceitualmente a estrutura, responsabilidade e governança do objeto de dados **Artigo de Solução** no ecossistema de informações do Setor Elétrico Brasileiro. Ele atua como elemento unificado do metamodelo SAP LeanIX v4.

## 1. Escopo de Negócio e Descrição
Documento de conhecimento estruturado contendo erros conhecidos, soluções de contorno (workarounds), guias de 'como fazer' (how-to) e procedimentos padrão. Utilizado contextualmente por analistas de TI/TO e operadores (como COD/COG) para acelerar a resolução de incidentes e promover o autoatendimento corporativo.

Este objeto de dados é fundamental para a governança e conformidade com as regras operacionais da ANEEL, do ONS ou da CCEE, garantindo a estabilidade operacional e o compliance contínuo das interfaces de integração entre TI e TO.

## 2. Relações no Metamodelo LeanIX

Para fins de rastreabilidade e análise de impacto, o objeto de dados possui as seguintes conexões lógicas:

*   **Subdomínio de Dados (Nível 1):** Corporativo / Tecnologia da Informação
*   **Sistemas e Aplicações que Manipulam (Applications):** ServiceNow Knowledge Management, Confluence, Jira Service Management Knowledge Base
*   **Sistema de Registro Canônico (System of Truth):** ServiceNow (Base de Conhecimento Central)

## # Schema

Este barramento conceitual é estruturado através dos seguintes campos mestre e tipos de dados correspondentes:

| Campo do Barramento | Tipo de Dado | Descrição Funcional e Regras de Negócio |
|---|---|---|
| `ID do Artigo` | String (ID) | Atributo técnico representando o campo mestre 'ID do Artigo'. |
| `Título do Artigo` | String | Atributo técnico representando o campo mestre 'Título do Artigo'. |
| `Categoria de Conhecimento` | String | Atributo técnico representando o campo mestre 'Categoria de Conhecimento'. |
| `Conteúdo do Artigo` | String | Atributo técnico representando o campo mestre 'Conteúdo do Artigo'. |
| `Palavras-chave / Tags` | String | Atributo técnico representando o campo mestre 'Palavras-chave / Tags'. |
| `Status de Aprovação (Rascunho` | String (Enum) | Atributo técnico representando o campo mestre 'Status de Aprovação (Rascunho'. |
| `Em Revisão` | String | Atributo técnico representando o campo mestre 'Em Revisão'. |
| `Publicado)` | String | Atributo técnico representando o campo mestre 'Publicado)'. |
| `Data de Validade` | String (ID) | Atributo técnico representando o campo mestre 'Data de Validade'. |
| `Autor (ID do Funcionário)` | String (ID) | Atributo técnico representando o campo mestre 'Autor (ID do Funcionário)'. |
| `Avaliação de Utilidade (Visualizações / Feedbacks)` | String (ID) | Atributo técnico representando o campo mestre 'Avaliação de Utilidade (Visualizações / Feedbacks)'. |
| `Problema (Problem) Relacionado.` | String | Atributo técnico representando o campo mestre 'Problema (Problem) Relacionado.'. |

## # Examples

Abaixo está detalhado um exemplo prático de payload estruturado que representa o objeto de dados trafegado em tempo real ou em lote nas integrações:

```json
{
  "id_do_artigo": "REF-DO-174-001",
  "titulo_do_artigo": "Dados de Exemplo",
  "categoria_de_conheci": "Dados de Exemplo",
  "conteudo_do_artigo": "Dados de Exemplo",
  "palavras_chave_tags": "Dados de Exemplo"
}
```

## # Citations

1. Gestão de Conhecimento (KCS / ITIL v4), Processo de Capacitação e Autoatendimento de Equipes de TI/TO.
2. [SAP LeanIX - Data Object Modeling Guidelines](https://www.leanix.net/) - Padrões de modelagem de objetos de dados corporativos integrados ao metamodelo de arquitetura.
