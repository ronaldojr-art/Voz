# 01 — Voz como produto: visão, mercado e plano de validação

> **Tese:** o Duolingo da fala, em português. Cinco minutos por dia para quem fala rápido, enrolado, ou trava e não sabe o que dizer.

Este doc segue o formato do estúdio (Lambari-pescado, docs 01, 02 e 04): engajamento ético, validação barata antes de construir, e critérios explícitos de passa ou não passa. O protótipo está em `index.html`; o método em [metodo.md](metodo.md).

## 1. O problema e o público

Medo de falar é um dos medos mais comuns que existem. A versão cotidiana dele não é "dar palestra": é a reunião de trabalho, a apresentação na faculdade, o pedido de aumento, a conversa com alguém que importa. O sintoma vem em três formas, geralmente juntas:

| Como a pessoa descreve | O que está acontecendo | O que o Voz treina |
|---|---|---|
| "Falo rápido demais" | Respiração curta e alta; boca correndo atrás do pensamento | Respiração baixa; leitura com ritmo-alvo e pausas marcadas |
| "Falo enrolado" | Articulação preguiçosa | Trava-línguas devagar e exagerado |
| "Dá branco, não sei o que falar" | Começa do zero, sem molde; o branco vira pânico | Molde fixo + permissão explícita de pausar |

**Público-alvo inicial:** adultos de 20 a 45 anos, no Brasil, que já perceberam que a fala os atrapalha e já tentaram "só falar mais devagar" sem sucesso. Não é o executivo que apresenta para a diretoria (esse já tem Yoodli e coach). É quem nunca teria um coach.

**Momento de dor (quando a pessoa baixa o app):** depois de uma situação ruim. Uma reunião em que travou, uma apresentação que correu. Por isso o conteúdo de aquisição precisa falar do sintoma ("você fala rápido demais?"), não da solução ("melhore sua oratória").

## 2. Mercado e concorrência

| Produto | O que faz | Preço | Fraqueza para o nosso público |
|---|---|---|---|
| Yoodli | IA analisa gravações e reuniões: muletas, ritmo, repetição | Grátis limitado (~5 gravações); pago US$ 8–28/mês | Inglês, computador, foco em reunião corporativa |
| Speeko | Exercícios curtos diários, análise de ritmo e entonação, streaks | Assinatura | Inglês; o modelo de streak pune quem falta |
| Orai | Pioneiro no celular, nota por gravação | Freemium | Inglês; fontes divergem se ainda está ativo |
| Poised | Dicas em tempo real durante reunião online | Assinatura | Outro problema (ao vivo, não treino) |
| Cursos de oratória BR | Presenciais ou online, 8 a 40 horas | R$ 300 a 3.000 | Caro, exige agenda, zero hábito diário |
| Fonoaudiólogo | Tratamento individual | R$ 150–300 por sessão | Certo para gagueira; caro e inacessível para "só falo rápido" |

**Lacuna:** não existe app consolidado em português para treino diário de fala. Em inglês, nenhum concorrente faz respiração e articulação antes da fala, e todos usam streak com punição.

**Diferenciais do Voz:**
1. Português, com trava-línguas e textos nossos, no tom de um amigo e não de um coach.
2. Cinco minutos no celular, sem conta, grátis no núcleo.
3. Sem streak, sem punição ("a trilha não zera, ela só espera"), que é também a filosofia inteira do estúdio.
4. Corpo antes da fala: respiração e articulação, que é onde o "rápido" e o "enrolado" realmente nascem.

## 3. Os riscos, sem maquiagem

| Risco | Por que é real | Como a gente responde |
|---|---|---|
| **Retenção** | App de hábito morre no dia 8; autoajuda tem o churn mais alto do mercado | Medir retorno no dia 7 com gente real antes de construir qualquer coisa (seção 5) |
| **Feedback fraco** | O reconhecimento de fala do navegador é ruim em português; sem feedback bom, a reescuta vira só "me ouvi" | Transcrição de qualidade + análise por IA no premium (seção 6) |
| **Fosso raso** | O código é copiável em uma semana | O fosso é conteúdo em português, marca com tom próprio, base que confia, e dados de progresso do usuário |
| **"Funciona?"** | Se não houver melhora perceptível em 30 dias, não há boca a boca | Programa de 30 dias com antes/depois gravado, que a própria pessoa compara |
| **Distribuição** | Sem orçamento de mídia | Conteúdo curto sobre o sintoma (seção 5, etapa 3) é ao mesmo tempo teste de demanda e canal |

## 4. Auditoria de gatilhos (doc 02 do estúdio, aplicado)

| Gatilho | Versão do Voz | O que NÃO fazemos |
|---|---|---|
| Hábito por rotina | Trilha da semana, treino de hoje, conteúdo sorteado pela data ("edição de hoje") | Streak que zera; notificação de culpa |
| Progresso visível | Antes/depois gravado; ritmo médio caindo; muletas por minuto caindo | Barra que só anda pagando |
| Competência (autodeterminação) | Dica do dia aplicável numa conversa real; "uma coisa pra amanhã" | Notas e rankings que humilham |
| Pico-fim | Fim do treino com dia marcado e frase gentil | Pop-up de upgrade no fim do treino |
| Recompensa variável | Tema e molde do dia são uma pequena surpresa | Loot, moedas, gacha (não cabe aqui) |
| Identidade | "Sou alguém que treina a voz todo dia" | Comparação social |

## 5. Plano de validação (cada etapa tem critério de passa ou não passa)

**Etapa 0 — O fundador (4 semanas).** Usar o protótipo todo dia. *Passa se:* 20 de 28 dias. Se nem o fundador aparece, não tem produto. Saída: lista do que incomodou no uso real (durações, textos, o que faltou).

**Etapa 1 — O círculo (10 pessoas, 2 semanas).** As mesmas pessoas que testaram o Feira Pop, mais duas ou três que já disseram "eu falo rápido". Entrega-se o link e nada mais: zero lembretes. *Passa se:* 4 ou mais voltam no dia 7 sem serem lembradas, e pelo menos 2 dizem espontaneamente que perceberam diferença. *Métrica secundária:* alguém pergunta "posso mandar pra fulano?".

**Etapa 2 — Demanda (2 semanas, custo zero).** Três a cinco vídeos curtos (Instagram/TikTok) sobre o sintoma: "você fala rápido demais? faz isso por 5 minutos". Link na bio para o app. *Passa se:* um vídeo passa de 10 mil visualizações orgânicas OU 200 pessoas abrem o app pelo link. O conteúdo que der certo vira o canal permanente.

**Etapa 3 — Disposição a pagar (só se 1 e 2 passarem).** Botão "quero feedback de IA" que leva a uma lista de espera com preço indicado. *Passa se:* 5% de quem vê clica e deixa e-mail.

**Etapa 4 — v1 de produto.** Só aqui entra construção de verdade (seção 7).

Cada etapa que não passa gera um doc curto com o que aprendemos, e a decisão de ajustar ou parar. Parar cedo é vitória do método, não derrota do produto.

## 6. Monetização (doc 04 do estúdio, aplicado)

**Regra:** o treino diário é grátis para sempre, sem anúncio, sem energia, sem streak. Quem paga, paga por **ouvir uma opinião boa sobre a própria fala** e por **programas para momentos específicos**.

| | Grátis | Premium (R$ 14,90 a 19,90/mês, ou anual com desconto) |
|---|---|---|
| Treino diário dos 5 passos | ✅ | ✅ |
| Trilha, diário, dicas | ✅ | ✅ |
| Histórico | últimos 30 treinos | completo, com gráfico de ritmo e muletas |
| Feedback de IA por gravação (transcrição boa, muletas, ritmo por trecho, estrutura, "o que mudar amanhã") | 3 por mês | ilimitado |
| Programas temáticos (entrevista, apresentação, pedir aumento, conversa difícil) | — | ✅ |
| Modo "antes de uma conversa importante" (90s) | ✅ | ✅ |

**O que nunca entra:** anúncio no meio do treino, notificação de culpa, streak que zera, desconto por pressão ("só hoje"), venda de dados de voz. O áudio é do usuário; análise premium processa e descarta.

**Conta de padaria:** transcrição e análise por IA custam centavos por minuto de áudio. Um usuário premium gravando 1 minuto por dia custa bem menos de R$ 2 por mês em servidor. Margem confortável a partir de poucos milhares de assinantes; o custo real é aquisição, não infraestrutura.

## 7. Produto v1 (só após a etapa 3)

- **PWA instalável:** ícone na tela inicial, funciona offline, o que já é 80% do caminho sem loja.
- **Onboarding por sintoma:** "O que mais te atrapalha?" (rápido, enrolado, branco) monta ênfase do plano. Primeira gravação de 30s vira o "antes".
- **Programa de 30 dias:** conteúdo progressivo em vez de sorteio; dia 30 compara com o dia 1.
- **Feedback de IA (premium):** transcrição de qualidade, análise de ritmo por trecho, muletas, estrutura (seguiu o molde?), e uma única sugestão para amanhã, em tom de amigo.
- **Conta opcional:** só para sincronizar entre aparelhos e para o premium. Sem conta continua funcionando.
- **Lojas (Android primeiro):** quando a PWA provar retenção.

**Stack:** continua web (HTML único hoje; migrar para componentes quando doer). Backend mínimo só para o premium: transcrição + análise por modelo de linguagem, por minuto de áudio.

## 8. Nome e marca

"Voz" é bom como nome de trabalho e fraco como marca: genérico demais para loja, busca e registro. Rodada de candidatos a fazer, no mesmo molde do Feira Pop (sonoridade, zero associação ruim, distintivo para ASO, verificação INPI e domínio na fase de loja). Critério: precisa dizer calma, não performance. O produto não promete "oratória", promete "falar tranquilo".

## 9. Decisões e próximos passos

- [ ] **Etapa 0 em andamento:** fundador usa 4 semanas (começou em nov/2026)
- [ ] Lista de incômodos do uso real → ajustes no protótipo
- [ ] Etapa 1: círculo de 10
- [ ] Etapa 2: vídeos sobre o sintoma
- [ ] Rodada de nomes
- [ ] Decisão de passa ou não passa para v1
