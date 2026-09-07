# Entrega 3 — Personas, mapa de empatia, contexto de uso e jornada

**Data:** 07/09/2026  
**Status:** 🟨 em andamento  
**Responsabilidade:** 1 persona por integrante; 1 mapa de empatia, 1 contexto de uso consolidado e 1 jornada por equipe (salvo orientação diferente do docente).

## Objetivo da atividade

Representar grupos de usuários de forma útil para decisões de design. Persona não é personagem decorativo: suas características devem alterar requisitos, prioridades, linguagem, fluxos ou critérios de avaliação.

## Atenção a projetos técnicos

Em TCCs sem interface original, a persona pode representar um **profissional que se apropria da contribuição técnica**: DBA, analista, cientista de dados, administrador, pesquisador, técnico, operador, gestor ou especialista de domínio.

Não escolha um perfil apenas porque “parece combinar” com a tecnologia. Explique **qual objetivo esse perfil teria e qual parte da contribuição do TCC produziria valor para ele**. Se ainda for hipótese, mantenha como hipótese/proto-persona a validar.

Também considere papéis diferentes quando houver tarefas distintas, por exemplo:

- operador que executa análises;
- administrador que configura e gerencia permissões;
- especialista que interpreta resultados;
- gestor que consulta relatórios e decide;
- auditor que revisa histórico.

## Entradas da Entrega 1

Antes de criar personas, retome os tipos de usuários, características relevantes, objetivos e hipóteses registradas na Entrega 1. A persona **não deve transformar uma hipótese inicial em fato por meio de uma história fictícia**.

| Item da Entrega 1 | Status inicial | Evidência disponível agora | Como será tratado nesta entrega |
|---|---|---|---|
| {{usuário/objetivo/característica/H01...}} | F / H / ? | {{...}} | incorporar / manter como hipótese / descartar / investigar |

## 1. Personas

### Persona P01 — Mário

**Autor(a):** Mariane S. Carvalho  
**Tipo:** primária 
**Base de evidências:** proto-persona a validar  
**Hipóteses da Entrega 1 relacionadas:** H02

![Persona P01](../assets/03_personas/persona_p01.svg)

| Campo | Descrição |
|---|---|
| Faixa etária / contexto relevante | 45 anos, médico experiente, com rotina clínica intensa e necessidade de tomar decisões com agilidade. Atua principalmente no acompanhamento e diagnóstico de pacientes com doenças renais. |
| Ocupação/papel | Médico nefrologista, responsável pela avaliação clínica dos pacientes, interpretação de exames e definição de condutas. Pode atuar em hospital, clínica especializada ou centro de diagnóstico. |
| Conhecimento do domínio | Amplo conhecimento em nefrologia, doenças renais e interpretação de exames relacionados aos rins. Possui experiência para avaliar achados clínicos e imagéticos e confrontá-los com o histórico do paciente. |
| Experiência tecnológica | Intermediária/alta. Utiliza prontuários eletrônicos, sistemas hospitalares e plataformas de exames diariamente. Não necessariamente possui conhecimento técnico sobre IA ou CNNs, mas entende os resultados clínicos e espera que o sistema seja simples de utilizar.  |
| Objetivos | Aumentar a precisão e agilidade da avaliação, identificar possíveis alterações renais em imagens, reduzir o risco de passar despercebidos achados relevantes e utilizar informações adicionais para apoiar sua decisão clínica. |
| Necessidades | Receber resultados claros, rápidos e confiáveis; visualizar a imagem analisada; identificar a região que levou o sistema a sinalizar uma possível alteração; compreender o resultado de maneira objetiva; comparar o resultado da IA com sua própria avaliação. |
| Dores/frustrações | Grande volume de exames; jornada de trabalho exaustiva; possibilidade de alterações sutis passarem despercebidas; sistemas hospitalares complexos; resultados de IA que não explicam por que chegaram a determinada conclusão; receio de confiar em uma ferramenta sem compreender suas limitações. |
| Motivadores | Melhorar a qualidade do atendimento; reduzir erros de interpretação; ganhar tempo na análise; utilizar novas tecnologias de forma segura; ter maior confiança nas decisões clínicas e oferecer um diagnóstico mais consistente aos pacientes. |
| Restrições/acessibilidade | Possui pouco tempo para aprender sistemas novos. A interface deve exigir baixa carga cognitiva, apresentar informações de forma objetiva e utilizar textos, ícones e indicadores facilmente compreensíveis. Deve permitir boa visualização das imagens e dos resultados, inclusive em monitores hospitalares de diferentes tamanhos. |
| Ambiente típico de uso | Consultório, clínica ou hospital, geralmente em um computador de trabalho, durante a avaliação de exames de pacientes. Pode utilizar o sistema em momentos de alta demanda, com interrupções frequentes. |
| Comportamentos relevantes | Analisa primeiro as informações clínicas e os exames; tende a validar o resultado da ferramenta antes de utilizá-lo; procura evidências visuais para confirmar uma indicação da IA; prefere interfaces objetivas; compara diferentes informações antes de tomar uma decisão; tende a desconfiar de resultados que não apresentem justificativa ou evidência visual. |

**Decisões de design influenciadas por P01:**

- Resultado objetivo: apresentar a classificação de maneira clara, evitando excesso de informações técnicas.
- Explicabilidade: permitir visualizar onde o modelo concentrou sua atenção na imagem.
- Comparação: possibilitar visualizar a imagem original junto da indicação gerada pelo sistema.
- Confiança: apresentar métricas ou indicadores de confiança de maneira compreensível, sem transformar o sistema em uma “caixa-preta”.
- Agilidade: o fluxo para carregar/analisar uma imagem e visualizar o resultado deve ter poucos passos.
- Controle médico: deixar explícito que o resultado é apoio à decisão, cabendo ao médico a avaliação final.
- Baixa carga cognitiva: evitar dashboards excessivamente complexos ou informações técnicas de ML que não contribuam diretamente para a decisão.

> Repita para P02, P03... Cada integrante deve produzir ao menos uma persona.

### Síntese das personas

O médico nefrologista é uma persona prioritária porque possui conhecimento especializado sobre doenças renais e é diretamente responsável pela interpretação dos resultados clínicos. Como o software tem como finalidade auxiliar na identificação de alterações em imagens dos rins, é esse profissional que utilizará os resultados da ferramenta para complementar sua própria avaliação.

## 2. Mapa de empatia — equipe

**Persona escolhida:** {{P01}}  
**Justificativa:** {{por que esse perfil é relevante}}

![Mapa de empatia](../assets/03_personas/mapa_empatia.svg)

Documente também em texto: o que vê; ouve; diz/faz; pensa/sente; dores; ganhos. Diferencie **evidência** de **hipótese**.

## 3. Contexto de uso — consolidação

| Dimensão | Descrição | Implicação de design |
|---|---|---|
| Usuários | {{...}} | {{...}} |
| Tarefas | {{...}} | {{...}} |
| Equipamentos | {{...}} | {{...}} |
| Ambiente físico | {{...}} | {{...}} |
| Ambiente social/organizacional | {{...}} | {{...}} |
| Papéis/permissões/governança | {{...}} | {{...}} |
| Volume de dados/histórico | {{...}} | {{...}} |

## 4. Jornada do usuário — equipe

**Persona:** {{P01}}  
**Objetivo da jornada:** {{...}}  
**Início e fim da jornada:** {{...}}

| Etapa | Situação/ação | Objetivo | Pensamento/emoção | Dor | Oportunidade de design | Evidência |
|---|---|---|---|---|---|---|
| 1 | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} |

> A jornada pode incluir etapas **antes, durante e depois** do uso do produto. Não transforme a jornada em lista de telas.

## Síntese

Quais necessidades e objetivos devem obrigatoriamente aparecer nos cenários e nas tarefas seguintes?

## Checklist

- [ ] Existe pelo menos uma persona por integrante.
- [ ] As personas não são apenas diferenças demográficas superficiais.
- [ ] Está claro o que é dado real e o que é hipótese/proto-persona.
- [ ] A persona não “validou por ficção” uma hipótese da Entrega 1; afirmações continuam marcadas como hipótese quando não há evidência.
- [ ] Objetivos e dores têm consequência para o design.
- [ ] Contexto de uso está coerente com a Entrega 1.
- [ ] Em TCC sem interface original, a persona possui relação explícita com a contribuição técnica.
- [ ] Papéis administrativos, técnicos e decisórios só foram criados quando possuem objetivos/tarefas diferentes.
- [ ] Jornada possui etapas, dores e oportunidades e não é apenas wireflow.
- [ ] IDs das personas foram adicionados à rastreabilidade.
