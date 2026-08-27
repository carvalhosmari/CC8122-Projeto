# Entrega 1 — Conhecendo o projeto, o usuário e o problema

**Data:** 23/08/2026  
**Status:** 🟩 concluída  
**Responsabilidade:** 1 solução consolidada por equipe

## Objetivo da atividade

Reinterpretar o tema do TCC sob a perspectiva de Interação Humano-Computador e construir um **entendimento comum entre os integrantes da equipe**.

A disciplina utiliza preferencialmente o tema do TCC para os exercícios de IHC. Isso vale tanto para TCCs que já preveem uma interface quanto para trabalhos cujo resultado principal é algoritmo, modelo, API, biblioteca, análise de dados, infraestrutura, estudo experimental ou outro artefato técnico.

> **Importante:** a interface projetada na disciplina é um artefato de aprendizagem de IHC. Ela **não se torna automaticamente uma obrigação do TCC**. Sua incorporação ao trabalho de conclusão depende de decisão da equipe e do orientador.

Antes de preencher, leia [`../GUIA_ESCOPO_IHC.md`](../GUIA_ESCOPO_IHC.md).

Nesta primeira semana a equipe **não deve começar desenhando telas**. Primeiro deverá compreender:

- o que o TCC realmente produz;
- quem poderia obter valor dessa contribuição;
- quais pessoas interagem, administram, configuram, interpretam ou são afetadas;
- o que essas pessoas precisam alcançar;
- como atividades relacionadas acontecem hoje;
- problemas, limitações e contexto;
- alternativas existentes;
- qual recorte de interação fará sentido para a disciplina.

Ao final desta entrega, a equipe deve diferenciar:

- **tema do TCC** × **escopo formal do TCC** × **escopo de IHC da disciplina**;
- **objetivo do projeto** × **objetivo do usuário**;
- **problema do usuário** × **solução tecnológica**;
- **fato conhecido** × **hipótese** × **lacuna de conhecimento**;
- **capacidade técnica** × **forma de uso dessa capacidade**;
- **funcionalidade** × **atividade/resultado que o usuário precisa alcançar**;
- **usuário direto** × **stakeholders**.

---

## Como classificar as respostas

Sempre que a resposta fizer uma afirmação sobre usuários, problemas, atividades, necessidades, contexto ou mercado, use:

- **[F] Fato conhecido** — existe evidência/fonte.
- **[H] Hipótese** — afirmação plausível que ainda precisa ser investigada.
- **[?] Não sabemos ainda** — lacuna relevante.

Quando usar `[F]`, informe a origem. Hipóteses prioritárias devem receber IDs (`H01`, `H02`...) e também ser registradas em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

> **Exemplo:** `[H] H01 — DBAs considerariam útil comparar automaticamente o plano atual de execução com uma recomendação produzida pelo algoritmo.`

Uma hipótese explicitada é melhor do que uma suposição escondida.

---

# 0. Identificação do TCC e da equipe

## 0.1 Membros

| Nome completo | Matrícula | GitHub |
|---|---:|---|
| Mariane S. Carvalho | 22.123.105-3 | [github.com/carvalhosmari](https://github.com/carvalhosmari)  |

## 0.2 Título atual do TCC

Detecção de patologias renais em tomografia computadorizada por meio de redes convolucionais de baixo custo computacional.

## 0.3 Orientador(a)

Leila Cristina Carneiro Bergamasco

## 0.4 Qual é o resultado principal atualmente previsto no TCC?

Marque e descreva:

- [ ] sistema/aplicação interativa;
- [ ] algoritmo;
- [x] modelo de IA/ML/LLM;
- [ ] biblioteca/API/framework;
- [ ] análise de dataset;
- [ ] estudo/benchmark/avaliação experimental;
- [ ] infraestrutura/backend;
- [ ] componente embarcado/IoT;
- [ ] outro: {{...}}.

**Descrição:** Classificação de imagens médicas renais, considerando não apenas o desempenho diagnóstico, mas também a eficiência computacional e a interpretabilidade do modelo utilizado, visando contribuir para o desenvolvimento de sistemas inteligentes mais acessíveis e aplicáveis na prática clínica.

## 0.5 O TCC já previa desenvolvimento de interface com usuário?

- [x] Sim, a interface já faz parte do TCC.
- [ ] Parcialmente; existe alguma interação, mas ainda não está bem definida.
- [ ] Não. O TCC é predominantemente técnico e não previa interface.

**Explique o que está formalmente previsto no TCC:** Um sistema para auxílio do diagnóstico de patologias renais a partir do processamento de tomografias computadorizadas, que, além de ser assertivo, também deve ser explicável e, principalmente, de baixo custo para viabilizar a aplicabilidade clínica em órgãos do SUS.

> Esta resposta serve para separar o compromisso do TCC do projeto da disciplina. Mesmo quando a opção for **não**, a equipe irá definir uma interface para exercitar IHC.

---

# 1. Entendendo a contribuição do projeto

## 1.1 Explique o TCC em uma frase, sem citar linguagem de programação, framework ou banco de dados.

Um sistema para auxílio do diagnóstico de patologias renais a partir do processamento de tomografias computadorizadas

## 1.2 Qual situação, atividade ou problema do mundo real motivou o TCC?

[F] 

## 1.3 Qual é a **capacidade/contribuição central** produzida pelo TCC?

Complete, se ajudar:

> “Nosso TCC produz, melhora, analisa ou permite `{{capacidade}}`.”

Exemplos: otimizar consultas; classificar imagens; detectar anomalias; comparar modelos; identificar padrões; prever demanda; analisar desempenho; gerar resumos; recomendar configurações.

O TCC melhora a aplicabilidade clínica, uma vez que tarefas de processamento de imagens normalmente demandam alto poder computacional, e também possui interpretabilidade, fundamental para garantir a confiabilidade do modelo proposto, viabilizando o seu uso.

## 1.4 O que se espera que esteja diferente **para pessoas, organizações ou processos** se essa contribuição for bem-sucedida?

[F] Que a solução seja acessível;
[F] Que patologias renais, normalmente diagnosticadas em estágios avançados, possam ter o diagnóstico antecipado.
 

## 1.5 O que é mérito técnico/científico do TCC e o que seria uma possível aplicação prática?

| Mérito/contribuição técnica | Possível aplicação/valor em uso |
|---|---|
| Classificação de imagens médicas renais com redes convolucionais de baixo custo computacional e análise de interpretabilidade | Apoiar médicos na análise de tomografias computadorizadas, oferecendo uma indicação complementar para a avaliação de possíveis patologias renais. |

---

# 2. Entendendo as pessoas envolvidas

## 2.1 Quem interage diretamente com o produto, se já existe interface prevista?

Se não houver interface prevista no TCC, escreva `NÃO SE APLICA AO ESCOPO ORIGINAL` e prossiga para 2.2.

[F] Médicos

## 2.2 Quem poderia **usar, configurar, administrar, operar, interpretar ou tomar decisões** a partir da contribuição técnica?

Considere perfis profissionais e stakeholders, não apenas consumidores finais.

| Perfil | Relação com a contribuição | O que faria | Status/evidência |
|---|---|---|---|
| Médico radiologista ou especialista responsável pelo diagnóstico | Usuário direto e intérprete do resultado | Carregaria a tomografia, analisaria a indicação do modelo e a explicação associada, usando essas informações como apoio à decisão clínica | [H] - perfil a confirmar com profissionais |
| Pesquisador ou profissional de IA/ML | Responsável técnico pela avaliação do modelo | Configuraria versões do modelo, parâmetros e conjuntos de avaliação | [H] - cenário de adoção |
| Profissional de TI ou administrador do serviço | Operação e manutenção da solução | Administraria acesso, disponibilidade e integração com o fluxo institucional | [H] - cenário de adoção |

## 2.3 Existem pessoas afetadas que não usariam a interface diretamente?

| Stakeholder | Como é afetado | Usa interface? | Status/evidência |
|---|---|---|---|
| Paciente | Exames de imagem avaliados | não | [H] - impacto depende da adoção clínica da solução |

## 2.4 Que características desses perfis podem influenciar a interação?

Considere conhecimento do domínio, experiência tecnológica, frequência de uso, necessidades de acessibilidade, responsabilidade profissional, familiaridade com métricas, linguagem técnica, urgência etc.

[H] H01 - O médico terá familiaridade com sistemas de visualização de exames, mas poderá não conhecer métricas de aprendizado de máquina; portanto, a interface deverá apresentar o resultado em linguagem clínica compreensível e permitir consultar detalhes técnicos quando necessário.

[H] H02 - O uso ocorrerá em um contexto profissional com responsabilidade sobre a decisão clínica, exigindo distinção clara entre a indicação do modelo e o diagnóstico final do médico.

[?] Ainda não se sabe a frequência de uso, o nível de experiência tecnológica dos profissionais, os requisitos de acessibilidade e quais termos clínicos são preferidos.

---

# 3. Entendendo objetivos e atividades

## 3.1 O que o usuário está tentando conseguir no mundo real?

Não responda “usar o algoritmo”, “clicar no sistema” ou “ver o dashboard”.

[F] Obter auxílio diagnóstico de patologias renais em estágios iniciais, uma vez que os danos causados na estrutura dos rins nesses estágios normalmente não são visíveis a olho nu.

## 3.2 Quais são as atividades mais importantes?

| ID | Atividade/objetivo | Quem realiza | Frequência/criticidade inicial | Status/evidência |
|---|---|---|---|---|
| A01 | Selecionar e carregar uma tomografia computadorizada renal válida | Médico ou técnico autorizado | Frequente; depende do volume de exames | [H] - fluxo proposto a validar |
| A02 | Consultar a classificação e a indicação de possível patologia | Médico | Frequente e alta criticidade | [H] - objetivo de uso a validar |
| A03 | Interpretar a explicação do modelo e decidir como prosseguir com a avaliação clínica | Médico | Frequente e alta criticidade | [H] - objetivo de uso a validar |

## 3.3 Qual atividade parece mais frequente? Por quê?

[H] A seleção e o carregamento de exames tende a ser a atividade mais recorrente, pois inicia cada análise; 

## 3.4 Qual parece mais crítica? Que consequência existe se for mal executada?

[H] Analisar e interpretar o resultado parece ser a atividade mais crítica, pois uma compreensão incorreta da indicação do modelo pode contribuir para uma decisão clínica inadequada. A consequência exata e os mecanismos de revisão precisam ser investigados.

---

# 4. Entendendo o problema ou processo atual

## 4.1 Como essas atividades são realizadas hoje, antes da interface imaginada na disciplina?

Pode existir software concorrente, linha de comando, planilha, notebook, script, painel técnico, processo manual, consulta a logs, análise visual, troca de mensagens, decisão por especialista etc.

[F] Processo manual;
[F] Decisão por especialista.

## 4.2 O que é difícil, demorado, confuso, repetitivo, arriscado ou pouco transparente?

[H] Processo de análise das tomografias, uma vez que está suscetível a erros humanos.

## 4.3 Que informações o profissional precisa interpretar para tomar decisão?

[H] Se os rins estão com a estrutura preservada (contornos regulares)

## 4.4 O que acontece quando a atividade falha ou quando o resultado é interpretado incorretamente?

[F] Um diagnóstico pode ser dado incorretamente.

## 4.5 Conte uma situação concreta.

Escreva uma pequena narrativa com pessoa, objetivo, atividade, contexto, dificuldade e consequência. **Não descreva ainda a futura solução.**

[H] H03 - Um médico recebe uma tomografia computadorizada durante sua rotina de atendimento e precisa avaliar se há sinais compatíveis com uma patologia. Ele observa as imagens e os contornos dos rins, mas trabalha sob pressão de tempo e pode ter dificuldade para identificar alterações sutis. Se a análise for incompleta ou o resultado for interpretado incorretamente, uma suspeita pode não ser investigada ou um diagnóstico pode ser feito de forma inadequada. A situação e suas condições reais ainda precisam ser confirmadas com profissionais.

## 4.6 Que evidência existe hoje?

| Evidência/fonte | O que sustenta | Limitação |
|---|---|---|
| Descrição do TCC e informações fornecidas | O TCC pretende classificar imagens renais, com eficiência computacional e interpretabilidade | Ainda não constitui evidência de uso clínico ou de desempenho em ambiente real |
| Entrevistas ou testes com médicos | PENDENTE - poderão sustentar necessidades e fluxos reais | Ainda não realizados |

---

# 5. Entendendo o contexto de uso

## 5.1 Onde e em quais situações a interação poderia ocorrer?

[H] O uso poderá ocorrer em hospitais, clínicas, laboratórios ou instituições de pesquisa, durante a avaliação de exames de pacientes. O contexto institucional exato ainda não foi definido.

## 5.2 Em quais dispositivos/equipamentos?

[H] A interação poderá ocorrer em um computador de trabalho com monitor adequado para visualização de imagens médicas, por meio de uma interface web ou desktop. O dispositivo e a integração com sistemas de imagem ainda precisam ser definidos.

## 5.3 Existem condições físicas relevantes?

Considere iluminação, ruído, mobilidade, conexão, privacidade, uso compartilhado, interrupções, pressão de tempo etc.

[H] O profissional poderá enfrentar interrupções, pressão de tempo, uso compartilhado do equipamento e necessidade de preservar a privacidade dos exames. 

[F] Imagens médicas são dados sensíveis no contexto da LGPD; os requisitos institucionais e técnicos de proteção ainda precisam ser detalhados.

## 5.4 Existem fatores sociais ou organizacionais?

Considere papéis, chefias, equipes, permissões, aprovação, responsabilidade profissional, auditoria, turnos e colaboração.

[H] A decisão permanece sob responsabilidade do profissional de saúde, podendo envolver colaboração entre radiologistas, médicos solicitantes, técnicos e equipe de TI. Permissões, aprovação, integração com o fluxo institucional e responsabilidades ainda são desconhecidas.

## 5.5 Existe necessidade de histórico, rastreabilidade ou auditoria?

[?] Ainda não foi definido se o protótipo precisará manter histórico de exames, registrar versões do modelo, permitir auditoria ou exportar evidências. Esses requisitos são relevantes para investigar antes de qualquer implementação.

## 5.6 Um erro pode produzir consequência relevante? Qual?

[F] Sim, um diagnóstico incorreto.

---

# 6. Entendendo mercado e alternativas existentes

> Nesta entrega faça apenas um **levantamento inicial**. A análise aprofundada ocorre na Entrega 2.

## 6.1 Como pessoas resolvem problemas semelhantes hoje?

| Alternativa atual | Quem usa | Para quê | Status/evidência |
|---|---|---|---|
| Avaliação visual e interpretação por profissional de saúde | Médico | Analisar as imagens e elaborar uma conclusão diagnóstica | [F] - processo tradicional |
| Sistemas de visualização e gestão de exames médicos | Médicos e equipes de saúde | Consultar, organizar e visualizar exames | [H] - alternativa e vocabulário a investigar |


## 6.2 Existem produtos que atuam na mesma área, mesmo sem serem equivalentes ao TCC?

[?] O levantamento inicial de concorrentes, produtos específicos, critérios de comparação e disponibilidade no contexto do SUS ainda não foi realizado. 

## 6.3 Quais interfaces profissionais esse público já conhece?

Exemplos possíveis: ferramentas de banco, IDEs, consoles de nuvem, dashboards, plataformas de dados, ferramentas de monitoramento, painéis de IA, sistemas administrativos.

[H] sistemas administrativos;
[H] sistemas médicos.

## 6.4 O que essas soluções parecem fazer bem?

[H] Sistemas médicos provavelmente oferecem visualização de imagens, identificação do paciente/exame e organização do fluxo de trabalho. 

## 6.5 O que parecem fazer mal, dificultar ou não atender?

[H] Soluções existentes podem dificultar a compreensão de recomendações automatizadas, a visualização da justificativa do resultado ou a distinção entre apoio computacional e diagnóstico profissional. 

## 6.6 Que padrões de interface ou vocabulário parecem familiares a esse público?

[H] Termos como paciente, exame, tomografia, imagem, achado, suspeita, resultado, confiança e histórico podem ser familiares, mas o vocabulário deve ser validado com médicos. 

---

# 7. Derivando o escopo de IHC da disciplina

## 7.1 Escolha o caminho do projeto

### Caminho A — TCC já possui interface

Explique qual parte da interface será usada como recorte da disciplina e por que esse fluxo é relevante.

O carregamento das tomografias computadorizadas e análise dos resultados gerados pelo modelo.

### Caminho B — TCC não possui interface prevista

Faça o exercício de transferência de uso:

> **Imagine que o TCC foi concluído com sucesso e uma empresa, laboratório ou organização quer transformar a contribuição em algo utilizável. Quem precisaria interagir com ela e para quê?**

Responda:

1. quem poderia contratar/adotar a solução? {{...}}
2. quem seria o usuário direto? {{...}}
3. quem administraria/configuraria? {{...}}
4. quem interpretaria resultados? {{...}}
5. quem tomaria decisões? {{...}}
6. quais dados/entradas seriam necessários? {{...}}
7. quais resultados deveriam ser compreendidos? {{...}}
8. que erros/rupturas seriam possíveis? {{...}}

## 7.2 Qual perfil será priorizado no projeto de IHC?

**Por que esse perfil foi escolhido?** {{...}}

## 7.3 Qual objetivo desse usuário será priorizado?

Interpretar a indicação produzida pelo modelo em conjunto com a tomografia, compreender seus limites e decidir como prosseguir com a investigação clínica.

## 7.4 Que interface será explorada na disciplina?

Complete:

> **Para fins da disciplina de IHC, será projetada uma interface que permita a `médicos` utilizar a `classificação interpretável de tomografias renais produzida pelo modelo` para `analisar possíveis patologias e apoiar a decisão sobre a investigação do exame`, no contexto de `avaliação profissional de tomografias computadorizadas renais`.**

O recorte explorará o fluxo de entrada de uma tomografia, acompanhamento do processamento e leitura do resultado com sua explicação. A interface será tratada como parte prevista do sistema.

## 7.5 Qual é a relação dessa interface com o TCC?

- [x] Já fazia parte do TCC.
- [ ] É um aprofundamento de algo parcialmente previsto.
- [ ] É uma extensão conceitual criada para a disciplina.
- [ ] É um protótipo demonstrativo de aplicação potencial.
- [ ] Outra: {{...}}.

> **Declaração:** a interface desenvolvida nesta disciplina é um artefato de aprendizagem de IHC baseado no tema do TCC. Sua inclusão ou implementação no TCC somente ocorrerá se isso for posteriormente decidido pela equipe e pelo orientador.

---

# 8. Levantando possibilidades de interação — sem desenhar ainda

A equipe pode registrar possibilidades para investigação. **Não significa que todas serão implementadas.**

Marque apenas as que parecem plausíveis e explique o objetivo correspondente.

| Possibilidade | Pode fazer sentido? | Objetivo/tarefa que justificaria | Evidência atual |
|---|---|---|---|
| Dashboard/visão geral | talvez | Acompanhar exames recentes, estados de processamento e pendências | [H] - só se houver mais de um exame no fluxo |
| Configuração/parametrização | talvez | Selecionar modelo ou parâmetros autorizados | ? - depende do perfil administrador |
| Entrada/upload/seleção de dados | sim | Fornecer uma tomografia válida para análise | [H] - fluxo central do recorte |
| Acompanhamento de processamento | sim | Saber se o exame foi recebido, processado ou apresentou erro | [H] - necessário para feedback do sistema |
| Relatório/resultados | sim | Consultar a indicação do modelo e registrar uma conclusão de apoio | [H] - resultado central do TCC |
| Histórico com busca/filtros | talvez | Localizar exames e análises anteriores | ? - necessidade ainda não confirmada |
| Comparação de resultados | talvez | Comparar versões, exames ou resultados quando houver justificativa clínica | ? - fora do primeiro recorte até investigação |
| Explicabilidade/detalhamento | sim | Compreender quais regiões ou características influenciaram a indicação | [H] - interpretabilidade é contribuição declarada |
| Administração/configurações globais | talvez | Manter configurações operacionais do serviço | [H] - depende de adoção institucional |
| Usuários/perfis/permissões | talvez | Restringir acesso a exames e funções conforme responsabilidade | [H] - relevante por privacidade e governança |
| CRUD de entidade do domínio | não inicialmente | Não há entidade administrativa necessária no recorte atual | [F] - não deriva de uma tarefa já identificada |
| Auditoria/logs | talvez | Rastrear processamento, versão do modelo e acesso aos resultados | [H] - relevância provável, ainda não validada |
| Alertas/ocorrências | talvez | Informar falhas, resultado inconclusivo ou necessidade de revisão | [H] - depende dos modos de falha confirmados |
| Ajuda/documentação | sim | Explicar termos, limitações e interpretação responsável do resultado | [H] - necessário para reduzir ambiguidades |

> **Atenção:** “login + dashboard + CRUD” não é uma solução universal. Cada padrão deve surgir de uma tarefa real.

---

# 9. Benefícios e ações iniciais

## 9.1 Qual benefício concreto o projeto de IHC pretende oferecer?

| Benefício esperado | Problema/necessidade | Usuário | Status/evidência |
|---|---|---|---|
| Apoiar a análise de tomografias renais com uma indicação interpretável | Processo manual sujeito a limitações e risco de interpretação incorreta | Médico | [H] - contribuição e problema declarados |

## 9.2 Que ações o usuário deverá conseguir realizar?

| ID | O usuário precisa conseguir... | Para alcançar... | Prioridade inicial |
|---|---|---|---|
| F01 | Carregar uma tomografia renal e confirmar os dados do exame | Iniciar uma análise válida | alta |
| F02 | Acompanhar o processamento e identificar falhas | Saber quando o resultado está disponível ou precisa de correção | alta |
| F03 | Consultar a classificação, a confiança e a explicação do modelo | Interpretar a indicação como apoio à avaliação médica | alta |
| F04 | Registrar ou comunicar a conclusão da avaliação | Dar continuidade ao atendimento com rastreabilidade adequada | média |

## 9.3 Tecnologias/restrições já definidas no TCC

A tecnologia aparece **agora**, depois do entendimento do uso.

| Tecnologia/restrição | Por que existe | Possível impacto na interação |
|---|---|---|
| Modelo de IA baseado em redes convolucionais | Detectar/classificar patologias em imagens renais com baixo custo computacional | Pode exigir mensagens de processamento, indicação de limitações e apresentação cuidadosa da confiança |
| Interpretabilidade do modelo | Permitir compreender os fatores associados ao resultado | Exige visualização ou descrição explicativa que não seja confundida com prova diagnóstica |
| Dados de tomografia computadorizada | São a entrada necessária para o modelo | Exige validação de formato, qualidade, privacidade e identificação do exame |

---

# 10. Hipóteses e dúvidas prioritárias

| ID | Hipótese/dúvida | Por que importa | Como poderá ser investigada |
|---|---|---|---|
| H01 | Médicos compreenderão e considerarão útil uma explicação do resultado do modelo apresentada junto à imagem | A aceitação depende da compreensão e da confiança na indicação | Entrega 3/7 |
| H02 | O fluxo de upload, processamento e resultado representa uma atividade real e relevante no contexto profissional | Define o recorte de IHC e evita criar telas sem tarefa correspondente | Entrega 3/4/5 |
| H03 | O médico distinguirá claramente a indicação do modelo do diagnóstico final | Um erro de interpretação pode produzir consequência clínica relevante | Entrega 4/7/8 |

Registre em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

---

# 11. Síntese da equipe

| Pergunta | Síntese atual |
|---|---|
| Qual é a contribuição central do TCC? | Classificar imagens de tomografias renais com baixo custo computacional e oferecer interpretabilidade para apoiar a aplicabilidade clínica. |
| O TCC já previa interface? | Sim; a forma final da interface ainda precisa ser detalhada. |
| Quem é o usuário prioritário de IHC? | Médico radiologista ou especialista responsável pela interpretação do exame. |
| O que ele precisa alcançar? | Analisar a tomografia, compreender a indicação do modelo e decidir como prosseguir com a avaliação clínica. |
| Qual problema/atividade será estudado? | O carregamento de tomografias e a interpretação de resultados de apoio ao diagnóstico. |
| Como isso acontece hoje? | Por análise visual e decisão de especialista, em processo declarado como manual. |
| Qual é o contexto de uso? | Ambiente profissional de saúde, com possível pressão de tempo, dados sensíveis e responsabilidade clínica. |
| Que interface/recorte será explorado? | Entrada do exame, acompanhamento do processamento e resultado explicável. |
| Como a interface se relaciona ao TCC? | É uma interface prevista no sistema descrito e será refinada como recorte de IHC; a implementação no TCC ainda depende de decisão. |
| Quais pontos ainda são hipóteses? | H01, H02, H03 e as demais afirmações marcadas `[H]`; ainda faltam dados com médicos e levantamento de alternativas. |

### Delimitação

**Dentro do escopo de IHC:** investigar, modelar, prototipar e avaliar o fluxo de carregamento de tomografias, acompanhamento do processamento e interpretação explicável do resultado por médicos.  
**Fora do escopo de IHC:** desenvolver toda a infraestrutura clínica, validar o modelo em larga escala, definir protocolos médicos, substituir o diagnóstico profissional, integrar todos os sistemas hospitalares e criar uma área administrativa completa.  
**Dentro do escopo formal do TCC:** desenvolver e avaliar o modelo de detecção/classificação de patologias renais em tomografias, considerando desempenho, eficiência computacional e interpretabilidade, conforme o escopo declarado pela equipe.  
**Interface da disciplina será implementada no TCC?** não definido - a interface é um recorte previsto para a disciplina e sua incorporação ao TCC depende de decisão da equipe e da orientadora.

---

# 12. Como esta entrega alimenta as próximas

- **Entrega 2:** verifica mercado, concorrentes e interfaces profissionais representativas.
- **Entrega 3:** detalha perfis e contexto.
- **Entrega 4:** aprofunda situações problemáticas.
- **Entrega 5:** modela tarefas centrais.
- **Entrega 6:** experimenta alternativas em baixa fidelidade.
- **Entrega 7:** investiga hipóteses com dados.
- **Entrega 8:** define restrições e metas de usabilidade.
- **Entregas 9–11:** transformam o recorte em modelo de interação e protótipo.
- **Entregas 12–14:** avaliam a interface construída na disciplina.

A Entrega 1 é uma **fotografia inicial do conhecimento**. Ela pode e deve ser revisada quando surgirem evidências.

---

# 13. Relação com INOVA e comunicação do projeto

Prepare uma explicação de até três frases:

1. **Problema/atividade humana:** Médicos precisam analisar tomografias renais e identificar possíveis patologias, inclusive alterações que podem ser difíceis de perceber em uma análise manual.
2. **Contribuição técnica do TCC:** Um modelo de redes convolucionais classifica imagens renais buscando baixo custo computacional e interpretabilidade.
3. **Como uma pessoa poderia utilizar essa contribuição:** Um médico poderia carregar uma tomografia, consultar a indicação e a explicação do modelo e usar essas informações como apoio, sem substituir sua avaliação clínica.

Essa síntese ajuda a apresentar o projeto para público não especializado sem reduzir seu mérito técnico.

---

# Checklist de qualidade

- [x] Está clara a diferença entre tema do TCC, escopo formal do TCC e escopo de IHC.
- [x] A equipe declarou se o TCC já previa interface.
- [ ] Se não previa, foi derivado um usuário plausível e um objetivo de uso.
- [x] A interface de IHC não foi apresentada como obrigação automática do TCC.
- [x] A contribuição do TCC foi descrita sem começar por tecnologias de implementação.
- [x] Usuários diretos e stakeholders foram diferenciados.
- [x] Foram considerados profissionais que configuram, administram, interpretam ou decidem, quando pertinente.
- [x] Objetivo do usuário não foi confundido com objetivo do projeto.
- [x] Processo/problema atual foi descrito antes da solução.
- [x] Existe situação concreta de uso/problema.
- [x] Contexto físico, social/organizacional, dispositivos e consequências de erro foram considerados.
- [x] Mercado/alternativas existentes foram levantados inicialmente.
- [x] Possibilidades como dashboard, relatório, histórico, filtros e CRUD foram tratadas como hipóteses de solução, não como requisitos automáticos.
- [x] Cada possibilidade de interface tem um objetivo/tarefa que poderia justificá-la.
- [x] Afirmações relevantes estão marcadas `[F]`, `[H]` ou `[?]`.
- [x] Hipóteses prioritárias receberam IDs e foram para a rastreabilidade.
- [x] O recorte de IHC é viável para modelar, prototipar e avaliar no semestre.
- [x] A equipe consegue explicar problema humano → contribuição computacional → forma de uso.
