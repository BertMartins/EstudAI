# EstudAI

Plataforma inteligente de estudos e apoio ao ensino com IA, projetada para estudantes e professores em diferentes contextos educacionais.

## Visão geral

O **EstudAI** é uma aplicação web front-end desenvolvida para centralizar recursos de aprendizagem assistida por inteligência artificial em uma interface moderna, responsiva e orientada à experiência do usuário.

A plataforma oferece fluxos distintos para **alunos** e **professores**, contemplando estudo por matéria, resolução de atividades, quizzes inteligentes, organização de conteúdo por unidades, cursos de idiomas, cálculo de médias, suporte para faculdade e preparação para concursos. :contentReference[oaicite:1]{index=1}

## Principais recursos

### Fluxo de acesso com configuração de IA
A aplicação inicia com uma tela de configuração onde o usuário informa:

- chave da API Poe
- modelo de IA desejado

Modelos disponíveis no sistema:

- GPT-5.2
- Gemini 3 Flash
- Claude Sonnet 4.5
- Grok 4.1 Fast Non-Reasoning :contentReference[oaicite:2]{index=2}

### Setup inicial com perfis de uso
O onboarding foi expandido para suportar dois perfis principais:

- **Aluno(a)**: fluxo voltado para estudo e acompanhamento acadêmico
- **Professor(a)**: fluxo voltado para apoio didático e organização do ensino :contentReference[oaicite:3]{index=3}

#### Perfil Aluno
O aluno informa nome e nível/série, com opções para:

- Ensino Fundamental I
- Ensino Fundamental II
- Ensino Médio
- Já Formado :contentReference[oaicite:4]{index=4}

#### Perfil Professor
O professor pode selecionar o contexto em que leciona:

- Escola
- Curso de Idioma
- Faculdade

Depois, o fluxo avança para configuração contextual, incluindo área e disciplina ministrada. :contentReference[oaicite:5]{index=5}

## Módulos da plataforma

### 1. Dashboard principal
O painel central da aplicação reúne os principais acessos do sistema:

- matérias
- calculadora de média
- cursos de idiomas
- faculdade
- concursos
- quiz aleatório :contentReference[oaicite:6]{index=6}

A exibição de alguns módulos varia de acordo com o contexto selecionado no onboarding e com o perfil do usuário. Isso evita poluição visual e deixa a experiência mais coerente. Coisa rara na internet: uma interface que tenta ajudar em vez de testar a paciência. :contentReference[oaicite:7]{index=7}

### 2. Estudo por matéria
Cada matéria possui uma área dedicada com navegação em abas:

- **Chat**
- **Atividades**
- **Quiz**
- **Conteúdo** :contentReference[oaicite:8]{index=8}

#### Chat com IA
Permite que o usuário envie dúvidas diretamente sobre a matéria selecionada, com histórico contextualizado por disciplina. :contentReference[oaicite:9]{index=9}

#### Ajuda com atividades
Usuários podem colar enunciados, exercícios ou tarefas no campo de atividade para receber suporte da IA na resolução ou explicação do conteúdo. :contentReference[oaicite:10]{index=10}

#### Conteúdo por unidades
A aba de conteúdo organiza a disciplina em unidades didáticas, com suporte para:

- exibição de unidades
- carregamento de tópicos via IA
- expansão e recolhimento por seção
- exibição de explicações em markdown :contentReference[oaicite:11]{index=11}

### 3. Quiz inteligente
O módulo de quiz foi refinado e agora permite:

- seleção de unidade específica
- quiz geral com todas as unidades
- geração de perguntas com IA
- pontuação
- barra de progresso
- streak de acertos
- explicação por resposta
- tela de resultado final :contentReference[oaicite:12]{index=12}

Esse formato melhora o uso para revisão segmentada, sem obrigar o usuário a cair num “modo prova surpresa” toda vez. :contentReference[oaicite:13]{index=13}

### 4. Quiz aleatório
Além do quiz por disciplina, o sistema mantém um modo de **Quiz Aleatório**, com perguntas de diferentes matérias, ideal para revisão geral e treino rápido. :contentReference[oaicite:14]{index=14}

### 5. Cursos de idiomas
A plataforma conta com um módulo específico para estudo de idiomas, incluindo:

- seleção de idioma
- seleção de nível
- interface dedicada
- modo “abrasileirado” para facilitar pronúncia de palavras estrangeiras com adaptação ao português brasileiro :contentReference[oaicite:15]{index=15}

### 6. Calculadora de média
A calculadora acadêmica permite acompanhar desempenho por disciplina com base em:

- número de unidades
- média mínima para aprovação
- entrada de notas por matéria
- resumo visual com indicador circular
- status por disciplina :contentReference[oaicite:16]{index=16}

Status previstos na interface:

- aprovado
- em progresso
- alerta
- risco
- sem dados :contentReference[oaicite:17]{index=17}

### 7. Área de faculdade
O sistema possui uma seção dedicada ao contexto universitário, com suporte para:

- cadastro do nome do curso
- gerenciamento de matérias do curso
- grade própria de disciplinas
- personalização de matérias por contexto universitário :contentReference[oaicite:18]{index=18}

### 8. Área de concursos
Também há suporte para estudos voltados a **concursos públicos**, com uma área própria para organizar matérias cobradas nesse contexto. :contentReference[oaicite:19]{index=19}

## Arquitetura da interface

Com base no arquivo atualizado, a aplicação é organizada em views principais renderizadas no front-end:

- `apiKeyScreen`
- `setupScreen`
- `mainScreen`

Dentro da tela principal, o sistema é segmentado em subviews:

- `dashboardView`
- `subjectView`
- `langSelectView`
- `calcView`
- `collegeView`
- `concursoView` :contentReference[oaicite:20]{index=20}

Essa estrutura permite uma navegação fluida dentro de uma aplicação de página única, controlada por estado global e exibição condicional. :contentReference[oaicite:21]{index=21}

## Gestão de estado

O projeto utiliza um objeto global de estado para centralizar informações da aplicação, como:

- credenciais e modelo de IA
- nome do usuário
- perfil selecionado
- série ou contexto educacional
- view atual
- matéria atual
- histórico de chat
- dados do quiz
- modo de idioma
- matérias personalizadas
- contexto escolar, universitário ou concurso
- dados da calculadora :contentReference[oaicite:22]{index=22}

## Persistência local

A aplicação utiliza uma camada de armazenamento baseada em:

- memória em tempo de execução
- cookies no navegador

Esse mecanismo permite persistir preferências e parte dos dados do usuário localmente, mesmo sem backend dedicado nesse trecho do projeto. :contentReference[oaicite:23]{index=23}

## Tecnologias utilizadas

O projeto, na versão enviada, utiliza:

- **HTML5**
- **CSS3**
- **JavaScript Vanilla**
- **Tailwind CSS** via CDN
- **Font Awesome**
- **Google Fonts**
- **Marked.js** para renderização de markdown :contentReference[oaicite:24]{index=24}

## Experiência do usuário e interface

A interface foi construída com foco em clareza visual e engajamento, incluindo:

- suporte a tema claro e escuro
- componentes com animações
- cards interativos
- modais
- toasts
- renderização de markdown
- layout responsivo
- identidade visual amigável e moderna :contentReference[oaicite:25]{index=25}

Também há refinamentos importantes no fluxo de onboarding e navegação contextual, o que melhora bastante a percepção de produto e usabilidade geral. :contentReference[oaicite:26]{index=26}

## Casos de uso

O EstudAI pode ser utilizado para:

- reforço escolar
- revisão para provas
- prática com quizzes por unidade
- explicação de exercícios
- estudo guiado por disciplina
- apoio ao ensino por professores
- estudo de idiomas
- acompanhamento de notas
- organização de conteúdos acadêmicos
- preparação para faculdade e concursos :contentReference[oaicite:27]{index=27}

## Estrutura atual do projeto

Pelo arquivo compartilhado, o projeto está concentrado em um documento HTML com:

- marcação da interface
- estilos embutidos
- configuração de bibliotecas
- gerenciamento de estado
- fluxo de navegação entre telas :contentReference[oaicite:28]{index=28}

## Como executar

Como a aplicação está estruturada em HTML com dependências carregadas via CDN, a execução local pode ser feita de forma simples:

```bash
# basta abrir o arquivo HTML no navegador
