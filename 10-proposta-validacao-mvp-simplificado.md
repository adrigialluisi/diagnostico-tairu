# TAIRU — Proposta de Validação da Tese de MVP Simplificado

Documento de transição entre o diagnóstico (Frentes 01-04) e a fase de continuidade prevista em `03-escopo-projeto-consultoria.md`. Consolida as conclusões do diagnóstico numa hipótese testável, e propõe um ciclo de 3 meses para validar essa hipótese — antes de qualquer decisão de desenvolvimento ou de pivô total da ideia original. Em outras palavras: este documento existe pra fazer, agora, o processo correto de desenvolvimento de produto — validar a dor e a proposta antes de construir — que não foi feito da primeira vez.

---

## 0. Resumo executivo

**Resumo do mercado**
O mercado de IA em turismo está em forte expansão (US$ 2,95 bi em 2024 → US$ 13,38 bi projetados até 2030), mas sofre de excesso de oferta fragmentada, não de falta dela: o usuário médio baixa 4-6 apps de viagem por jornada e usa só 2-3. O mercado se divide em 4 quadrantes (planejamento, agregação de reservas, diário passivo, IA-native) e nenhum concorrente cobre os 4 com qualidade madura. Concorrentes robustos como Wanderlog, Stippl e Tripsy já têm versão em português e cobram, na média, perto de R$ 20/mês — preço e idioma não são a barreira real. A barreira real é que eles acabam genéricos ("planeje tudo", pra qualquer viajante) ou evoluem pra um modelo de marketplace via comissão de reserva/afiliado, perdendo o apelo pessoal pra uma dor e um público específicos.

**Resumo da análise de usabilidade e dos feedbacks de Nelson e Vera**
A análise de usabilidade encontrou uma UI/UX estruturalmente quebrada: bugs de sincronização, campos essenciais ausentes (nº de voo, checkout, múltiplos destinos/moedas), navegação com opções ambíguas e colaboração em grupo que não funciona. Nelson (nota 7/10) usou o app numa viagem real de 10 dias: achou o input manual cansativo, só registrou eventos grandes, a colaboração com a família falhou tecnicamente, e nem sabia que o app tinha IA — mas elogiou muito o álbum de fotos pós-viagem. Vera (nota 6/10) usou o app só pra planejamento: confirmou bugs técnicos reais (erro ao abrir documentos, sincronização de datas falha) e apontou a limitação de 1 destino/1 moeda por viagem. Os dois, de forma independente, relataram o mesmo padrão: planejamento muito manual, viagem sempre acompanhada (família ou amigos), forte desejo de colaboração e sugestões, e um perfil de viagem que muda a cada vez — o mesmo padrão de dor do próprio fundador.

**Resumo da conclusão**
- O produto foi desenvolvido sem definição de ICP, dor ou proposta de valor clara.
- O mercado tem apps diversificados, mas nenhum resolve o ciclo completo de ponta a ponta — cada um acaba mais específico em algum ponto isolado.
- O app construído não entrega o que foi prometido no pitch, e o que foi construído tem problemas técnicos reais.

**Resumo da proposta de trabalho**
- **Mês 1:** definição do ICP (a partir das conversas com o fundador e do feedback já coletado), definição do problema a ser resolvido e da proposta de valor; entrevista com 4 a 6 pessoas do ICP, sem vínculo pessoal, para validar o problema e a proposta de valor.
- **Mês 2:** desenho do protótipo de um fluxo ponta a ponta mais simples, com os insights já trazidos pelo feedback; definição do que se deseja validar e das métricas que garantem o sucesso; definição de 1 modelo comercial a ser testado com o público.
- **Mês 3:** teste do fluxo com o ICP e teste do modelo comercial, mapeado dentro da mesma pesquisa com essas 6-8 pessoas; consolidação dos resultados já indicando o que vale ser implementado e o que precisa de ajuste.

**Resumo do investimento**
R$ 5.500/mês, totalizando R$ 16.500 pelo ciclo de 3 meses.

---

## 1. Conclusões do diagnóstico

**C1 — O "faz-tudo" desde o início não é viável no estágio atual do produto.**
Nenhuma das 10 promessas centrais do pitch foi entregue por completo (`09-entrega-prometida-vs-real.md`: 0 entregas plenas, 3 parciais, 7 não entregues). O investimento necessário para sustentar planejamento assistido + timeline automática + IA + colaboração em grupo com qualidade, tudo ao mesmo tempo, é incompatível com o estágio e o orçamento atuais do projeto, e o risco de não atingir product-market fit mesmo assim é alto.

**C2 — A promessa de diferenciação (automação) é hoje o ponto mais frágil da execução.**
O único recurso de automação testado (geolocalização por IA) errou; todo o resto do fluxo é manual. O argumento comercial central do produto ("tudo automático, sem esforço") não tem lastro real hoje.

**C3 — Não existe proposta de valor clara nem público-alvo definido.**
O pitch original não nomeia uma dor específica nem um público específico — tenta servir "o viajante" de forma genérica, disputando ao mesmo tempo os 4 quadrantes do mercado (`02-pesquisa-mercado-consolidada.md`).

**C4 — Existe um núcleo de valor real, mas é diferente do argumento central do pitch.**
O que foi mais elogiado nos testes reais (timeline organizada, campo de notas usado organicamente, álbum de memórias pós-viagem) não é "automação e planejamento assistido" — é registro e memória de viagem, mais perto do território do Polarsteps do que do Wanderlog.

**C5 — Preço e idioma não são a barreira real dos concorrentes robustos; a genericidade e a lógica de marketplace, sim.**
Wanderlog, Stippl e Tripsy já têm versão em português, e cobram, na média, algo perto de R$ 20/mês — não é caro pro padrão brasileiro de assinatura de app, ao contrário do que o diagnóstico assumiu inicialmente. A barreira real desses concorrentes é outra: eles se posicionam de forma genérica ("planeje tudo", pra qualquer viajante) ou evoluem pra um modelo de marketplace, monetizando via comissão de reserva/afiliado, o que dilui o apelo pessoal em favor de conversão comercial. Nenhum concorrente, brasileiro ou estrangeiro, oferece uma proposta de valor desenhada especificamente pra um público e uma dor específicos, como grupos de 45+ que viajam sempre acompanhados. É aí que está o espaço real, não no preço.

**C6 — A UI/UX atual está estruturalmente quebrada, não apenas com problemas de polimento.**
Bugs de sincronização (nome da viagem, datas passadas), campos de dados ausentes (nº de voo, checkout, múltiplos destinos/moedas) e falha completa da colaboração em grupo são falhas de modelagem de produto, não de estética. Some-se a isso uma navegação com muitas opções simultâneas (ícones de filtro sem indicação clara, menus com função ambígua) — um fluxo mais linear, passo a passo, tende a facilitar a adoção justamente pro público que este produto quer servir.

**C7 — Já houve um ciclo de construção e teste, e ele não performou bem.**
A versão atual do app é resultado de uma primeira aposta de desenvolvimento; o diagnóstico confirma que essa aposta não deve ser expandida como está. Esse investimento é sunk cost e não deve condicionar a decisão daqui pra frente.

**C8 — O processo de criação do TAIRU inverteu a ordem correta de validação: construiu antes de validar, não depois.**
O fundador partiu do próprio cenário como viajante, contratou o time de dev, construiu o produto inteiro, e só depois pediu para os amigos testarem. O diagnóstico confirma que os amigos (Nelson e Vera), com perfil parecido com o dele, de fato compartilham a mesma dor — ou seja, a intuição original do fundador sobre a dor estava certa. Mas essa validação aconteceu **depois** de construir, não antes, e nunca chegou a perguntar especificamente o que resolveria essa dor comum. Se essa etapa tivesse sido feita antes, o fundador teria descoberto o que de fato importava pra resolver a dor compartilhada, e construído de forma mais certeira, com o fluxo correto, desde o início. A entrevista aprofundada com o fundador sobre essa dor original **já foi realizada** — o próximo passo é verificar se esse mesmo padrão aparece em pessoas dentro do ICP (perfil de cliente ideal) que não conhecem o fundador nem o produto.

**C9 — Os relatos de Nelson e Vera revelam um padrão de dor consistente, não uma coincidência entre dois amigos.**
De forma independente, os dois relataram: **(1)** planejamento muito mais manual do que gostariam; **(2)** viajam sempre acompanhados — família ou amigos, nunca sozinhos; **(3)** colaboração e o desejo de receber sugestões de terceiros vieram à tona repetidamente nas conversas; **(4)** cada viagem tem um "perfil" diferente — o estilo de viagem não é fixo por pessoa, muda a cada vez, confirmando na prática o achado da análise de usabilidade sobre o quiz de onboarding único e fixo ser um erro conceitual (`01-analise-usabilidade.html`).

---

## 2. Hipótese a ser testada

**Hipótese principal (H1):**
Pessoas de 45 anos ou mais — o mesmo perfil do fundador, de Nelson e de Vera, que viajam sempre acompanhadas em família ou entre amigos — sentem duas dores que se somam: o planejamento cai inteiro nas costas de uma única pessoa do grupo, porque não existe um lugar onde cada um contribui com o que quer fazer; e cada viagem exige recomeçar do zero, porque o perfil e os interesses mudam a cada vez. Um companheiro de viagem colaborativo — cada membro entra, escolhe seus lugares, envia fotos e documentos, e a organização e a memória final ficam divididas entre todo mundo, sem IA generativa — resolve essa sobrecarga, a ponto de trocarem o método atual e pagarem por isso.

**Proposta de valor (frase de posicionamento):**
Um fluxo de planejamento mais simples e direto, que transforma a viagem numa memória coletiva bonita — construída por todos os membros da viagem juntos, não por uma pessoa só. TAIRU vem do tupi e significa "companheiro de viagem" — a proposta de companhia e compartilhamento encaixa organicamente com o significado original do nome, o que reforça (em vez de reinventar) o posicionamento da marca.

**Sub-hipóteses a testar dentro de H1:**
- **H1a (colaboração distribuída):** permitir que cada membro da viagem entre no app, escolha seus próprios lugares e atrações, e receba de volta um roteiro sugerido que combina as escolhas de todos, otimizado por distância/tempo, resolve o conflito de "cada um quer ir a um lugar diferente" sem que uma pessoa precise montar tudo sozinha nem que alguém precise ceder.
- **H1b (dica local sem IA generativa):** sugestões de eventos e lugares por cidade e data, buscadas de fontes de dados reais (agenda cultural, eventos locais), entregam parte do valor de "curadoria inteligente" sem o risco de erro que já prejudicou a confiança no produto atual.
- **H1c (estrutura de dados):** corrigir os gaps estruturais identificados no diagnóstico (múltiplos destinos e moedas por viagem, campo de nº de voo e horário de chegada, checkout de hospedagem) resolve fricção real, independente das novas funcionalidades de colaboração.
- **H1d (fechamento emocional compartilhável):** um resumo "melhores momentos" ao final da viagem, no estilo retrospectiva anual, com opção de compartilhar nas redes sociais, reforça o valor percebido do produto e cria um canal de aquisição orgânica.
- **H1e (fluxo linear):** um fluxo linear, passo a passo, sem navegação ramificada nem opções simultâneas ambíguas, facilita a adoção desse público — reduz a sensação de complexidade que o produto atual tem hoje.

**Nota sobre diferenciação:** mesmo que features específicas já existam isoladamente no mercado (mapa colaborativo do Wanderlog, split de conta do Stippl, diário automático do Polarsteps), a diferenciação do TAIRU não depende de inventar uma funcionalidade inédita — depende de montar essa combinação para uma dor e um público específicos, com um fluxo simples e direto, em vez da genericidade ou da lógica de marketplace que os concorrentes acabam adotando (C5). Isso direciona toda a comunicação, o apelo visual e o canal de distribuição de um jeito que nenhum concorrente genérico faz hoje.

**H2 — canal de distribuição (testada separadamente):**
Operadores de excursão/viagem em grupo (estilo CVC), que já atendem esse público, são um canal viável para oferecer o app aos participantes — validado à parte, com conversas exploratórias, sem prender o cronograma do teste principal a essa resposta.

**Critério de decisão:**
Este ciclo de validação **não é um pivô automático**, e também não é um teste tudo-ou-nada: cada funcionalidade da seção 3 será validada (ou não) individualmente com o público testado. O que for validado entre as pessoas testadas segue para implementação; o que não for validado volta para revisão, antes de qualquer linha de código. A ideia original do fundador só será considerada para pivô total se o conjunto do fluxo, bem desenhado e corretamente testado, não se mostrar sustentável como um todo.

---

## 3. Funcionalidades a considerar no protótipo

Lista levantada a partir do que já foi coletado com Nelson e Vera — coisas que eles disseram que seria bom ter no app pra resolver as dores deles — organizada por momento da viagem, sem nenhuma dependência de IA generativa:

**Planejamento**
- Quiz de perfil curto, por viagem (não único e fixo no onboarding, como hoje) — corrige o erro conceitual já identificado na análise de usabilidade.
- Seleção de múltiplos destinos por viagem.
- Seleção de múltiplas moedas por viagem.
- Dicas locais por cidade e data ("você vai estar em X no dia Y, e vai ter esse evento") buscadas de fontes de dados reais, com opção de selecionar eventos de acordo com o perfil daquela viagem — sem geração por IA.
- Fluxo linear, passo a passo, evitando telas com muitas opções simultâneas e navegação ramificada.

**Colaboração**
- Cada membro da viagem seleciona lugares e atrações que quer visitar; o app sugere um roteiro que combina as escolhas de todos, otimizado por distância, pra aproveitar melhor o tempo do grupo.
- Acesso à galeria de fotos do celular para envio simplificado, com identificação (tag) de qual membro enviou cada foto.
- Carteira de documentos compartilhada entre os membros da viagem — útil no cenário comum de alguém ficar sem bateria ou perder algo, e outra pessoa do grupo ter o documento à mão.

**Memória**
- Ao final da viagem, um resumo "melhores momentos", no estilo retrospectiva anual (Spotify Wrapped), compartilhável nas redes sociais.

---

## 4. Etapas — ciclo de 3 meses

### Mês 1 — Definição de ICP e proposta de valor

**Objetivo:** definir o ICP e a proposta de valor para esse público, e validar com pesquisa se o problema é o mesmo relatado por Nando (fundador), Nelson e Vera, e se a proposta de valor faz sentido para esse público.

**Atividades:**
- Definir o ICP com precisão, a partir da dor do fundador (já documentada em entrevista) e do padrão observado em Nelson e Vera (C9): pessoas de 45+ que viajam sempre acompanhadas (família ou amigos), planejam de forma manual e dispersa, e vivem cada viagem com um perfil diferente.
- Escrever a proposta de valor diferenciada para esse ICP.
- Pesquisa com o ICP: 4 a 6 entrevistas com pessoas **fora do círculo pessoal do fundador e que nunca viram ou usaram o TAIRU**, validando se o problema relatado é o mesmo de Nando, Nelson e Vera, e se a proposta de valor faz sentido para esse público.
- Definir, por escrito, os critérios de sucesso e fracasso do teste do Mês 3 (antes de rodar o teste, não depois).

**Entregável:** ICP definido, proposta de valor validada (ou não) com a pesquisa, e critérios de sucesso/fracasso.

### Mês 2 — Desenho do protótipo

**Objetivo:** desenhar o protótipo de acordo com os feedbacks coletados, seguindo um fluxo mais linear e simples de ponta a ponta, com os principais assuntos trazidos pelos feedbacks e pelo mapeamento de mercado.

**Atividades:**
- Redesenhar as telas centrais reunindo os principais pontos levantados nos feedbacks de Nando, Nelson e Vera (funcionalidades da seção 3) e no mapeamento de mercado (`02-pesquisa-mercado-consolidada.md`, `05-panorama-mercado-detalhado.md`).
- Priorizar um fluxo linear, passo a passo, ponta a ponta, em vez da navegação ramificada e cheia de opções simultâneas do produto atual.
- Sem IA generativa; inputs simplificados, mas **sem perder os campos que os testes anteriores mostraram fazer falta** (múltiplos destinos, múltiplas moedas, nº de voo, checkout).
- Adaptar a comunicação visual e o tom do protótipo para o ICP definido no Mês 1 — não é só simplificar telas, é desenhar linguagem e apelo visual voltados a esse público específico, não genéricos.
- Preparar roteiro de teste de protótipo (adaptado de `08-roteiro-entrevista-feedback.md`), incluindo pergunta explícita de disposição a pagar/substituir o método atual — não só "gostou da tela".

**Entregável:** protótipo clicável do fluxo de ponta a ponta + roteiro de teste.

### Mês 3 — Teste do fluxo com o ICP e do modelo comercial

**Objetivo:** testar o fluxo com o ICP e testar um modelo comercial com esse mesmo público; consolidar os resultados já indicando o que vale ser implementado e o que precisa de ajuste.

**Atividades:**
- Sessões moderadas de teste do protótipo com o ICP (recomendado: 6 a 8 pessoas, incluindo Nelson e Vera como comparação "antes vs. depois", mas não como maioria da amostra).
- Testar um modelo comercial junto ao mesmo grupo — mapeado dentro da própria pesquisa, não como etapa separada —, perguntando diretamente se pagariam e quanto, com referência de preço competitivo frente aos concorrentes (média de mercado perto de R$ 20/mês).
- Verificar, funcionalidade por funcionalidade, se ela faz sentido pro ICP e se ele reconhece a mesma dor que motivou aquela funcionalidade.
- Rodar em paralelo, e separado do teste principal, uma validação leve do canal de distribuição (H2): 1-2 conversas exploratórias com operadores de excursão/viagem em grupo.
- Consolidar os resultados contra os critérios de sucesso/fracasso definidos no Mês 1, já indicando o que vale ser implementado e o que precisa de ajuste.

**Entregável:** relatório de validação com o que foi validado (pronto para implementação), o que precisa de ajuste, e recomendação geral: seguir para desenvolvimento, ajustar e testar de novo, ou (só se o conjunto não se sustentar) considerar pivô total da ideia original.

---

## 5. Proposta de trabalho

**Objetivo geral:** validar a dor, a proposta de valor e a disposição a pagar de pessoas além dos amigos do fundador — o processo correto de desenvolvimento de produto que não foi feito antes de construir a primeira versão — antes de qualquer novo investimento em desenvolvimento de software.

**Formato:** consultoria de produto, com entregas mensais e um ponto de decisão claro ao final do 3º mês.

**Cronograma:**
- **Mês 1** — Definição de ICP e proposta de valor. *Entrega: ICP definido + proposta de valor validada com a pesquisa + critérios de sucesso/fracasso.*
- **Mês 2** — Desenho do protótipo. *Entrega: protótipo navegável do fluxo de ponta a ponta + roteiro de teste.*
- **Mês 3** — Teste do fluxo com o ICP e do modelo comercial. *Entrega: relatório de validação com o que implementar e o que ajustar.*

**Papéis:**
- Consultoria (Adriana): condução das entrevistas, desenho do protótipo, moderação dos testes, consolidação e recomendação final.
- Fundador: entrevista aprofundada sobre a dor original (já realizada), validação das decisões de escopo em cada etapa, eventual apresentação a operadores de excursão para testar o canal de distribuição (H2), e decisão final sobre seguir, ajustar ou pivotar ao final do ciclo. A recrutação das pessoas do ICP para entrevista é feita pela consultoria, **fora da rede pessoal do fundador**, para preservar a isenção do teste.

**O que este ciclo explicitamente não inclui:** desenvolvimento de software, contratação de dev ou software house, ou definição fechada de modelo de monetização — essas decisões ficam para depois da validação, condicionadas ao resultado do Mês 3. Os 3 meses validam a dor, a proposta e a disposição a pagar; a implementação de desenvolvimento é uma fase seguinte, só decidida depois.

**Investimento:** R$ 5.500/mês, totalizando R$ 16.500 pelo ciclo de 3 meses — parcela mensal fixa, alinhada ao formato de continuação mencionado em `03-escopo-projeto-consultoria.md`.

**Próximo passo após os 3 meses:** com o relatório de validação em mãos, a decisão entre (a) seguir para desenvolvimento da versão validada, (b) rodar um segundo ciclo de ajuste nas partes não validadas, ou (c) considerar pivô total, deixa de ser uma escolha por intuição e passa a ser uma escolha embasada em teste real com o ICP — o processo correto de desenvolvimento de produto, feito desta vez antes de construir.

---

## 6. O que você vai ter ao final dos 3 meses

- **Fluxo de ponta a ponta com validação real** — não mais uma hipótese de produto, e sim um fluxo de planejamento, acompanhamento e memória testado com o ICP, com dados de aceitação e disposição a pagar, não apenas opinião sobre telas.
- **Comprovação se vale a pena construir de fato nessa linha** — resposta objetiva, funcionalidade por funcionalidade, sobre o que está validado e pronto para implementação e o que precisa de revisão, antes de qualquer linha de código ser escrita.
- **Todos os requisitos técnicos para desenvolver a solução, evitando retrabalho com o desenvolvedor** — o protótipo navegável e a estrutura de dados corrigida (multi-destino, multi-moeda, campos de transporte e hospedagem, colaboração entre membros) funcionam como especificação validada, reduzindo idas e vindas de interpretação com o time de dev.
- **Diminuição do trabalho do dev** — como o fluxo já chega desenhado, testado e ajustado a nível de protótipo, o time de desenvolvimento entra direto na construção do que já foi validado, sem gastar ciclos de sprint testando hipóteses de produto no código.
- **Uma solução mais certeira e diferenciada** — o próximo investimento em desenvolvimento é direcionado para construir o que o público-alvo, além dos amigos do fundador, já demonstrou que quer e pagaria, com uma proposta de valor clara sobre pra quem e para qual dor o produto existe.
