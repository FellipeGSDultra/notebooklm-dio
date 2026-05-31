# 🚀 Miniguia de Estudos: Dominando Git e GitHub com NotebookLM

## 📌 1. Contexto e Objetivos

Este repositório foi desenvolvido como o desafio de projeto final para a conclusão de curso na **DIO (Digital Innovation One)**. O objetivo principal deste trabalho é aplicar o conceito de **aprendizagem ativa** utilizando a Inteligência Artificial como ferramenta de suporte técnico e curadoria de conhecimento.

O tema escolhido para este caderno temático foi o ecossistema **Git e GitHub**, abrangendo desde conceitos estruturais e fluxos de trabalho locais até boas práticas de versionamento em equipe e resolução de conflitos. Através da ferramenta **NotebookLM** da Google, foi possível consolidar fontes confiáveis para gerar resumos de alto valor, um glossário técnico e prompts reutilizáveis voltados para produtividade.

---

## 📚 2. Curadoria de Fontes

Para alimentar a base de conhecimento da IA e garantir a precisão técnica das respostas geradas, foram selecionadas as seguintes fontes abertas, incluindo artigos, e-books e documentações em PDF:

* **Fonte 1:** *Artigo Scielo - Gestão de Produção* - [Acessar Link](https://www.scielo.br/j/prod/a/VXmXkX86mRyjxVWqhZJ7sKm/?lang=pt)
* **Fonte 2:** *Artigo Alura - Como escrever um bom README* - [Acessar Link](https://www.alura.com.br/artigos/escrever-bom-readme?srsltid=AfmBOoqkBj80U3f1oZAq6zeO7tKuEsr2FbdMijUck1w9gUcsl7du1WIw)
* **Fonte 3:** *E-book Git (Sérgio Cabral)* - [Acessar Link](https://ebooks.sergiocabral.com/git/)
* **Fonte 4:** *PDF - Implementando o Gitflow para Gerencia de Configuração em um Projeto de Desenvolvimento de Software Ágil* (Upload no NotebookLM)
* **Fonte 5:** *PDF - GitHub: Folha de Dicas de Git (Cheat Sheet)* (Upload no NotebookLM)

---

## 🛠️ 3. Engenharia de Prompts e "Cicatrizes" (Troubleshooting)

O mercado valoriza profissionais que sabem interagir de forma estratégica com a IA. Abaixo está documentado o processo de evolução de escrita de prompts (*prompt engineering*) realizado no NotebookLM, demonstrando o raciocínio aplicado para extrair respostas de alta qualidade.

### ❌ Teste 1: Prompt Vago (Abordagem Ruim)
* **Prompt enviado:** *"Como mexe no Git?"*
* **Comportamento da IA:** A IA retornou uma explicação muito ampla, misturando conceitos teóricos genéricos sem focar em casos de uso práticos ou na sintaxe real dos comandos.
* **"Cicatriz" (Dificuldade encontrada):** Prompts sem contexto ou sem uma persona definida geram respostas vagas e pouco acionáveis para o dia a dia de um desenvolvedor.

### 🎯 Teste 2: Prompt Refinado (Abordagem Sênior)
* **Prompt enviado:** *"Atue como um Engenheiro de Software Sênior e me dê um passo a passo objetivo, incluindo os comandos de terminal necessários, para resolver um conflito de Merge (Merge Conflict) entre duas branches."*
* **Resultado obtido (Troubleshooting de Sucesso):** O NotebookLM compreendeu o papel técnico e entregou um fluxo de trabalho cirúrgico, estruturado em passos lógicos que um profissional realmente executa:
    1.  Uso do `git status` para isolar os arquivos impactados.
    2.  Identificação visual e humana dos marcadores de conflito (`<<<<<<< HEAD`, `=======`, `>>>>>>>`) dentro do editor de código.
    3.  Preparação e indexação via `git add`.
    4.  Finalização e consolidação do histórico com `git commit`.

---

## 📖 4. Miniguia de Estudo (Entrega Final)

### 📄 Resumos Estruturados do Assunto

#### O que é o Git?
O **Git** é um software de linha de comando de código aberto classificado como um **Sistema de Controle de Versão Distribuído (VCS)** ou Gerenciamento de Controle de Código-Fonte (SCM). A sua principal finalidade é registrar modificações em um conjunto de arquivos ao longo de uma linha do tempo, mantendo um histórico seguro de versões e viabilizando o trabalho de equipes distribuídas.

#### O que é o GitHub?
O **GitHub** é um **servidor de repositórios baseado na nuvem**, amplamente utilizado para hospedar projetos de código e conhecido no mercado como uma "rede social para pessoas desenvolvedoras".

#### A Diferença Crucial entre Ambos
Apesar dos nomes parecidos, eles são projetos independentes, mas totalmente integrados. **O GitHub funciona como o servidor de repositórios na nuvem, enquanto o Git atua como o cliente local para esse servidor**. O Git é a ferramenta instalada na sua máquina de desenvolvimento; o GitHub é a plataforma web onde você hospeda o código gerenciado pelo Git. (Outras alternativas de servidores incluem GitLab, Bitbucket e Azure DevOps).

#### As Etapas do Fluxo de Trabalho do Git (As Três Árvores + Nuvem)
O fluxo de arquivos gerenciados pelo Git transita principalmente por três áreas locais, culminando na sincronização com o servidor externo:
1.  **Working Directory (Diretório de Trabalho):** A pasta física do seu projeto no sistema operacional onde você cria e edita seus arquivos.
2.  **Staging Area (Index/Stage):** A área de preparação. Funciona como um rascunho contendo as alterações selecionadas pelo comando `git add` que estão prestes a entrar no repositório.
3.  **Local Repository (Repositório Local / HEAD):** O banco de dados oficial do Git na sua máquina (localizado na pasta oculta `.git`). Armazena permanentemente os históricos de commits através do comando `git commit`. O ponteiro `HEAD` sempre referencia o último commit feito ali.
4.  **Remote Repository (Repositório Remoto):** O servidor na nuvem (como o GitHub) usado para compartilhar o histórico com o time através de comandos como `git push` (para enviar) e `git pull` / `git fetch` (para baixar e atualizar).

---

### 📝 Glossário de Conceitos Essenciais

* **Commit:** Grava uma alteração ou conjunto de alterações permanentemente no histórico de versão do repositório local. Cada commit possui um identificador único em formato de *hash* de 40 caracteres.
* **Push:** Envia os commits realizados no seu repositório local (ou ramificação atual) para o repositório remoto hospedado no GitHub.
* **Pull:** Baixa o histórico de dados do servidor remoto e incorpora automaticamente essas mudanças no seu branch local atual (executa de forma combinada o `git fetch` e o `git merge`).
* **Clone:** Faz o download e cria uma cópia local idêntica de um repositório existente na nuvem, trazendo todo o projeto e seu respectivo histórico de versões.
* **Fork:** Funcionalidade de plataformas como o GitHub que cria uma cópia pessoal de um repositório de terceiros na sua própria conta, permitindo modificações sem afetar o projeto original.
* **Branch:** Uma nova linha de desenvolvimento em paralelo à ramificação principal (como a `main` ou `master`), muito útil para criar novas funcionalidades sem quebrar o código em produção.
* **Merge:** Realiza a fusão de dois branches diferentes, combinando e conciliando seus históricos de alterações em um único ponto do projeto.
* **Pull Request (PR):** Um pedido formal feito no GitHub para que os mantenedores de um repositório revisem, discutam e integrem (via *merge*) as alterações enviadas por você a partir de uma branch ou fork.

---

### 📋 Biblioteca de Prompts Reutilizáveis

Abaixo estão dispostos **3 templates de prompts de engenharia reversa** para serem utilizados com assistentes de IA no dia a dia técnico. Para usar, basta copiar o texto e preencher as informações indicadas entre os colchetes `[ ]`.

#### 1. Prompt para Criação e Revisão de Mensagens de Commit
> **Prompt:**
> "Atue como um desenvolvedor sênior especialista em Git. Aqui está o resultado do comando `git diff` com as alterações que acabei de adicionar à *Staging Area* (index): 
>
> **[COLE SEU GIT DIFF AQUI]**
>
> Com base nessas alterações, escreva 3 opções de mensagens de commit (utilizando o formato `git commit -m "[mensagem]"`). A primeira opção deve ser direta e concisa. A segunda e a terceira devem ser mais detalhadas, explicando não apenas *o que* mudou, mas o *porquê* da mudança, ajudando a manter um histórico claro e rastreável. Siga as convenções de boas práticas de versionamento."

#### 2. Prompt para Estruturação de Branch e Descrição de Pull Request (Baseado em GitFlow)
> **Prompt:**
> "Estou trabalhando em um projeto que utiliza o modelo GitFlow de versionamento. Vou iniciar o desenvolvimento da seguinte tarefa:
> 
> **[INSERIR BREVE DESCRIÇÃO DA TAREFA/ISSUE AQUI]**
> 
> 1. Sugira um nome padronizado para a minha branch de funcionalidade, considerando que ela deve ser criada a partir da branch `develop` (exemplo: `feature/nome-da-tarefa`).
> 2. Crie um template de descrição de Pull Request (PR) em Markdown para quando eu for mesclar essa branch de volta na `develop`. O template de PR deve conter: um título claro, o objetivo da PR, uma lista de 'O que foi feito', 'Como testar', menção a possíveis conflitos e um checklist de garantia de qualidade."

#### 3. Prompt para Geração de README Atrativo
> **Prompt:**
> "Acabei de finalizar um projeto e preciso criar um arquivo `README.md` incrível e atrativo para o GitHub. Aqui está um resumo sobre o que o projeto faz e as tecnologias que utilizei:
>
> **[INSERIR RESUMO DO PROJETO E TECNOLOGIAS]**
> 
> Com base nisso, gere um código em Markdown contendo as seguintes seções recomendadas:
> - Título do projeto centralizado.
> - Sugestões de Badges (como status do projeto e licença).
> - Um Índice gerado em Markdown.
> - Descrição do Projeto.
> - Lista de Funcionalidades (utilizando emojis para ficar mais dinâmico).
> - Como baixar, abrir e executar o projeto localmente.
> - Tecnologias utilizadas.
> - Contribuidores ou Pessoas Desenvolvedoras.
> 
> O tom deve ser técnico, porém acessível, seguindo o padrão visual de repositórios famosos e de código aberto."

---
Feito com 💙 por Fellipe Gabriel Santos Dultra no desafio de aprendizagem ativa da DIO.
