# Matriz de rastreabilidade de IHC

A matriz deve ser atualizada ao longo do semestre. Ela ajuda a demonstrar que a interface não surgiu arbitrariamente e registra **como o conhecimento da equipe evoluiu**.

Para projetos cujo TCC não previa interface, esta matriz é especialmente importante: deve ficar visível a passagem da **contribuição técnica do TCC** para um **cenário de uso plausível**, e desse cenário para as decisões de interação.

## 1. Derivação do escopo de IHC a partir do TCC

| Elemento | Registro da equipe | Evidência/justificativa | Estado |
|---|---|---|---|
| Tema do TCC | Detecção de patologias renais em tomografia computadorizada por meio de redes convolucionais de baixo custo computacional | Título declarado na Entrega 1, seção 0.2 | definido |
| Resultado técnico esperado | Modelo de IA/ML para classificação de imagens médicas renais | Declaração da equipe na Entrega 1, seções 0.4 e 1.5 | definido |
| O TCC previa interface? | Sim, conforme declaração atual da equipe | Entrega 1, seções 0.5 e 7.5; a implementação da interface no TCC ainda não está decidida | definido como declaração da equipe |
| Capacidade/contribuição central | Classificar imagens de tomografias renais com redes convolucionais, com foco em eficiência computacional e análise de interpretabilidade | Entrega 1, seções 1.3 e 1.5 | definido como escopo declarado |
| Possíveis beneficiários/stakeholders | Médicos nefrologistas, pacientes, profissionais de IA/ML e profissionais de TI/administração | Perfis e impactos propostos na Entrega 1, seções 2.2–2.3; adoção e papéis são hipóteses | H |
| Usuário escolhido para IHC | Médico nefrologista, escolhido inicialmente pela equipe por sua especialização em doenças do sistema urinário, com foco nos rins | Decisão inicial registrada na Entrega 1, seção 7.2; adequação ao uso da solução precisa ser validada com profissionais | H |
| Objetivo principal do usuário | Avaliar uma tomografia renal, interpretar possíveis achados e decidir como prosseguir com a avaliação clínica, considerando a indicação do modelo como apoio | Objetivo proposto na Entrega 1, seções 3.2 e 7.3; atividade real e uso do modelo precisam ser validados | H |
| Contexto de uso adotado | Avaliação profissional de tomografias computadorizadas renais; instituição, rotina e fluxo específicos ainda não definidos | Entrega 1, seções 5.1 e 7.4; contexto proposto a investigar | H |
| Interface/recorte de IHC | Fornecimento do exame, acompanhamento do processamento e consulta aos elementos do resultado que a investigação confirmar como necessários; envio manual e elementos a apresentar não estão definidos | Deriva da capacidade técnica e do objetivo proposto; validar H02 e H06 na Entrega 1, seção 10 | proposta; fluxo e informações a validar |
| Relação com o TCC | Interface declarada como prevista no sistema descrito; o recorte da disciplina é um artefato de aprendizagem de IHC e sua implementação no TCC depende de decisão posterior da equipe e da orientadora | Entrega 1, seções 0.5, 7.5 e delimitação | definido como declaração da equipe |

> Se o escopo de IHC mudar ao longo do semestre, preserve a decisão anterior no histórico e registre **qual evidência motivou a mudança**.

## 2. Registro de hipóteses e lacunas da Entrega 1

Use esta tabela para itens importantes marcados como `[H]` ou `[?]`. Preserve o histórico: não apague uma hipótese refutada.

| ID | Afirmação / dúvida inicial | Tipo | Por que importa | Como/onde investigar | Evidência obtida | Estado atual | Impacto no projeto |
|---|---|---|---|---|---|---|---|
| H01 | Médicos nefrologistas compreenderão e considerarão útil uma explicação do resultado do modelo apresentada junto à imagem | H | A compreensão e a utilidade precisam ser verificadas; interpretabilidade não garante compreensão, utilidade ou confiança | Entrega 3 / 7 | PENDENTE — investigar com médicos nefrologistas | aberta | Pode orientar a forma de apresentar explicações e detalhes técnicos |
| H02 | O fluxo de fornecimento do exame, processamento e resultado representa uma atividade real e relevante no contexto profissional; é necessário descobrir quem fornece o exame e por qual meio | H | Define o recorte de IHC e os papéis envolvidos sem pressupor upload manual | Entrega 3 / 4 / 5 | PENDENTE — investigar com profissionais envolvidos no fluxo do exame | aberta | Pode confirmar ou alterar o fluxo priorizado e os perfis envolvidos |
| H03 | O médico nefrologista distinguirá claramente a indicação do modelo do diagnóstico final | H | Uma interpretação equivocada poderia afetar a avaliação clínica; a consequência concreta precisa ser investigada | Entrega 4 / 7 / 8 | PENDENTE — investigar com médicos nefrologistas | aberta | Exige comunicação clara das limitações e da responsabilidade profissional |
| H04 | O médico nefrologista poderá ter familiaridade com sistemas de visualização de exames, mas não necessariamente com métricas de aprendizado de máquina | H | A experiência e as necessidades de apresentação podem orientar o vocabulário e o nível de detalhe | Entrega 3 / 7 | PENDENTE — investigar com médicos nefrologistas | aberta | Pode orientar o vocabulário e o nível de detalhe da interface |
| H05 | A rotina de avaliação de tomografias poderá envolver pressão de tempo ou dificuldade para identificar alterações sutis; instituição, etapas, papéis, sistemas e condições ainda são desconhecidos | H | O contexto e as dificuldades reais podem alterar o problema e o recorte de IHC | Entrega 3 / 4 | PENDENTE — investigar com profissionais envolvidos na avaliação do exame | aberta | Pode confirmar, alterar ou refutar a situação de uso descrita |
| H06 | Classificação, medida de confiança e explicação do modelo são elementos distintos; quais são produzidos, necessários e compreendidos pelo nefrologista ainda precisa ser investigado | H | Evita tratar elementos diferentes como equivalentes ou presumir que todos devam ser apresentados na interface | Entrega 3 / 7 | PENDENTE — investigar com médicos nefrologistas | aberta | Pode definir quais informações serão apresentadas e como serão diferenciadas da conclusão clínica |

## 3. Rastreabilidade entre contribuição técnica, necessidades e artefatos

| ID | Capacidade do TCC utilizada | Necessidade/problema | Persona | Cenário problema | Objetivo/tarefa | HTA/GOMS/CTT | Cenário de interação / signos | MoLIC | Tela(s) Figma | Heurística / problema | Tarefa no teste | Decisão/melhoria |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| R01 | {{ex.: recomendação de otimização}} | {{...}} | {{P01}} | {{C01}} | {{T01}} | {{links}} | {{...}} | {{M01}} | {{F01...}} | {{V01 ou —}} | {{UT01}} | {{...}} |
| R02 |  |  |  |  |  |  |  |  |  |  |  |  |

## 4. Rastreabilidade de padrões de interface

Use esta tabela quando o projeto incorporar padrões como dashboard, relatório, histórico, filtros ou administração. O objetivo é **justificar o padrão**, não apenas listar telas.

| ID da tela/fluxo | Padrão de interface | Objetivo/tarefa que justifica | Informação/ação principal | Evidência de necessidade | Artefatos relacionados |
|---|---|---|---|---|---|
| F01 | dashboard | {{T01}} | {{...}} | {{H01/evidência...}} | {{C01/M01}} |
| F02 | histórico com filtros | {{T02}} | {{...}} | {{...}} | {{...}} |
| F03 | administração/CRUD | {{T03}} | {{...}} | {{...}} | {{...}} |

## 5. Registro de mudanças de escopo

| Data | O que mudou | Evidência/feedback que motivou | Artefatos afetados | Responsável |
|---|---|---|---|---|
| {{...}} | {{...}} | {{...}} | {{...}} | {{...}} |

## Como usar

- Use identificadores estáveis (`H01`, `P01`, `C01`, `T01`, `M01`, `F01`, `UT01`).
- Quando uma necessidade/problema tiver origem em hipótese da Entrega 1, cite o ID correspondente.
- Em TCC sem interface original, pelo menos uma linha deve mostrar claramente **como uma capacidade técnica chega até uma tarefa de usuário e uma tela/fluxo**.
- Uma linha pode se desdobrar quando um objetivo possui múltiplos caminhos.
- Não force relação inexistente: se algo ainda não foi modelado, marque `PENDENTE`.
- Ao remover uma funcionalidade, registre a decisão em vez de apagar silenciosamente o histórico.
- Dashboard, CRUD, filtros e relatórios só devem aparecer quando houver objetivo/tarefa que os justifique.
