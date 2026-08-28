# PROTOCOL.md: Ecossistema de Desenvolvimento Baseado em Habilidades (Skill-Driven Development)

**Languages:** [English](PROTOCOL.md) · [Русский](PROTOCOL_ru.md) · [العربية](PROTOCOL_ar.md) · [中文](PROTOCOL_zh.md) · [Deutsch](PROTOCOL_de.md) · [Español](PROTOCOL_es.md) · [Français](PROTOCOL_fr.md) · [日本語](PROTOCOL_ja.md) · [한국어](PROTOCOL_ko.md) · **Português**

## 1. Conceito e Filosofia

Este documento descreve a metodologia de desenvolvimento dentro do portfólio, adaptada para um ecossistema de agentes híbridos. O protocolo cobre todo o ciclo de vida do produto — desde o rascunho arquitetônico inicial até a geração final de artefatos de apresentação.

Princípio fundamental: **As decisões arquitetônicas devem ser explícitas, reproduzíveis e defensáveis.** Transicionamos de simplesmente escrever código para o **Desenvolvimento Baseado em Habilidades (Skill-Driven Development)**, onde as operações rotineiras, design, testes e análises são delegados a habilidades especializadas de agentes específicos.

---

## 2. Papéis e Distribuição de Habilidades

Três entidades principais e o ambiente de agentes unificado participam do processo. Seus papéis são estritamente separados e não se sobrepõem.

### 2.1. Developer (Humano)
O proprietário do produto. Tem a palavra final em cada ponto de decisão arquitetônica, aprova o escopo, define a direção do desenvolvimento e aceita as entregas dos agentes.

### 2.2. OpenCode (Implementador Autónomo)
O agente executor, operando no terminal com uma janela de contexto de até 1M de tokens. Responsável por escrever código, construir interfaces e gerar documentos e artefatos de mídia.
Possui o seguinte arsenal de habilidades:
*   **Engenharia e Código:** `code-review-skill`, `webapp-testing`, `mcp-builder`, `skill-creator`, `claude-api`.
*   **Design e Frontend:** `frontend-design`, `web-artifacts-builder`, `theme-factory`, `canvas-design`, `algorithmic-art`, `brand-guidelines`.
*   **Documentação e Escritório:** `build-project-docs`, `doc-coauthoring`, `docx`, `pdf`, `pptx`, `xlsx`.
*   **Comunicação e Treinamento:** `academy-guide`, `internal-comms`, `slack-gif-creator`, `discernment-nudge`.

### 2.3. Claude Desktop (Arquiteto e Analista)
Atua como centro de dados e revisor arquitetônico. Não escreve código de produção diretamente, mas verifica a lógica, analisa dados do banco de dados e formula tarefas para o OpenCode.
Arsenal de habilidades:
*   **Gestão de Contexto:** `morning`, `Import-memory`, `skill-creator`, `doc-coauthoring`.
*   **Análise e Validação:** `analyze`, `data-context-extractor`, `explore-data`, `validate-data`, `statistical-analysis`.
*   **BD e Visualização de Dados:** `sql-queries`, `write-query`, `build-dashboard`, `create-viz`, `data-visualization`.

### 2.4. Antigravity (Ambiente de Agentes Unificado)
Um ambiente totalmente autônomo que integra o conjunto completo de 33 habilidades.
*   **Regla principal:** Toda a documentação do projeto deve a partir de agora ser criada e mantida exclusivamente através do Antigravity, aproveitando os modelos Gemini e Claude (como as ferramentas de documentação preferenciais com acesso irrestrito às habilidades).

---

## 3. Etapas do Protocolo (Ciclo de Vida do Projeto)

### Etapa 1: Inicialização e ARCHITECTURE.md
A arquitetura é formulada antes de ser escrita qualquer linha de código.
1.  O **Claude Desktop** ativa as habilidades `morning` e `Import-memory` para carregar o contexto e os trabalhos anteriores. Depois, aplica `analyze` para decompor os requisitos.
2.  O **OpenCode** usa a habilidade `build-project-docs` para criar um rascunho de `ARCHITECTURE.md`.
3.  O documento consolida-se: estruturas de dados, formatos de armazenamento, stack tecnológico e divisão de módulos.

### Etapa 2: Grill-me (Teste de Estresse da Arquitetura)
A arquitetura não é aceita por fé. Ela deve ser atacada e questionada.
1.  O **Claude Desktop** aplica `data-context-extractor` para identificar "pontos cegos" nos dados e `doc-coauthoring` para gerar perguntas desconfortáveis.
2.  O **OpenCode** pode usar `discernment-nudge` para uma autoavaliação crítica das soluções técnicas propostas.
3.  Cada ponto de decisão controverso é encerrado com uma tríade: **solução escolhida -> razão para rejeitar a alternativa -> exclusões do escopo**.

### Etapa 3: Desvios Deliberadas (Deliberate Deviations)
Uma seção no `ARCHITECTURE.md` onde registramos todas as funcionalidades e capacidades que **decidimos conscientemente não construir**. A fronteira das capacidades de um projeto é parte integrante de sua arquitetura. Se uma decisão mudar durante o desenvolvimento, a decisão antiga é movida para cá junto com a justificativa.

### Etapa 4: Implementação Módulo a Módulo
O desenvolvimento avança de baixo para cima ao longo do grafo de dependências.
1.  O **OpenCode** implementa o núcleo do projeto. Para integrações e protocolos, são utilizados `mcp-builder` e `claude-api`.
2.  Ao trabalhar no lado visual, o **OpenCode** ativa a cadeia: `brand-guidelines` -> `theme-factory` -> `frontend-design` -> `web-artifacts-builder`.
3.  Para geração de gráficos procedimentais ou canvas complexos, aplicam-se `algorithmic-art` e `canvas-design`.

### Etapa 5: Revisão de Código e Testes
A verificação é sempre separada da escrita do código.
1.  O **OpenCode** realiza uma análise separada usando a habilidade `code-review-skill`, identificando bugs e compromissos.
2.  Os testes de interface e integração são conduzidos através da habilidade `webapp-testing`. O output dos testes (stdout/stderr) é guardado sem modificações.
3.  O **Claude Desktop** intervém para verificar o manuseio de dados: usa `sql-queries` e `write-query` para verificar a integridade da base de dados, juntamente com `validate-data` e `statistical-analysis` para verificar a lógica de negócio.

### Etapa 6: Geração de Artefatos e Análises
O projeto deve ser apresentado ao usuário ou stakeholders.
1.  O **Claude Desktop**, usando `build-dashboard`, `create-viz` e `data-visualization`, elabora relatórios baseados nos resultados ou métricas da aplicação.
2.  O **OpenCode** empacota estes dados em artefatos de negócios prontos para uso:
    *   Relatórios e especificações: habilidades `pdf`, `docx`, `xlsx`.
    *   Apresentações de arquitetura: habilidade `pptx`.
    *   Treinamentos e materiais internos: `academy-guide`, `internal-comms`.
    *   Conteúdo dinâmico para anúncios: `slack-gif-creator`.

### Etapa 7: Checklist Final
Antes do lançamento, verifica-se:
*   Sincronização do código final com o `ARCHITECTURE.md`.
*   Presença de logs reais de teste.
*   Ausência de arquivos temporários, caches e chaves secretas.

---

## 4. Política de Seleção de Modelos (Model Selection Policy)

O OpenCode roda em modelos gratuitos, cuja escolha é ditada pela tarefa:

| Modelo | Papel | Finalidade | Status de Privacidade |
| :--- | :--- | :--- | :--- |
| **Muse Spark 1.2 Free** | Agente Autónomo (Core) | Execução da matriz de habilidades principal, contexto de 1M de tokens, lógica de múltiplas etapas no terminal. | Camada gratuita permanente |
| **Nemotron 3 Ultra Free** | Analista Profundo | Matemática pesada, algoritmos complexos, refactorização de sistemas em grande escala. | **Trial da NVIDIA** — os dados são registrados para melhorar o produto. |
| **Nemotron 3.5 Lightning Free** | Executor em Segundo Plano | Validação rápida, chamadas de função utilitárias, processamento em lote de pipelines. | **Trial da NVIDIA** — idêntico ao Ultra. |
| **MiMo V2.5 Free** | Assistente de UI/UX | Depuração por captura de tela, `frontend-design` em tempo real. | Período gratuito temporário. |

Para o **Antigravity**, o **Gemini 3.5 Flash (Medium)** é utilizado como o motor primário para garantir o consumo mínimo de limites/quotas e permitir o trabalho contínuo em tarefas e documentação.

**Restrição de Segurança:** É **estritamente proibido** passar chaves privadas, tokens, bancos de dados reais e repositórios privados para os endpoints de teste (Nemotron, MiMo). Apenas ambientes locais ou confiáveis devem ser usados para dados confidenciais.

---

## 5. Princípios Fundamentais do Ecossistema

1. **Uma decisão explícita é melhor do que um padrão conveniente.** Se um agente se deparar com uma encrusilhada, ele não tenta adivinhar; ele formula opções e aguarda aprovação (ou registra um compromisso).
2. **As habilidades são usadas para a finalidade pretendida.** Não há necessidade de gerar tabelas em Markdown se for necessário um relatório em Excel (use `xlsx`). Não há necessidade de descrever um painel em texto (use `build-dashboard` + `create-viz`).
3. **Um bug encontrado na revisão significa um sistema funcionando.** Um achado durante a fase de revisão através do `code-review-skill` é prova de que o filtro de duas etapas funciona.
4. **Os limites do projeto são invioláveis.** Uma ferramenta inacabada que faz tudo é pior do que uma ferramenta altamente especializada com uma seção de Desvios Deliberadas (Deliberate Deviations) claramente documentada.
