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

[?] A situação concreta do processo clínico que motivaria a intervenção ainda não foi identificada. Será necessário investigar com profissionais como tomografias renais são avaliadas e se há dificuldades ou oportunidades relevantes nessa atividade.

[F] A escolha do tema também foi motivada pela experiência pessoal da equipe com pessoas próximas acometidas por Doença Renal Crônica (DRC). Esse relato explica a motivação da equipe, mas não constitui evidência sobre o processo clínico.

## 1.3 Qual é a **capacidade/contribuição central** produzida pelo TCC?

Complete, se ajudar:

> “Nosso TCC produz, melhora, analisa ou permite `{{capacidade}}`.”

Exemplos: otimizar consultas; classificar imagens; detectar anomalias; comparar modelos; identificar padrões; prever demanda; analisar desempenho; gerar resumos; recomendar configurações.

O TCC produz um modelo de redes convolucionais para classificar imagens de tomografias renais, com foco em eficiência computacional e análise de interpretabilidade.

## 1.4 O que se espera que esteja diferente **para pessoas, organizações ou processos** se essa contribuição for bem-sucedida?

[H] Se o modelo demonstrar desempenho, eficiência e interpretabilidade adequados, poderá apoiar a análise de tomografias renais em contextos com recursos computacionais limitados; a acessibilidade e o benefício clínico ainda não foram demonstrados.

[H] A possibilidade de contribuir para a identificação mais precoce de patologias renais é um benefício esperado, mas ainda não foi demonstrada por evidências desta entrega.
 

## 1.5 O que é mérito técnico/científico do TCC e o que seria uma possível aplicação prática?

| Mérito/contribuição técnica | Possível aplicação/valor em uso |
|---|---|
| Classificação de imagens médicas renais com redes convolucionais de baixo custo computacional e análise de interpretabilidade | Apoiar médicos na análise de tomografias computadorizadas, oferecendo uma indicação complementar para a avaliação de possíveis patologias renais. |

---

# 2. Entendendo as pessoas envolvidas

## 2.1 Quem interage diretamente com o produto, se já existe interface prevista?

Se não houver interface prevista no TCC, escreva `NÃO SE APLICA AO ESCOPO ORIGINAL` e prossiga para 2.2.

[F] Perfil prioritário inicial definido pela equipe para o projeto de IHC: médico nefrologista. A adequação desse perfil ao uso da solução ainda será validada com profissionais.

## 2.2 Quem poderia **usar, configurar, administrar, operar, interpretar ou tomar decisões** a partir da contribuição técnica?

Considere perfis profissionais e stakeholders, não apenas consumidores finais.

| Perfil | Relação com a contribuição | O que faria | Status/evidência |
|---|---|---|---|
| Médico nefrologista | Usuário direto potencial e intérprete do resultado no recorte inicial | Poderia avaliar a tomografia e considerar os resultados do modelo ao decidir como prosseguir; quais informações consultaria e quem forneceria o exame ainda precisam ser investigados (H02, H06) | [H] - perfil escolhido inicialmente pela equipe, a confirmar com profissionais |
| Pesquisador ou profissional de IA/ML | Responsável técnico pela avaliação do modelo | Configuraria versões do modelo, parâmetros e conjuntos de avaliação | [H] - cenário de adoção |
| Profissional de TI ou administrador do serviço | Operação e manutenção da solução | Administraria acesso, disponibilidade e integração com o fluxo institucional | [H] - cenário de adoção |

## 2.3 Existem pessoas afetadas que não usariam a interface diretamente?

| Stakeholder | Como é afetado | Usa interface? | Status/evidência |
|---|---|---|---|
| Paciente | Exames de imagem avaliados | não | [H] - impacto depende da adoção clínica da solução |

## 2.4 Que características desses perfis podem influenciar a interação?

Considere conhecimento do domínio, experiência tecnológica, frequência de uso, necessidades de acessibilidade, responsabilidade profissional, familiaridade com métricas, linguagem técnica, urgência etc.

[H] H04 - O médico nefrologista poderá ter familiaridade com sistemas de visualização de exames, mas não necessariamente com métricas de aprendizado de máquina; essa experiência e suas necessidades de apresentação ainda precisam ser investigadas.

[H] H03 - O médico nefrologista distinguirá claramente a indicação do modelo do diagnóstico final; essa distinção e a forma de comunicar responsabilidades e limites precisam ser investigadas.

[?] Ainda não se sabe a frequência de uso, o nível de experiência tecnológica dos profissionais, os requisitos de acessibilidade e quais termos clínicos são preferidos.

---

# 3. Entendendo objetivos e atividades

## 3.1 O que o usuário está tentando conseguir no mundo real?

Não responda “usar o algoritmo”, “clicar no sistema” ou “ver o dashboard”.

[?] Ainda não há evidência nesta entrega sobre dificuldades específicas na avaliação de tomografias renais, nem sobre a possibilidade de identificar patologias em estágios iniciais. A atividade e as necessidades dos profissionais precisam ser investigadas.

## 3.2 Quais são as atividades mais importantes?

| ID | Atividade/objetivo | Quem realiza | Frequência/criticidade inicial | Status/evidência |
|---|---|---|---|---|
| A01 | Avaliar uma tomografia renal e interpretar possíveis achados | Médico nefrologista (perfil inicial) | Frequência e criticidade a investigar | [H] - atividade profissional a validar |
| A02 | Decidir como prosseguir diante dos achados da avaliação | Médico nefrologista (perfil inicial) | Criticidade e processo decisório a investigar | [H] - atividade profissional a validar |
| A03 | Interpretar a indicação e a explicação do modelo como apoio à avaliação clínica | Médico nefrologista (perfil inicial) | Frequência e criticidade a investigar | [H] - objetivo de uso proposto, a validar |

## 3.3 Qual atividade parece mais frequente? Por quê?

[?] Ainda não é possível determinar qual atividade é mais frequente; isso depende do volume de exames e da rotina profissional, que ainda não foram investigados.

## 3.4 Qual parece mais crítica? Que consequência existe se for mal executada?

[H] Analisar e interpretar o resultado parece ser a atividade mais crítica, pois uma compreensão incorreta da indicação do modelo pode contribuir para uma decisão clínica inadequada. A consequência exata e os mecanismos de revisão precisam ser investigados.

---

# 4. Entendendo o problema ou processo atual

## 4.1 Como essas atividades são realizadas hoje, antes da interface imaginada na disciplina?

Pode existir software concorrente, linha de comando, planilha, notebook, script, painel técnico, processo manual, consulta a logs, análise visual, troca de mensagens, decisão por especialista etc.

[?] A forma como os profissionais avaliam tomografias renais atualmente ainda não foi descrita nem sustentada por evidências nesta entrega. A avaliação visual e a decisão por especialista são possibilidades a investigar com profissionais.

## 4.2 O que é difícil, demorado, confuso, repetitivo, arriscado ou pouco transparente?

[H] Processo de análise das tomografias, uma vez que está suscetível a erros humanos.

## 4.3 Que informações o profissional precisa interpretar para tomar decisão?

[H] Se os rins estão com a estrutura preservada (contornos regulares)

## 4.4 O que acontece quando a atividade falha ou quando o resultado é interpretado incorretamente?

[H] Uma avaliação ou interpretação incorreta poderia contribuir para uma decisão clínica inadequada; a ocorrência, as consequências e os mecanismos de revisão precisam ser investigados.

## 4.5 Conte uma situação concreta.

Escreva uma pequena narrativa com pessoa, objetivo, atividade, contexto, dificuldade e consequência. **Não descreva ainda a futura solução.**

[H] H05 - Um médico recebe uma tomografia computadorizada durante sua rotina de atendimento e precisa avaliar se há sinais compatíveis com uma patologia. A rotina, a eventual pressão de tempo, a dificuldade para identificar alterações e as possíveis consequências de uma avaliação incompleta ainda são hipóteses a confirmar com profissionais.

## 4.6 Que evidência existe hoje?

| Evidência/fonte | O que sustenta | Limitação |
|---|---|---|
| Descrição do TCC e informações fornecidas | O TCC pretende classificar imagens renais, com eficiência computacional e interpretabilidade | Ainda não constitui evidência de uso clínico ou de desempenho em ambiente real |
| Entrevistas ou testes com médicos | PENDENTE - poderão sustentar necessidades e fluxos reais | Ainda não realizados |

---

# 5. Entendendo o contexto de uso

## 5.1 Onde e em quais situações a interação poderia ocorrer?

[H] O uso poderá ocorrer em hospitais, clínicas, laboratórios ou instituições de pesquisa, durante a avaliação de exames de pacientes. Ainda precisam ser investigados o contexto institucional, a rotina e as etapas da avaliação, os profissionais envolvidos, quem fornece o exame, os sistemas utilizados e as condições de trabalho. Essas possibilidades não definem requisitos da interface.

## 5.2 Em quais dispositivos/equipamentos?

[H] A interação poderá ocorrer em um computador de trabalho com monitor adequado para visualização de imagens médicas, por meio de uma interface web ou desktop. O dispositivo e a integração com sistemas de imagem ainda precisam ser definidos.

## 5.3 Existem condições físicas relevantes?

Considere iluminação, ruído, mobilidade, conexão, privacidade, uso compartilhado, interrupções, pressão de tempo etc.

[H] O profissional poderá enfrentar interrupções, pressão de tempo, uso compartilhado do equipamento e necessidade de preservar a privacidade dos exames.

[F] Dados referentes à saúde são dados pessoais sensíveis conforme a LGPD (Lei nº 13.709/2018, art. 5º, II; referência em [`../BIBLIOGRAFIA.md`](../BIBLIOGRAFIA.md)). Os requisitos institucionais e técnicos de proteção ainda precisam ser detalhados.

## 5.4 Existem fatores sociais ou organizacionais?

Considere papéis, chefias, equipes, permissões, aprovação, responsabilidade profissional, auditoria, turnos e colaboração.

[H] A decisão permanece sob responsabilidade do profissional de saúde, podendo envolver colaboração entre radiologistas, médicos solicitantes, técnicos e equipe de TI. Permissões, aprovação, integração com o fluxo institucional e responsabilidades ainda são desconhecidas.

## 5.5 Existe necessidade de histórico, rastreabilidade ou auditoria?

[?] Ainda não foi definido se o protótipo precisará manter histórico de exames, registrar versões do modelo, permitir auditoria ou exportar evidências. Esses requisitos são relevantes para investigar antes de qualquer implementação.

## 5.6 Um erro pode produzir consequência relevante? Qual?

[H] Uma avaliação incorreta poderia contribuir para uma decisão clínica inadequada; a consequência concreta e os mecanismos de revisão ainda precisam ser investigados.

---

# 6. Entendendo mercado e alternativas existentes

> Nesta entrega faça apenas um **levantamento inicial**. A análise aprofundada ocorre na Entrega 2.

## 6.1 Como pessoas resolvem problemas semelhantes hoje?

| Alternativa atual | Quem usa | Para quê | Status/evidência |
|---|---|---|---|
| Avaliação visual e interpretação por profissional de saúde | Médico | Analisar as imagens e elaborar uma conclusão diagnóstica | [H] - processo atual a confirmar com profissionais |
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

**Perfil prioritário inicial:** médico nefrologista.

**Por que esse perfil foi escolhido?** A equipe escolheu inicialmente o nefrologista por ser o especialista médico dedicado ao diagnóstico, à prevenção e ao tratamento clínico das doenças do sistema urinário, com foco nos rins. Essa é uma decisão inicial de recorte, não uma confirmação de que esse profissional será o usuário da solução; a adequação do perfil e sua relação com a avaliação de tomografias precisam ser validadas com profissionais.

## 7.3 Qual objetivo desse usuário será priorizado?

Interpretar a indicação produzida pelo modelo em conjunto com a tomografia, compreender seus limites e decidir como prosseguir com a investigação clínica.

## 7.4 Que interface será explorada na disciplina?

Complete:

> **Para fins da disciplina de IHC, será projetada uma interface que permita a `médicos nefrologistas` utilizar a `classificação de tomografias renais produzida pelo modelo e sua explicação` para `analisar possíveis patologias e decidir como prosseguir com a avaliação clínica`, no contexto de `avaliação profissional de tomografias computadorizadas renais`.**

O recorte proposto explora a entrada de uma tomografia, o acompanhamento do processamento e a leitura do resultado com sua explicação. O envio manual do exame é uma hipótese de interação (H02): ainda é necessário investigar quem fornece o exame, quais profissionais participam e se esse fluxo corresponde à prática existente ou se o exame chega por outro sistema.

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
| CRUD de entidade do domínio | não inicialmente | Nenhuma tarefa administrativa foi identificada no recorte inicial | [H] - rever se a investigação apontar essa necessidade |
| Auditoria/logs | talvez | Rastrear processamento, versão do modelo e acesso aos resultados | [H] - relevância provável, ainda não validada |
| Alertas/ocorrências | talvez | Informar falhas, resultado inconclusivo ou necessidade de revisão | [H] - depende dos modos de falha confirmados |
| Ajuda/documentação | sim | Explicar termos, limitações e interpretação responsável do resultado | [H] - necessário para reduzir ambiguidades |

> **Atenção:** “login + dashboard + CRUD” não é uma solução universal. Cada padrão deve surgir de uma tarefa real.

---

# 9. Benefícios e ações iniciais

## 9.1 Qual benefício concreto o projeto de IHC pretende oferecer?

| Benefício esperado | Problema/necessidade | Usuário | Status/evidência |
|---|---|---|---|
| Investigar se uma indicação interpretável pode apoiar a avaliação de tomografias renais | Necessidade e dificuldades no processo atual ainda não foram confirmadas | Médico nefrologista (perfil inicial) | [H] - benefício a validar com profissionais |

## 9.2 Que ações o usuário deverá conseguir realizar?

| ID | O usuário precisa conseguir... | Para alcançar... | Prioridade inicial |
|---|---|---|---|
| F01 | Fornecer uma tomografia renal válida à solução, por forma de entrada ainda a confirmar | Iniciar uma análise válida | alta |
| F02 | Acompanhar o processamento e identificar falhas | Saber quando o resultado está disponível ou precisa de correção | alta |
| F03 | Consultar os elementos do resultado que a investigação confirmar como necessários, distinguindo classificação do modelo, eventual medida de confiança e explicação | Interpretar a indicação como apoio à avaliação médica, sem confundi-la com a conclusão clínica | proposta; validar H01, H03 e H06 |
| F04 | Registrar ou comunicar a conclusão da avaliação | Dar continuidade ao atendimento com rastreabilidade adequada | média |

Classificação, medida de confiança, explicação do modelo e conclusão clínica são elementos distintos. Ainda não foi confirmado quais deles são produzidos pelo TCC, quais seriam úteis ao nefrologista, como seriam interpretados ou se deveriam aparecer na interface. Em particular, a presença de uma explicação não garante que ela seja compreendida ou considerada útil, e uma medida de confiança não deve ser presumida como necessária ou autoexplicativa. Investigar essas questões antes de defini-las como requisitos (H01, H03, H06).

## 9.3 Tecnologias/restrições já definidas no TCC

A tecnologia aparece **agora**, depois do entendimento do uso.

| Tecnologia/restrição | Por que existe | Possível impacto na interação |
|---|---|---|
| Modelo de IA baseado em redes convolucionais | Detectar/classificar patologias em imagens renais com baixo custo computacional | Se houver medida de confiança entre as saídas do modelo, sua necessidade, compreensão e forma de apresentação deverão ser investigadas; também será necessário comunicar limitações relevantes |
| Interpretabilidade do modelo | Analisar fatores associados ao resultado, conforme o método definido no TCC | A forma de explicação, sua apresentação e compreensão pelo nefrologista precisam ser investigadas; não deve ser presumida como prova diagnóstica |
| Dados de tomografia computadorizada | São a entrada necessária para o modelo | Exige validação de formato, qualidade, privacidade e identificação do exame |

---

# 10. Hipóteses e dúvidas prioritárias

| ID | Hipótese/dúvida | Por que importa | Como poderá ser investigada |
|---|---|---|---|
| H01 | Médicos nefrologistas compreenderão e considerarão útil uma explicação do resultado do modelo apresentada junto à imagem | A compreensão e a utilidade precisam ser verificadas; interpretabilidade não garante compreensão, utilidade ou confiança | Entrega 3/7 |
| H02 | O fluxo de fornecimento do exame, processamento e resultado representa uma atividade real e relevante no contexto profissional; é necessário descobrir quem fornece o exame e por qual meio | Define o recorte de IHC e os papéis envolvidos sem pressupor upload manual | Entrega 3/4/5 |
| H03 | O médico nefrologista distinguirá claramente a indicação do modelo do diagnóstico final | Uma interpretação equivocada poderia afetar a avaliação clínica; a consequência concreta precisa ser investigada | Entrega 4/7/8 |
| H04 | O médico nefrologista poderá ter familiaridade com sistemas de visualização de exames, mas não necessariamente com métricas de aprendizado de máquina | A experiência e as necessidades de apresentação podem orientar o vocabulário e o nível de detalhe | Entrega 3/7 |
| H05 | A rotina de avaliação de tomografias poderá envolver pressão de tempo ou dificuldade para identificar alterações sutis; instituição, etapas, papéis, sistemas e condições ainda são desconhecidos | O contexto e as dificuldades reais podem alterar o problema e o recorte de IHC | Entrega 3/4 |
| H06 | Classificação, medida de confiança e explicação do modelo são elementos distintos; quais são produzidos, necessários e compreendidos pelo nefrologista ainda precisa ser investigado | Evita tratar elementos diferentes como equivalentes ou presumir que todos devam ser apresentados na interface | Entrega 3/7 |

Registre em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

---

# 11. Síntese da equipe

| Pergunta | Síntese atual |
|---|---|
| Qual é a contribuição central do TCC? | Classificar imagens de tomografias renais com baixo custo computacional e oferecer interpretabilidade para apoiar a aplicabilidade clínica. |
| O TCC já previa interface? | Sim; a forma final da interface ainda precisa ser detalhada. |
| Quem é o usuário prioritário de IHC? | Médico nefrologista, escolhido inicialmente pela equipe; a adequação do perfil será validada com profissionais. |
| O que ele precisa alcançar? | Como objetivo proposto, avaliar a tomografia, interpretar possíveis achados e decidir como prosseguir; a atividade real será investigada. |
| Qual problema/atividade será estudado? | A avaliação profissional de tomografias renais; dificuldades e processo atual ainda precisam ser investigados. |
| Como isso acontece hoje? | Ainda não há evidência suficiente nesta entrega para descrever o processo atual. |
| Qual é o contexto de uso? | Avaliação profissional de tomografias renais; instituição, rotina, etapas, papéis, sistemas e condições específicas ainda precisam ser investigados. |
| Que interface/recorte será explorado? | Recorte inicial proposto: fornecimento do exame, acompanhamento do processamento e consulta ao resultado; forma de entrada e elementos a apresentar permanecem nas hipóteses H02 e H06. |
| Como a interface se relaciona ao TCC? | É uma interface prevista no sistema descrito e será refinada como recorte de IHC; a implementação no TCC ainda depende de decisão. |
| Quais pontos ainda são hipóteses? | H01–H06 e as demais afirmações marcadas `[H]`; ainda faltam dados com profissionais e levantamento de alternativas. |

### Delimitação

**Dentro do escopo de IHC:** investigar, modelar, prototipar e avaliar o recorte inicial proposto de fornecimento do exame, acompanhamento do processamento e consulta ao resultado por médicos nefrologistas; o fluxo e os elementos do resultado ainda serão validados (H02, H06).

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

1. **Problema/atividade humana:** A avaliação profissional de tomografias renais e as dificuldades enfrentadas nessa atividade ainda precisam ser investigadas; a equipe não dispõe de evidência para afirmar que alterações sejam difíceis de perceber ou que haja pressão de tempo.
2. **Contribuição técnica do TCC:** Um modelo de redes convolucionais classifica imagens renais buscando baixo custo computacional e interpretabilidade.
3. **Como uma pessoa poderia utilizar essa contribuição:** Um médico nefrologista poderia consultar a indicação e a explicação do modelo como apoio à avaliação clínica; a forma de entrada do exame ainda é uma hipótese a validar.

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
