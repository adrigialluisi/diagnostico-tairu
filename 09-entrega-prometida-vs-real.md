# TAIRU — Entrega Prometida (Pitch) vs. Entrega Real (Frente 04 do diagnóstico)

Cruzamento entre o que o pitch (`Apresentação TAIRU 2.pdf`) promete e o que a análise de usabilidade (`01-analise-usabilidade.html`) e as duas entrevistas de feedback (`03-feedback-existente.html`, Nelson e Vera) mostram que o produto entrega hoje. Cada bloco traz a promessa literal do pitch, a evidência real encontrada, e um status.

Legenda de status: 🟢 Entregue · 🟡 Parcial / aquém do prometido · 🔴 Não entregue · ⚪ Não verificável com os dados atuais

---

## 1. Planejamento assistido
**Promessa do pitch:** reserva acomodações, pesquisa voos mais baratos, sugere espetáculos, passeios e atrações conforme perfil e interesses do usuário.

**Realidade:**
- A trilha de planejamento (Nome → Datas → Destinos → Acomodações → Transporte → Convidar → Resumo) existe, mas todos os campos são 100% digitação manual, sem autocomplete ou sugestão (achado da análise de usabilidade).
- Não há evidência de busca de voo mais barato, reserva integrada, nem sugestão de passeios por perfil em nenhuma das duas entrevistas.
- Nelson organizou hotel e transporte inteiramente fora do app; a esposa dele mantém controle próprio em planilha.
- O quiz de estilo de viagem (proxy do "perfil de interesses") é preenchido uma única vez no onboarding e, segundo Vera, "não parece influenciar nada nas sugestões".

**Status:** 🔴 Não entregue — a promessa é de curadoria ativa; o que existe é um formulário manual.

---

## 2. Carteira de documentos
**Promessa do pitch:** centraliza reservas, tickets de atrações e seguros de viagem, evitando que o usuário precise procurá-los espalhados em e-mail/WhatsApp.

**Realidade:**
- Conceito validado como ponto forte na análise de usabilidade ("centralizar os documentos da viagem... facilita bastante o acesso").
- Mas Vera encontrou erro técnico real e reproduzível: botão "ver" não abre o documento, com mensagem de erro exata **"URL do documento não disponível"** — bug de storage/link, não lentidão.
- Nelson pouco usou; preferiu a carteira digital da Apple.

**Status:** 🟡 Parcial — a ideia está certa, a execução tem um bug crítico que quebra a função central da feature.

---

## 3. Timeline automática
**Promessa do pitch:** gera automaticamente, dia a dia e hora a hora, um registro de lugares visitados, gastos, fotos, comida e bebida — sem o usuário precisar alimentar dados manualmente.

**Realidade:**
- A palavra-chave da promessa é "automática". Na prática, cada evento da timeline precisa ser criado manualmente pelo usuário.
- Nelson achou o input manual cansativo e, por isso, só registrou os eventos "grandes" (lazer), deixando de fora logística (transporte com custo R$ 0,00 registrado só como diário depois).
- O único ponto de automação real testado — geolocalização via IA ao criar um evento com foto — errou o local (evento registrado longe do ponto real, mesmo com GPS ativado), sem pedir confirmação ao usuário antes de salvar.
- Lançar um gasto depende de criar um evento; não existe lançamento direto na tela de Gastos.

**Status:** 🔴 Não entregue — é uma timeline manual com um recurso de IA que errou no único teste registrado. Este é o gap mais grave, porque "automação sem esforço manual" é o eixo central do discurso comercial do pitch.

---

## 4. Mapa dinâmico
**Promessa do pitch:** atualiza a rota percorrida em tempo real, marcando os lugares visitados automaticamente.

**Realidade:**
- O mapa existe e foi elogiado por Vera ("mapa automático ao inserir endereço numa atividade"), mas é acionado por evento inserido manualmente, não por rastreamento passivo em tempo real (como Polarsteps faz, por comparação de mercado).
- O caso de geolocalização incorreta via IA (item 3) também afeta diretamente a confiabilidade deste mapa.

**Status:** 🟡 Parcial — funciona bem quando o dado de entrada é manual e correto; não há "rota em tempo real" automática, e já houve erro de localização.

---

## 5. Controle financeiro
**Promessa do pitch:** contabiliza os gastos da viagem por categoria.

**Realidade:**
- Existe e Vera elogiou a "agregação automática de despesas de várias atividades numa única tela".
- Mas: gasto só entra via criação de evento (fricção para lançamentos rápidos e frequentes); valor total aparece em fonte grande e destacada em várias telas, inclusive fora da aba de gastos, o que Vera sinalizou como excessivo; e não há conversão multi-moeda nem divisão de despesas em grupo — o app aceita só 1 moeda por viagem.

**Status:** 🟡 Parcial — funcionalidade central existe, mas sem os dois recursos que o mercado (Stippl, por exemplo) já entrega: multi-moeda e split em grupo.

---

## 6. Notificações automáticas
**Promessa do pitch:** status de voos, previsão do tempo, check-in, atividades programadas.

**Realidade:**
- Nenhuma das duas entrevistas menciona ter recebido qualquer notificação — nem confirmando, nem reclamando de atraso/erro.
- Mais grave: o formulário de transporte nem tem campo de número de voo ou horário de chegada (achado direto de Vera). Sem esse dado estrutural cadastrado, uma notificação de status de voo é tecnicamente inviável hoje, independente de a funcionalidade existir no backend.

**Status:** 🔴 Não entregue (ou, na melhor hipótese, ⚪ não testável, pois falta o dado-base que a alimentaria).

---

## 7. Automação como diferencial central
**Promessa do pitch:** "tudo isso acontece automaticamente, sem exigir que o usuário fique alimentando dados manualmente" — mencionado repetidamente como o diferencial do produto.

**Realidade:** esta é a promessa mais distante do que foi observado em qualquer frente do diagnóstico:
- Todo o fluxo de planejamento é manual, sem autocomplete.
- A timeline depende de criação manual de evento por evento.
- O único recurso de automação testado (geolocalização por IA) errou.
- O quiz de personalização não demonstra impacto percebido nas sugestões, segundo Vera.

**Status:** 🔴 Não entregue — é o maior gap entre discurso e produto real, porque é justamente o argumento usado para justificar por que o TAIRU seria diferente dos concorrentes especializados (Wanderlog, TripIt, Polarsteps).

---

## 8. Assistente conversacional
**Promessa do pitch:** responde perguntas pontuais do tipo "restaurante aberto de madrugada", "melhor caminho de volta ao hotel" — o "alguém pra perguntar" do viajante.

**Realidade:**
- Nelson relatou explicitamente que **não sabia que o app tinha IA e recursos automáticos** — problema de descoberta de funcionalidade tão grave quanto um problema de ausência da funcionalidade.
- Nenhum dos dois entrevistados menciona ter usado ou visto um assistente conversacional.

**Status:** 🔴 Não entregue (ao menos não de forma descobrível pelo usuário) — falha de discovery/onboarding, ou funcionalidade ainda não lançada.

---

## 9. Sincronização em grupo
**Promessa do pitch:** viajantes em família ou grupo podem se convidar e acompanhar a viagem em tempo real, sincronizados.

**Realidade — a funcionalidade mais frágil encontrada em todo o diagnóstico:**
- Convites enviados por Nelson não funcionaram: os convidados nunca viram a mesma viagem.
- Bug de sincronização confirmado: ao renomear a viagem de "Buenos Aires" para "São Paulo", o e-mail de convite foi enviado com o nome antigo — o convite chega com informação desatualizada.
- Lista de contatos sugerida na tela de convite é inconsistente entre sessões, sem critério claro, e não persiste.
- Convite só pode ser enviado por e-mail — sem link compartilhável por WhatsApp, o canal mais usado no Brasil para esse tipo de compartilhamento.
- Dentro da tela "Membros da viagem", convites pendentes não aparecem (só no menu principal), dificultando gestão por quem organiza a viagem.
- Estruturalmente, o limite de 1 destino por viagem já dificulta o caso de uso que Nelson pediu (família com destinos diferentes, otimizados em conjunto).

**Status:** 🔴 Não entregue — citada por ambos os entrevistados como funcionalidade desejada, mas não testada com sucesso por nenhum dos dois.

---

## 10. Consolidação de apps ("substituir um monte de aplicativos")
**Promessa do pitch:** TAIRU como camada única, eliminando a necessidade de abrir vários apps durante a viagem.

**Realidade:** o próprio uso relatado por Nelson contradiz a promessa — ele usou Google Maps para descoberta de locais (não o TAIRU), a carteira digital da Apple para documentos (não a Carteira do TAIRU), e uma planilha externa para planejamento (feita pela esposa). Ou seja, na prática ele manteve o mesmo número de apps/ferramentas de sempre, com o TAIRU rodando em paralelo como diário.

**Status:** 🔴 Não entregue no uso real observado.

---

## O que está *melhor* do que o esperado / é o ponto forte real

- **Álbum de fotos e revisão pós-viagem** — não é uma promessa detalhada no pitch além de "arquivar memórias em álbuns", mas é, sem concorrência, o item mais elogiado nas duas fontes: análise de usabilidade cita a Carteira de documentos como ponto forte, e Nelson chamou o álbum pós-viagem de "principal virtude do app".
- **Linha do tempo organizada por dia** (quando alimentada manualmente) — Nelson avaliou bem a organização, mesmo usando só uma fração da funcionalidade.
- **Campo de notas por evento** — usado organicamente por Nelson para guardar dicas práticas (ex.: "chegar 2h antes do pôr do sol"), sugerindo que há apetite real do usuário para esse tipo de conteúdo — hoje represado num campo de texto livre, sem virar produto (ver pedido de "dicas culturais/locais" abaixo).

## Padrão geral que emerge do cruzamento

O TAIRU entrega razoavelmente bem no **fim do ciclo** (diário, timeline organizada, álbum pós-viagem) e falha consistentemente:

1. **Na promessa central de automação** — o produto é hoje mais manual do que os concorrentes especializados que ele tenta superar (Wanderlog e TripIt, por exemplo, têm autocomplete e parsing de e-mail; o TAIRU não tem nenhum dos dois).
2. **Nas pontas estruturais do dado** — "Destino" e "Moeda" no singular, ausência de campo de nº de voo/checkout, são falhas de modelagem de dados, não de polimento visual, e explicam vários outros sintomas (colaboração em grupo travada, controle financeiro incompleto).
3. **Na colaboração/grupo** — a funcionalidade mais citada como desejada pelos dois entrevistados é também a mais quebrada tecnicamente.
4. **No discovery de IA** — mesmo onde a IA existe (geolocalização, quiz), o usuário não sabe que existe, não confia nela, ou não percebe efeito — o que, somado ao erro de geolocalização observado, é um risco reputacional a mais, coerente com a dor de "confiança na IA" já mapeada na pesquisa de mercado (`02-pesquisa-mercado-consolidada.md`).

## Pedido espontâneo dos dois usuários, ausente do pitch

Nelson e Vera pediram, de forma independente, **dicas culturais e locais** (evitar perrengues, costumes, gorjeta, lugares menos turísticos, comida boa e barata) — algo que o pitch não promete e que hoje só existe de forma improvisada no campo de notas livre. É o gap de produto mais consistente entre os dois relatos e não estava mapeado nem no pitch nem na pesquisa de mercado original.

---

## Tabela-resumo: prometido × real

| # | Promessa do pitch | Status | Em uma frase |
|---|---|---|---|
| 1 | Planejamento assistido (reserva, voos, sugestões por perfil) | 🔴 Não entregue | Trilha 100% manual, sem autocomplete; quiz de perfil não influencia sugestões |
| 2 | Carteira de documentos | 🟡 Parcial | Conceito bom, mas "ver documento" quebra com erro de URL |
| 3 | Timeline automática | 🔴 Não entregue | Cada evento é criado manualmente; único recurso de IA testado errou o local |
| 4 | Mapa dinâmico em tempo real | 🟡 Parcial | Funciona por evento manual, não por rastreamento passivo |
| 5 | Controle financeiro por categoria | 🟡 Parcial | Existe, mas sem multi-moeda, sem split em grupo, e preso à criação de evento |
| 6 | Notificações automáticas (voo, clima, check-in) | 🔴 Não entregue | Falta até o campo de nº de voo/horário — dado-base nem existe |
| 7 | Automação como diferencial central | 🔴 Não entregue | Maior gap do diagnóstico: produto é mais manual que os concorrentes que tenta superar |
| 8 | Assistente conversacional | 🔴 Não entregue | Usuário nem sabia que a IA existia — falha de descoberta |
| 9 | Sincronização em grupo | 🔴 Não entregue | Convites falharam tecnicamente; e-mail chegou com dado desatualizado |
| 10 | Consolidação de apps ("substituir vários apps") | 🔴 Não entregue | Usuário seguiu usando Google Maps, carteira Apple e planilha em paralelo |
| — | Álbum de fotos / diário pós-viagem | 🟢 Acima do prometido | Item mais elogiado nas duas fontes, "principal virtude do app" |

**Placar:** 1 entrega acima do esperado · 0 entregas plenas · 3 parciais · 7 não entregues.

---

## Conclusões

1. **A distância entre discurso e produto é estrutural, não cosmética.** Das 10 promessas centrais do pitch, nenhuma foi entregue por completo e 7 simplesmente não existem hoje na prática. Isso não é uma lista de bugs de polimento — são lacunas de modelagem de dados (destino/moeda no singular, ausência de campo de voo/checkout) e de arquitetura de produto (automação que depende de input manual), que não se resolvem com ajuste de UI.

2. **O diferencial vendido é o ponto mais fraco do produto.** O pitch se apoia quase inteiramente em "automação sem esforço manual" para justificar por que o TAIRU deveria vencer concorrentes especializados e maduros (Wanderlog, TripIt, Polarsteps, Stippl — ver `04-gaps-e-oportunidades-diferenciacao.md`). Hoje é o inverso: o produto é mais manual do que eles, e o único recurso de IA testado (geolocalização) errou. Enquanto essa lacuna existir, TAIRU compete em desvantagem em todos os quadrantes de mercado ao mesmo tempo, sem vencer nenhum.

3. **O produto já tem um núcleo de valor real, só que é outro.** O que funciona de verdade — timeline organizada, campo de notas usado organicamente, e principalmente o álbum de fotos pós-viagem — não é o argumento central do pitch (automação/planejamento), e sim a experiência de registro e memória, mais perto do território do Polarsteps do que do Wanderlog ou TripIt. Isso é uma pista de posicionamento, não só um achado de usabilidade: há um produto menor, mais honesto e mais forte escondido dentro da promessa atual de "fazer tudo".

4. **Colaboração em grupo é hoje um risco de confiança, não uma feature em desenvolvimento.** Falhou tecnicamente (convites), estruturalmente (1 destino/1 moeda por viagem) e informacionalmente (status de convite sumindo de tela em tela) ao mesmo tempo. É a funcionalidade mais pedida pelos dois entrevistados e a mais quebrada — prioridade caso o roadmap mantenha viagem em grupo como caso de uso central.

5. **O pedido não atendido mais consistente veio de fora do pitch.** Dicas culturais/locais foram pedidas espontaneamente por Nelson e por Vera, sem que nenhum dos dois soubesse que o outro faria o mesmo pedido, e sem que o pitch ou a pesquisa de mercado original tivessem mapeado essa dor. Vale investigar se isso é sinal de uma necessidade maior do público-alvo do que a proposta de valor atual assume.

6. **Recomendação de sequenciamento para as próximas frentes do diagnóstico (validação da proposta de valor e formatos de continuidade):** antes de qualquer decisão de crescimento ou aquisição de usuários, a pergunta que este cruzamento levanta é se o TAIRU deveria (a) investir pesado para fechar o gap de automação e sustentar a promessa atual de "tudo em um", ou (b) reposicionar o produto em torno do que ele já faz bem — registro, memória e diário de viagem — como uma aposta mais estreita, mas mais defensável. Essa decisão estratégica, não a lista de bugs, é o verdadeiro ponto de virada do diagnóstico.

---

*Fontes: `Apresentação TAIRU 2.pdf` (pitch, 15 páginas) · `01-analise-usabilidade.html` (achados de usabilidade heurística) · `03-feedback-existente.html` e memória de entrevistas (Nelson, 20/07/2026; Vera, 22/07 e 28/07/2026) · `02-pesquisa-mercado-consolidada.md` (contexto de mercado citado nas leituras cruzadas).*
