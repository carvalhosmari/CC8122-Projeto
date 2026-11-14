# Entrega 7 — Coleta de dados, necessidades e aspectos éticos

**Data:** 14/11/2026  
**Status:** 🟩 concluída

## Objetivo da atividade

Planejar dados necessários para compreender usuários e requisitos de IHC, escolher técnicas adequadas e documentar instrumentos de modo que a aplicação possa ser reproduzida por pessoas diferentes.

## Para escopos de IHC derivados de TCC técnico

Quando o usuário e a interface foram propostos pela disciplina, uma prioridade da coleta é investigar se esse **cenário de uso realmente faz sentido**. Não trate o exercício de comercialização da Entrega 1 como validação de mercado.

Perguntas úteis incluem:

- esse perfil realmente realiza a atividade imaginada?
- quais ferramentas usa hoje?
- quais informações consulta?
- quais decisões toma?
- que vocabulário utiliza?
- quais parâmetros compreende e quais deveriam ser abstraídos?
- precisa de dashboard, histórico, filtros, relatórios ou comparação? Por quê?
- quais erros são frequentes e quais são críticos?
- existem papéis/permissões diferentes?
- que resultados do algoritmo/modelo seriam úteis ou difíceis de interpretar?

Quando o acesso ao perfil profissional for difícil, discuta com o docente alternativas metodológicas (especialistas próximos, dados secundários, literatura, participantes proxy) e registre as limitações. **Não esconda a limitação da amostra.**

## Hipóteses e lacunas prioritárias herdadas da Entrega 1

Antes de decidir “que dados coletar”, retome os itens `[H]` e `[?]` da Entrega 1 e o registro de hipóteses em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md). A coleta deve responder perguntas reais do projeto, e não apenas produzir um formulário porque a técnica foi solicitada.

| ID | Hipótese/lacuna | Evidência atual | Decisão que depende da resposta | Prioridade |
|---|---|---|---|---|
| H02 | O fluxo proposto de fornecimento do exame, processamento e consulta do resultado corresponde a uma atividade real? Quem fornece o exame e por qual meio? | Fluxo proposto na Entrega 1; papéis, meios de fornecimento e relevância na rotina ainda não foram validados com profissionais. | Confirmar ou ajustar o recorte de IHC, as etapas do fluxo e os perfis envolvidos, sem pressupor upload manual. | alta |
| H04 | Nefrologistas têm familiaridade com visualizadores de exames, mas não necessariamente com métricas de aprendizado de máquina? | Suposição registrada na Entrega 1; experiência com sistemas e métricas ainda não investigada com nefrologistas. | Definir vocabulário e nível de detalhe das informações apresentadas na interface. | média |
| H05 | A avaliação de tomografias envolve pressão de tempo ou dificuldade para identificar alterações sutis? Quais são as etapas, os papéis, os sistemas e as condições reais? | Contexto e dificuldades propostos na Entrega 1; instituição, rotina e condições de avaliação ainda não foram confirmadas com profissionais. | Confirmar ou reformular o cenário de uso e priorizar tarefas e informações conforme as dificuldades reais. | alta |
| H07 | É necessário consultar exames anteriores ou filtrar um histórico dentro da solução? | Entrega 2 registra histórico e filtros em Shosp e Nav Pro; isso não demonstra a necessidade dessas tarefas no fluxo de tomografias renais. | Decidir se consulta a exames anteriores ou filtros devem integrar o escopo, sem adotá-los apenas por analogia com outras interfaces. | média |

## Parte A — necessidades e requisitos de IHC

> **Responsabilidade:** solução individual por integrante.

### A01 — Mariane S. Carvalho

**Autor(a):** Mariane S. Carvalho RA: 22.123.105-3

#### Que dados coletar?

| Dado/informação | Hipótese/lacuna relacionada | Por que é necessário | Qual decisão de design pode afetar |
|---|---|---|---|
| Dados sobre o próprio usuário: especialidade, formação e experiência profissional; familiaridade com leitura de laudos e informações técnicas. Não coletar idade, sexo ou condição socioeconômica sem justificativa específica. | H02, H04, H05 | Identificar se o perfil escolhido participa da avaliação de tomografias renais e contextualizar diferenças de experiência, sem solicitar dados pessoais sem finalidade definida. | Definição dos perfis atendidos, da linguagem e do nível de orientação na interface. |
| Dados sobre sua relação com tecnologia: sistemas e equipamentos usados para acessar exames, frequência de uso, experiência com visualizadores e ferramentas de apoio à avaliação. | H02, H04, H05, H07 | Entender como o exame chega ao profissional, quais ferramentas já utiliza e se a consulta a exames anteriores ocorre em outros sistemas. | Integração com o fluxo existente, forma de acesso aos exames e eventual necessidade de histórico na solução. |
| Dados sobre seu conhecimento do domínio: experiência na avaliação de tomografias renais e familiaridade com métricas de aprendizado de máquina. | H04 | Distinguir conhecimento clínico de conhecimento técnico para não presumir que o nefrologista compreenda métricas do modelo. | Vocabulário, explicações e nível de detalhe técnico exibido. |
| Dados sobre suas tarefas: objetivos e etapas da avaliação, quem fornece o exame e por qual meio, papéis envolvidos, tempo disponível, dificuldades e uso de exames anteriores. | H02, H05, H07 | Verificar se o fluxo proposto corresponde à rotina real e se pressão de tempo, alterações sutis e consulta ao histórico são necessidades concretas. | Recorte das etapas e ações da interface, priorização de informações e decisão sobre histórico e filtros. |
| Dados sobre suas motivações e valores: disposição para adotar uma ferramenta de apoio, preferência por orientação ou exploração autônoma e tempo disponível para aprender a utilizá-la. | H02, H04, H05 | Compreender condições de adoção no trabalho e necessidade de apoio ao aprendizado, sem confundir preferência declarada com validação do fluxo. | Forma de introduzir a ferramenta, recursos de orientação e complexidade da interação. |

#### De quem coletar?

| Perfil/stakeholder | Critério de inclusão | Relação com persona/público |
|---|---|---|
| Médicos nefrologistas | Atuam ou já atuaram na avaliação clínica de pacientes com exames de tomografia renal; incluir profissionais com diferentes níveis de experiência e familiaridade com sistemas de exames. | Público principal proposto para a interface e perfil da proto-persona P01; permite investigar H02, H04, H05 e H07 sem presumir que utilize diretamente o modelo. |
| Médicos radiologistas envolvidos com tomografias renais | Interpretam ou emitem laudos de tomografias renais na rotina profissional. | Ajudam a identificar quem efetivamente avalia as imagens, quais informações chegam ao nefrologista e como exames anteriores são consultados; contribuem para H02, H05 e H07, sem substituir o público principal. |
| Profissionais que disponibilizam ou gerenciam exames de imagem | Participam diretamente do recebimento, armazenamento ou disponibilização de tomografias para avaliação clínica, como profissionais do serviço de imagem ou responsáveis pelo sistema de exames. | Informam etapas, meios de fornecimento, sistemas e papéis do fluxo real; contribuem sobretudo para H02 e H05 e, quando pertinente, H07. |

#### Aspectos éticos

Analise voluntariedade, consentimento, minimização de dados, privacidade, riscos, gravação, anonimização, armazenamento e descarte. Não responda apenas “sim, por causa da LGPD”: explique **quais dados e riscos existem neste projeto**.

O convite a nefrologistas, radiologistas e profissionais do fluxo de exames deve deixar claro que a participação é voluntária, sem remuneração ou consequência profissional pela recusa ou desistência. Antes da coleta, apresentar a finalidade acadêmica, os temas abordados, o tempo estimado, quem terá acesso às respostas e como serão usadas; registrar o consentimento informado e permitir que o participante deixe de responder itens. Se o recrutamento ocorrer por intermédio de uma instituição, obter as autorizações exigidas por ela e evitar que chefias tenham acesso a respostas individuais.

Coletar apenas informações necessárias para investigar H02, H04, H05 e H07: função, experiência, sistemas utilizados e descrição da rotina. Não solicitar nome, registro profissional, instituição identificável, idade, sexo ou condição socioeconômica sem justificativa. Não pedir imagens, laudos, identificadores ou histórias clínicas de pacientes. Caso exemplos de casos reais apareçam espontaneamente, orientar o participante a omitir dados identificáveis e não registrar detalhes que permitam reconhecer pacientes ou colegas. A participação não envolve tomar decisões clínicas nem avaliar o desempenho profissional.

Há risco de identificação indireta de especialistas em equipes pequenas e de exposição de dificuldades de trabalho, sistemas ou processos institucionais. Por isso, separar eventuais dados de contato das respostas, usar códigos para os participantes, restringir o acesso aos integrantes responsáveis pela coleta e divulgar somente resultados agregados ou trechos revisados para remover identificadores. Não chamar os dados brutos de anônimos quando ainda puderem ser associados a uma pessoa ou instituição.

O questionário deve ser aplicado sem gravação. Se outra técnica exigir áudio ou vídeo, pedir autorização específica, oferecer participação sem gravação e proteger e apagar o arquivo após a transcrição e conferência. Armazenar respostas e termos de consentimento separadamente, em local com acesso restrito à equipe, sem compartilhar dados brutos em repositórios públicos. Informar no termo o prazo de guarda e o procedimento de descarte; ao fim desse prazo, excluir respostas identificáveis e gravações, mantendo apenas sínteses não identificáveis necessárias ao trabalho.

> Repita A02, A03...

## Parte B — ferramentas de coleta

> Cada integrante deve preparar uma técnica/instrumento completo. As técnicas devem ser diferentes entre si e **questionário deve estar entre as técnicas escolhidas**, conforme o enunciado da disciplina.

### Instrumento I01 — Questionário

**Autor(a):** Mariane S. Carvalho RA: 22.123.105-3
**Técnica:** questionário
**Objetivo:** Investigar H02, H04, H05 e H07 por meio de relatos sobre o fluxo de tomografias renais, os papéis e sistemas envolvidos, a familiaridade com visualizadores e métricas de aprendizado de máquina, as condições da rotina e a necessidade de consultar exames anteriores. Usar os dados para verificar a plausibilidade do recorte de IHC e orientar decisões de fluxo, vocabulário e funcionalidades, sem tratar respostas declaradas como validação de uso da interface.
**Público:** Médicos nefrologistas que atuam ou já atuaram na avaliação clínica de pacientes com tomografias renais (público principal); médicos radiologistas que interpretam esses exames e profissionais que participam diretamente de seu recebimento, armazenamento ou disponibilização (para questões sobre fluxo e contexto). Direcionar as questões conforme o papel de cada participante.

#### Procedimento padronizado de aplicação

1. **Preparação:** finalizar e testar o questionário com ao menos uma pessoa para verificar clareza, tempo de resposta e encaminhamento por função; definir quais itens se aplicam a nefrologistas, radiologistas e profissionais do fluxo de exames. Obter as autorizações institucionais exigidas, se houver recrutamento por uma instituição, e convidar somente profissionais que atendam aos critérios descritos em "De quem coletar", sem solicitar dados de pacientes.
2. **Apresentação e consentimento:** antes das perguntas, apresentar o objetivo acadêmico, os temas, o tempo estimado após o teste, os responsáveis, o prazo de guarda e o uso dos dados. Informar que a participação é voluntária, que é possível pular questões ou interromper a resposta e que não haverá gravação. Registrar a concordância explícita antes de prosseguir; em caso de recusa, encerrar sem coletar respostas.
3. **Aplicação:** disponibilizar a mesma versão do questionário aos participantes, iniciando pela identificação da função profissional para direcionar apenas questões pertinentes ao papel declarado. Manter a ordem e a redação das perguntas, permitir "não sei/não se aplica" quando pertinente e não pedir imagens, laudos ou informações identificáveis de pacientes, colegas ou instituições. Em caso de dúvida, esclarecer termos sem sugerir uma resposta.
4. **Encerramento:** agradecer, informar como entrar em contato com a equipe para dúvidas ou solicitação de retirada dos dados enquanto ainda for possível vinculá-los ao participante e verificar se respostas abertas contêm identificadores; se contiverem, removê-los antes da análise. Não apresentar respostas individuais a chefias ou instituições.
5. **Armazenamento e anonimização:** separar eventuais contatos e termos de consentimento das respostas, atribuir códigos aos registros e restringir o acesso à equipe responsável. Guardar os arquivos em local protegido, fora de repositórios públicos; divulgar apenas resultados agregados ou trechos sem identificadores. Cumprir o prazo de guarda informado no consentimento e, ao final, excluir dados identificáveis e manter somente sínteses não identificáveis.

#### Instrumento

**Informações para consentimento (apresentar antes da questão 1):**

- **Objetivo acadêmico:** esta pesquisa integra a disciplina de IHC do projeto sobre uma possível interface de apoio à avaliação de tomografias renais. Busca compreender a rotina profissional e verificar se o perfil de usuário e o fluxo inicialmente propostos fazem sentido; não avalia o desempenho dos participantes nem fornece diagnóstico.
- **Temas:** atuação profissional, etapas e meios de acesso aos exames, ferramentas utilizadas, condições de avaliação, consulta a exames anteriores e, para nefrologistas, familiaridade com visualizadores e métricas de IA. Não serão solicitados exames, laudos nem dados de pacientes.
- **Tempo estimado:** aproximadamente 10 a 15 minutos. Esta é uma estimativa inicial; a equipe deve conferi-la no pré-teste e atualizar este texto antes de convidar participantes.
- **Responsáveis:** Mariane S. Carvalho (RA 22.123.105-3) e Equipe 12 do projeto. O contato para dúvidas e solicitações de retirada dos dados deve ser informado no convite antes da participação.
- **Uso dos dados:** respostas serão analisadas para investigar H02, H04, H05 e H07 e fundamentar decisões sobre fluxo e interface. Apenas resultados agregados ou trechos sem identificadores constarão dos trabalhos acadêmicos; respostas individuais não serão enviadas a chefias ou publicadas no repositório.
- **Guarda e descarte:** respostas e eventuais registros de consentimento ficarão separados, com acesso restrito à equipe, até 90 dias após o encerramento da disciplina; então, dados identificáveis serão excluídos, mantendo-se somente sínteses não identificáveis. Se a instituição exigir outro prazo, informar o prazo aplicável antes da coleta.
- **Participação:** é voluntária, sem gravação ou consequência profissional pela recusa. É possível pular perguntas ou interromper a participação; a retirada de respostas já enviadas pode ser solicitada enquanto ainda for possível associá-las ao participante.

**Instruções ao participante:** Responda com base em sua experiência profissional com tomografias renais, atual ou anterior. Não inclua nomes de pessoas ou instituições, imagens, laudos ou informações que identifiquem pacientes. Exceto a concordância inicial e as questões de triagem, você pode deixar uma questão sem resposta. Nas questões de escolha única, marque uma alternativa; nas de múltipla escolha, marque todas as aplicáveis. Se marcar "nenhuma" ou "não sei informar", não marque outras alternativas na mesma questão. "Outro" admite uma descrição breve, sem dados identificáveis.

**Consentimento e triagem (todos os participantes)**

1. Você leu as informações de consentimento apresentadas antes deste questionário e concorda em participar voluntariamente? (escolha única: sim; não). **Se não, encerrar sem registrar respostas.**
2. Qual é sua atuação em relação a tomografias renais? (escolha única: nefrologista na avaliação clínica; radiologista na interpretação ou elaboração de laudo; profissional que recebe, armazena ou disponibiliza exames; outra atuação; nenhuma dessas atuações). **Se "outra" ou "nenhuma", encerrar; não solicitar identificação profissional adicional.**
3. Você exerce ou já exerceu essa atuação com tomografias renais? (escolha única: atualmente; anteriormente; nunca). **Se "nunca", encerrar.**
4. Há quanto tempo exerce ou exerceu essa atuação? (escolha única: menos de 1 ano; 1 a 5 anos; 6 a 10 anos; mais de 10 anos; prefiro não informar).

**Fluxo do exame e tecnologia (todos os participantes elegíveis; H02, H04, H05)**

5. Em quais etapas você participa ou participou? (múltipla escolha: solicitação do exame; recebimento ou disponibilização; acesso às imagens; interpretação ou elaboração do laudo; avaliação clínica do resultado; consulta a exames anteriores; outra etapa; não sei informar).
6. Como o exame chega ou chegava à etapa em que você atua? (múltipla escolha: sistema institucional de imagens/exames; prontuário eletrônico; mídia física; arquivo enviado por meio eletrônico; documento ou laudo impresso; outra forma; não sei informar).
7. Quem disponibiliza ou disponibilizava o exame para sua etapa? (escolha única: serviço de imagem; profissional administrativo; outro profissional de saúde; o próprio paciente; acesso direto em sistema, sem envio por outra pessoa; outra forma; não sei informar).
8. A quais informações você tem ou tinha acesso nessa etapa? (múltipla escolha: imagens da tomografia; laudo; informações clínicas da solicitação; exames anteriores; resultado de ferramenta automatizada de análise; outra informação; não sei informar).
9. Quais ferramentas você utiliza ou utilizava nesse fluxo? (múltipla escolha: sistema de visualização de imagens; prontuário eletrônico; sistema de gestão de exames; ferramenta de análise automatizada/IA; documentos ou mídia fora de sistemas; outra ferramenta; não sei informar).
10. Em qual etapa, se alguma, um resultado automatizado de classificação de imagens poderia ser consultado no seu trabalho? (escolha única: antes da interpretação ou do laudo; durante a interpretação ou elaboração do laudo; durante a avaliação clínica após o laudo; em outra etapa; não identifico uma etapa útil; não sei informar).
11. Há alguma etapa ou profissional importante para o acesso ao exame que não foi contemplado nas alternativas anteriores? (resposta aberta opcional; descreva apenas a função ou a etapa, sem identificar pessoas ou instituições).

**Rotina de avaliação (somente nefrologistas e radiologistas; H05)**

12. Com que frequência você avalia ou avaliava informações de tomografias renais em sua atividade? (escolha única: diariamente; semanalmente; mensalmente; menos de uma vez por mês; não sei informar).
13. Com que frequência o tempo disponível dificulta ou dificultava essa atividade? (escolha única: nunca; raramente; às vezes; frequentemente; sempre; não sei informar).
14. Com que frequência identificar ou avaliar alterações sutis é ou era uma dificuldade nessa atividade? (escolha única: nunca; raramente; às vezes; frequentemente; sempre; não sei informar).
15. O que mais dificulta ou dificultava sua atividade com esses exames? (múltipla escolha: tempo disponível; acesso às imagens; qualidade das imagens; falta de informações clínicas; localização de exames anteriores; identificação ou interpretação de achados; comunicação entre profissionais; nenhuma dificuldade relevante; outra dificuldade; não sei informar).
16. Se quiser, descreva uma dificuldade relevante não contemplada acima, sem mencionar casos clínicos ou pessoas identificáveis. (resposta aberta opcional).

**Exames anteriores (todos os participantes elegíveis; H07)**

17. Na sua atuação, com que frequência é ou era necessário consultar ou disponibilizar exames anteriores do mesmo paciente? (escolha única: nunca; raramente; às vezes; frequentemente; sempre; não sei informar). **Se "nunca" ou "não sei informar", ir para a questão 22.**
18. Para qual finalidade os exames anteriores são ou eram utilizados na sua etapa? (múltipla escolha: comparar achados ao longo do tempo; contextualizar decisão clínica; elaborar ou revisar laudo; localizar informações para outro profissional; outra finalidade; não sei informar).
19. Como esses exames anteriores são ou eram encontrados? (múltipla escolha: sistema institucional de imagens/exames; prontuário eletrônico; solicitação a outro profissional ou setor; arquivos ou mídia fornecidos pelo paciente; outro meio; não sei informar).
20. Quais critérios você utiliza ou utilizava para localizar exames anteriores? (múltipla escolha: identificação do paciente, sem informar o identificador; data do exame; tipo de exame; parte do corpo examinada; texto do laudo; outro critério; não sei informar).
21. O meio atualmente disponível para localizar esses exames atende ou atendia às necessidades da sua etapa? (escolha única: sim; parcialmente; não; não sei informar).
22. Se uma nova ferramenta de apoio à avaliação fosse utilizada, como a consulta a exames anteriores deveria ocorrer para sua etapa? (escolha única: não seria necessária; pelo sistema já utilizado, sem consulta na nova ferramenta; por acesso aos exames anteriores na nova ferramenta; não sei informar). **Esta questão investiga uma necessidade declarada, não define um requisito.**

**Experiência e aprendizado (somente nefrologistas; H04)**

23. Qual é sua familiaridade com sistemas de visualização de imagens de tomografia? (escolha única: nunca utilizei; conheço, mas não utilizo; utilizo com ajuda; utilizo de forma independente; não sei informar).
24. Qual é sua familiaridade com medidas usadas para descrever resultados de modelos de IA, como probabilidade atribuída a uma classe ou medida de confiança? (escolha única: não conheço; já ouvi falar, mas não sei interpretá-las; consigo interpretar com orientação; consigo interpretá-las de forma independente; não sei informar).
25. Você já utilizou alguma ferramenta de IA como apoio à avaliação de exames de imagem? (escolha única: sim, regularmente; sim, ocasionalmente; conheço, mas nunca utilizei; não conheço; prefiro não informar).
26. Se precisasse usar uma nova ferramenta de apoio à avaliação, qual forma de aprendizado seria mais viável na sua rotina? (escolha única: orientações curtas na própria ferramenta; demonstração por outra pessoa; material de consulta; exploração por conta própria; não teria tempo para aprender; outra forma; não sei informar).

#### Como os dados serão analisados

Separar as respostas por função declarada (Q2) e considerar apenas participantes elegíveis (Q1–Q3). Para cada questão fechada, registrar contagens e proporções entre os participantes aos quais ela se aplicava; indicar o número de respostas válidas, ausências, "não sei informar" e saltos previstos, sem tratar itens não respondidos como "não". Em questões de múltipla escolha, contar cada alternativa separadamente; as proporções podem somar mais de 100%. Comparar grupos profissionais apenas quando houver respostas suficientes para preservar a privacidade, sem divulgar combinações de características que identifiquem alguém.

- **H02 — fluxo e papéis (Q5–Q11):** organizar as etapas, os meios de chegada do exame, os responsáveis pela disponibilização e os pontos em que um resultado automatizado poderia ou não ser consultado. Confrontar relatos de nefrologistas, radiologistas e profissionais do fluxo para verificar se o recorte proposto corresponde às atividades descritas; não inferir que exista upload manual.
- **H04 — experiência técnica (Q9 e Q23–Q26, estas últimas apenas para nefrologistas):** descrever familiaridade declarada com visualizadores, métricas de IA e ferramentas semelhantes, considerando experiência profissional (Q4). Identificar necessidade relatada de orientação e possível ajuste de vocabulário, sem concluir que a pessoa interpreta corretamente as métricas apenas por autodeclaração.
- **H05 — condições e dificuldades (Q5, Q8–Q9 e Q12–Q16):** resumir frequência da atividade, pressão de tempo e dificuldades relatadas; relacioná-las às etapas e ferramentas usadas, mantendo separadas as respostas de nefrologistas e radiologistas. Usar os resultados para revisar o cenário e a priorização das tarefas, sem presumir que alterações sutis sejam uma dificuldade universal.
- **H07 — exames anteriores (Q17–Q22):** apurar frequência e finalidade da consulta ou disponibilização, meios e critérios usados para localizar exames e suficiência das ferramentas atuais. Comparar a necessidade declarada de acesso na nova ferramenta com a possibilidade de continuar usando sistemas existentes; não transformar preferência por histórico ou filtros em requisito sem justificar a tarefa.

Revisar respostas abertas e descrições em "outro" (Q11, Q16 e alternativas correspondentes) para remover identificadores e agrupar temas recorrentes e casos divergentes, registrando exemplos não identificáveis. Sintetizar para cada hipótese o que os dados sustentam, contradizem ou deixam em aberto, relacionando achados a decisões de design e atualizando `RASTREABILIDADE.md` após a coleta. Como a amostra pode ser pequena e de conveniência, apresentar resultados como exploratórios, sem generalização estatística ou validação do uso real da interface.

## Síntese

Explique quais lacunas de conhecimento sobre usuários o conjunto de técnicas pretende reduzir. Indique explicitamente quais hipóteses da Entrega 1 deverão ficar **sustentadas, refutadas ou refinadas** após a análise dos dados. Quando os dados forem coletados/analisados, atualize o histórico em `RASTREABILIDADE.md`.

O questionário I01 pretende reduzir lacunas sobre quem participa da avaliação de tomografias renais, como os exames chegam a cada profissional, quais sistemas são usados, que dificuldades surgem na rotina e se a consulta a exames anteriores precisa ocorrer na solução proposta. As respostas de nefrologistas serão analisadas separadamente das de radiologistas e profissionais que disponibilizam exames, para não atribuir ao usuário principal tarefas desempenhadas por outros papéis. Até o momento, este documento detalha o questionário; outras técnicas da equipe, se adotadas, deverão ser integradas à síntese após sua definição.

- **H02:** poderá ser sustentada quanto ao contexto de uso se os relatos indicarem um fluxo profissional relevante de fornecimento do exame e uma etapa plausível para consultar o resultado automatizado; refutada se esse fluxo não corresponder às atividades descritas; ou refinada quanto a responsáveis, meios de acesso e momento de consulta. O processamento técnico precisará ser detalhado com a equipe do modelo. Isso orientará o recorte de IHC sem pressupor upload manual.
- **H04:** poderá ser sustentada se nefrologistas relatarem familiaridade com visualizadores, mas pouca familiaridade com métricas de IA; refutada se o perfil relatado for diferente; ou refinada conforme a variação entre profissionais. Isso orientará vocabulário e necessidade de orientação, sem comprovar compreensão efetiva das métricas.
- **H05:** poderá ser sustentada se pressão de tempo ou dificuldade com alterações sutis forem recorrentes na atividade relatada; refutada se não se mostrarem relevantes; ou refinada pela identificação de outras dificuldades, etapas, sistemas e condições. Isso poderá alterar o cenário de uso e as tarefas priorizadas.
- **H07:** poderá ser sustentada se a consulta a exames anteriores for uma tarefa recorrente cuja execução exija recursos na solução; refutada se não fizer parte do fluxo investigado; ou refinada se a tarefa existir, mas já for atendida por outros sistemas, sem necessidade de histórico ou filtros próprios.

Essas classificações serão feitas **somente após a coleta**, com registro das evidências, divergências entre papéis e limites da amostra em `RASTREABILIDADE.md`. Respostas declaradas não validam a interface nem a compreensão do resultado do modelo: H01, H03 e a parte de H06 relativa à interpretação das saídas ainda exigem avaliação com exemplos ou tarefas concretas; o que o modelo produz deve ser confirmado com a equipe técnica.

## Checklist

- [x] Hipóteses/lacunas prioritárias da Entrega 1 foram revisitadas.
- [x] Se o escopo de IHC foi derivado de TCC técnico, a coleta investiga a plausibilidade do usuário, tarefa e contexto adotados.
- [x] Perguntas não pressupõem que dashboard, CRUD, filtros ou relatórios sejam necessários; investigam a necessidade.
- [x] Cada dado a coletar responde uma dúvida concreta do projeto ou justifica outra necessidade de informação.
- [x] Parte A identifica dados e perfis de coleta de forma específica.
- [x] Aspectos éticos são contextualizados para o projeto.
- [x] Há uma técnica completa por integrante e técnicas distintas.
- [x] Questionário está incluído entre as técnicas.
- [x] Cada instrumento possui objetivo, público, procedimento e conteúdo integral.
- [x] Perguntas evitam indução e coletam apenas dados necessários.
- [x] Está claro como os dados serão analisados e usados no design.
