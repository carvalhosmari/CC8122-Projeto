# Entrega 5 — Análise de tarefas: HTA, GOMS e CTT

**Data:** 02/11/2026  
**Status:** 🟨 em andamento  
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
| T01 | Avaliar tomografia | P01/C01 | {{...}} | {{...}} |

> Priorize tarefas necessárias para que o usuário alcance objetivos centrais. Não desperdice a modelagem em ações triviais isoladas, como “clicar em login”, se o objetivo relevante é maior. Da mesma forma, não modele o funcionamento interno do algoritmo como se fosse uma tarefa humana.

---

## HTA — T01 Avaliar tomografia

**Autor(a):** Mariane S. Carvalho — RA: 22.123.105-3

### Descrição da tarefa

{{objetivo, ponto de início, conclusão esperada, contexto}}

### Diagrama

![HTA T01](../assets/05_tarefas/hta_t01.svg)

### Decomposição e planos

| ID | Objetivo/operação | Plano/ordem | Problema ou decisão de design observada |
|---|---|---|---|
| 0. | Avaliar tomografia 1 > 2 | Fazer login **E DEPOIS** Selecionar imagens |  |
| 1. | Fazer login 1 + 2 | Informar usuário **E** Informar senha |  |
| 1.1. | Informar usuário |  |  |
| 1.2. | Informar senha |  |  |
| 2. | Selecionar imagens 1 / 2 | Fazer upload **OU** selecionar paciente |  |
| 2.1. | Fazer upload 1 / 2 | Selecionar localmente **OU** arrastar imagens |  |
| 2.1.1. | Selecionar localmente |  |  |
| 2.1.2. | Arrastar imagens |  |  |
| 2.2. | Selecionar paciente 1 / 2 | Informar nome e cpf **OU** informar prontuário |  |
| 2.2.1. | Informar nome e cpf |  |  |
| 2.2.2. | Informar prontuário |  |  |

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
    - Clicar no botão de upload
    - Aguardar abertura do explorador de arquivos
    - Navegar até o diretório desejado
    - Selecionar as imagens
    - Confirmar a seleção
    - Aguardar o carregamento
- **Method M2:** Arrastar imagens
  - Operators: 
    - Localizar as imagens no computador
    - Selecionar os arquivos
    - Arrastar os arquivos até a área de upload
    - Soltar os arquivos na área indicada
    - Aguardar o carregamento
- **Selection Rule SR1:** usar M1 quando preferência do usuário for utilizar o explorador de arquivos; usar M2 quando preferência do usuário for utilizar a funcionalidade de arrastar e soltar.

> Não chame qualquer passo de “método”. Em GOMS, métodos são sequências alternativas capazes de atingir uma meta; regras de seleção explicam quando escolher entre eles.

---

## CTT — T01 Avaliar tomografia

**Autor(a):** Mariane S. Carvalho — RA: 22.123.105-3

### Descrição

{{...}}

### Diagrama

![CTT T01](../assets/05_tarefas/ctt_t01.svg)

### Legenda e relações temporais usadas

| Operador/relação | Significado no diagrama | Exemplo no modelo |
|---|---|---|
| {{...}} | {{...}} | {{...}} |

Identifique, quando aplicável, tarefas de usuário, sistema, interação e tarefas abstratas. Verifique se concorrência, escolha, habilitação, desabilitação e repetição estão representadas corretamente segundo a notação adotada em aula.

---

## Síntese da equipe

Quais problemas de interação, oportunidades e requisitos apareceram a partir das modelagens? Quais tarefas irão para o protótipo e para o teste de usabilidade?

## Checklist

- [ ] Cada integrante produziu ao menos 1 HTA, 1 GOMS e 1 CTT.
- [ ] Cada artefato identifica autor e tarefa.
- [ ] Diagramas são legíveis e possuem fonte editável quando possível.
- [ ] HTA contém planos, não apenas árvore de tópicos.
- [ ] GOMS distingue Goals, Operators, Methods e Selection Rules.
- [ ] CTT usa operadores temporais e tipos de tarefa coerentes.
- [ ] Há texto explicando cada diagrama.
- [ ] Tarefas estão ligadas a cenários/personas na rastreabilidade.
- [ ] Em TCC técnico, as tarefas descrevem o que a pessoa faz com a contribuição/resultados, não passos internos do código.
- [ ] CRUDs, relatórios, filtros e atividades administrativas foram escolhidos por relevância ao objetivo do usuário.
