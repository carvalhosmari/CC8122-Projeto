# Entrega 5 — Análise de tarefas: HTA, GOMS e CTT

**Data:** 07/11/2026  
**Status:** 🟩 concluída  
**Responsabilidade:** cada integrante modela pelo menos 1 HTA, 1 GOMS e 1 CTT. As três técnicas podem abordar a mesma funcionalidade ou funcionalidades distintas, conforme a orientação da disciplina.

## Objetivo da atividade

Modelar tarefas importantes sob perspectivas complementares: decomposição hierárquica (HTA), estrutura de metas/métodos/operações (GOMS) e relações temporais entre tarefas (CTT). O diagrama deve ser acompanhado de interpretação textual.

## Para projetos cujo TCC não previa interface

Modele **tarefas humanas relacionadas ao uso da contribuição técnica**, e não a implementação interna do algoritmo. Exemplos de boas tarefas para análise:

- investigar uma consulta de baixo desempenho;
- configurar uma análise e selecionar parâmetros;
- submeter um dataset e verificar sua validade;
- acompanhar uma execução demorada;
- comparar dois resultados/modelos;
- interpretar uma recomendação e decidir se a aceita;
- localizar uma execução anterior usando busca/filtros;
- gerar e compartilhar um relatório;
- administrar papéis/permissões quando isso for parte do trabalho real;
- revisar um alerta e registrar uma decisão.

Um CRUD pode gerar tarefas relevantes, mas “cadastrar usuário” só merece modelagem se tiver significado no domínio (papéis, validações, riscos, permissões, dependências).

## Seleção das tarefas

| ID | Tarefa | Persona/cenário de origem | Frequência/criticidade | Autor responsável |
|---|---|---|---|---|
| T01 | Avaliar tomografia | P01/C01 | Alta frequência / Alta criticidade | Mariane S. Carvalho - RA: 22.123.105-3 |

> Priorize tarefas necessárias para que o usuário alcance objetivos centrais. Não desperdice a modelagem em ações triviais isoladas, como “clicar em login”, se o objetivo relevante é maior. Da mesma forma, não modele o funcionamento interno do algoritmo como se fosse uma tarefa humana.

---

## HTA — T01 Avaliar tomografia

**Autor(a):** Mariane S. Carvalho - RA: 22.123.105-3

### Descrição da tarefa

O objetivo é avaliar uma tomografia renal e decidir como prosseguir diante de possíveis achados. A tarefa começa quando o Mario Russano precisa examinar o caso em uma clínica de nefrologia e tem acesso às imagens e às informações clínicas disponíveis; termina após revisar o exame, considerar possíveis achados e definir se é necessária alguma avaliação complementar. O cenário e o fluxo de acesso às imagens são hipóteses ainda não validadas com profissionais. No diagrama atual, a decomposição chega apenas à seleção das imagens e ainda não representa sua avaliação nem a decisão final, que é feita unicamente por Mario.

### Diagrama

![HTA T01](../assets/05_tarefas/hta_t01.svg)

### Decomposição e planos

| ID | Objetivo/operação | Plano/ordem | Problema ou decisão de design observada |
|---|---|---|---|
| 0. | Avaliar tomografia 1 > 2 | Fazer login **E DEPOIS** Selecionar imagens | A decomposição ainda não representa a análise das imagens, a consideração da indicação do modelo nem a decisão de como prosseguir; login como pré-requisito também é uma hipótese a validar. |
| 1. | Fazer login 1 + 2 | Informar usuário **E** Informar senha | Os dois dados são necessários no fluxo proposto, mas a autenticação e a ordem de preenchimento precisam ser validadas com o fluxo real. |
| 1.1. | Informar usuário |  | Definir qual identificador é aceito e orientar o formato e os erros sem exigir dados além do necessário. |
| 1.2. | Informar senha |  | A senha deve ser protegida na interface; mensagens de erro não devem expor credenciais. |
| 2. | Selecionar imagens 1 / 2 | Fazer upload **OU** selecionar paciente | As alternativas precisam levar ao exame correto; validar se o fluxo real permite envio de arquivos, busca de paciente ou ambos. |
| 2.1. | Fazer upload 1 / 2 | Selecionar localmente **OU** arrastar imagens | Especificar formatos e quantidade aceitos e informar validação e progresso do envio; esses requisitos ainda não foram definidos. |
| 2.1.1. | Selecionar localmente |  | Orientar a seleção de arquivos aceitos e indicar quando a seleção ou o carregamento terminar. |
| 2.1.2. | Arrastar imagens |  | Indicar a área de destino e confirmar o carregamento; oferecer também uma alternativa que não dependa de arrastar e soltar. |
| 2.2. | Selecionar paciente 1 / 2 | Informar nome e cpf **OU** informar prontuário | A busca deve permitir localizar e confirmar o paciente correto sem expor dados pessoais desnecessariamente; validar os identificadores usados no fluxo real. |
| 2.2.1. | Informar nome e cpf |  | Nome e CPF são dados pessoais; apresentar resultados de modo que o profissional confirme a identidade sem ambiguidade. |
| 2.2.2. | Informar prontuário |  | Orientar o formato do identificador e informar claramente quando não houver correspondência ou houver mais de uma. |

**Verificação do HTA:**

- O objetivo 0 representa uma meta do usuário?
- As subtarefas são necessárias e suficientes?
- Os **planos** indicam ordem, alternativa, repetição ou condição?
- A decomposição parou em nível útil para projeto de interação?

---

## GOMS — T01 Avaliar tomografia

**Autor(a):** Mariane S. Carvalho — RA: 22.123.105-3

### Goal

`G0: Fazer upload das imagens`

### Métodos, operadores e regras de seleção

- **Method M1:** Selecionar localmente
  - Operators: 
    - OP1: Clicar no botão de upload
    - OP2: Aguardar abertura do explorador de arquivos
    - OP3: Navegar até o diretório desejado
    - OP4: Selecionar as imagens
    - OP5: Confirmar a seleção
    - OP6: Aguardar o carregamento
- **Method M2:** Arrastar imagens
  - Operators: 
    - OP1: Localizar as imagens no computador
    - OP2: Selecionar os arquivos
    - OP3: Arrastar os arquivos até a área de upload
    - OP4: Soltar os arquivos na área indicada
    - OP5: Aguardar o carregamento
- **Selection Rule SR1:** usar M1 quando preferência do usuário for utilizar o explorador de arquivos; usar M2 quando preferência do usuário for utilizar a funcionalidade de arrastar e soltar.

> Não chame qualquer passo de “método”. Em GOMS, métodos são sequências alternativas capazes de atingir uma meta; regras de seleção explicam quando escolher entre eles.

---

## CTT — T01 Avaliar tomografia

**Autor(a):** Mariane S. Carvalho — RA: 22.123.105-3

### Descrição

O diagrama representa uma proposta de fluxo em que Mario Russano faz login, informa usuário e senha e tem as credenciais validadas antes de acessar a avaliação. Em seguida, seleciona as imagens por upload ou seleciona um paciente; no upload, pode selecionar os arquivos localmente ou arrastá-los, e na busca do paciente pode informar nome e CPF ou número de prontuário. Após selecionar as imagens, interpreta o resultado da avaliação. Assim, a tarefa começa com o acesso ao sistema e termina com a interpretação desse resultado; o diagrama não detalha a inspeção das imagens nem como o profissional decide os próximos passos clínicos. O fluxo, as alternativas e o papel do resultado são propostas ainda a validar com profissionais.

### Diagrama

![CTT T01](../assets/05_tarefas/ctt_t01.svg)

### Legenda e relações temporais usadas

| Operador/relação | Significado no diagrama | Exemplo no modelo |
|---|---|---|
| `[]>>` — ativação com passagem de informação | A segunda tarefa ocorre somente após a primeira, e a informação da primeira tarefa é passada para a segunda | Mário Russano faz o login para acessar o sistema, e só após estar autenticado pode ter acesso à funcionalidade de avaliar um conjunto de imagens de uma tomografia computadorizada. |
| `>>` — ativação | A segunda tarefa ocorre somente após a primeira, e a informação da primeira tarefa é passada para a segunda | Uma vez que Mario Russano está autenticado, ele inicia o processo de avaliação. |
| `[]` — escolha | Duas opções habilitadas para alcançar a mesma meta, mas uma vez que uma é escolhida, a outra é desabilitada. | Mario Russano escolhe o conjunto de um paciente específico a partir de uma busca por nome e cpf deste paciente. |

Identifique, quando aplicável, tarefas de usuário, sistema, interação e tarefas abstratas. Verifique se concorrência, escolha, habilitação, desabilitação e repetição estão representadas corretamente segundo a notação adotada em aula.

---

## Síntese da equipe

Como oportunidades de interação a investigar, destacam-se a forma de localizar o exame e confirmar o paciente correto, a orientação e o retorno durante o envio, alternativas acessíveis ao arrastar e soltar e a apresentação do resultado como informação de apoio, relacionada às imagens e às informações disponíveis. Esses pontos, assim como login, identificadores e caminhos alternativos, são hipóteses de fluxo e precisam ser validados com profissionais.

Para o protótipo e o teste de usabilidade, priorizar um cenário em que o profissional localiza ou envia um exame, consulta as imagens e o resultado do modelo, interpreta essa informação no contexto disponível e identifica como prosseguir diante de possível achado ou dúvida. Avaliar se a pessoa encontra o exame correto, entende o resultado sem tratá-lo como conclusão clínica e consegue indicar um próximo passo. Tratar os caminhos de seleção local/arrastar arquivos e busca por paciente como alternativas a testar; manter o login como contexto ou pré-condição, não como objetivo principal da tarefa.

## Checklist

- [x] Cada integrante produziu ao menos 1 HTA, 1 GOMS e 1 CTT.
- [x] Cada artefato identifica autor e tarefa.
- [x] Diagramas são legíveis e possuem fonte editável quando possível.
- [x] HTA contém planos, não apenas árvore de tópicos.
- [x] GOMS distingue Goals, Operators, Methods e Selection Rules.
- [x] CTT usa operadores temporais e tipos de tarefa coerentes.
- [x] Há texto explicando cada diagrama.
- [x] Tarefas estão ligadas a cenários/personas na rastreabilidade.
- [x] Em TCC técnico, as tarefas descrevem o que a pessoa faz com a contribuição/resultados, não passos internos do código.
- [x] CRUDs, relatórios, filtros e atividades administrativas foram escolhidos por relevância ao objetivo do usuário.
