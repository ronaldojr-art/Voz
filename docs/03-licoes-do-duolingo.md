# 03 — Lições do Duolingo: o que entra, o que adapta, o que fica de fora

> A tese do doc 01 é "o Duolingo da fala". Este doc decide o que isso quer dizer na prática: quais mecânicas a gente pega, quais muda e quais recusa.

## Como este estudo foi feito

Por observação do produto e material público (blog e entrevistas do time do Duolingo). **Sem engenharia reversa.** Avaliamos a ferramenta REA (`morluto/rea`), que desmonta apps sem o código-fonte, e descartamos em 14/11/2026 por três motivos: o que queremos são decisões de produto, visíveis para quem usa o app; o código de um app nativo com servidor não serve para uma página web; e termos de uso de apps comerciais costumam proibir engenharia reversa, um risco sem ganho para um produto que queremos lançar.

## O veredito, mecânica por mecânica

| Mecânica do Duolingo | Por que funciona | Veredito | Versão do Vozi |
|---|---|---|---|
| Trilha visual com unidades | Mostra onde estou e o que vem; cada unidade fechada é uma pequena vitória | ✅ **Entra** | Trilha de 30 dias em 4 unidades (seção abaixo) |
| Lição de poucos minutos com retorno imediato | Baixa a barreira para começar; termina antes de cansar | ✅ **Entra** (já temos) | Os 5 passos em ~5 min, com a reescuta como retorno |
| Mascote com personalidade | Dá um rosto à marca e um tom à conversa | ✅ **Entra** (já temos) | O Vozi, o amigo que ouve (doc 02) |
| Meta escolhida no primeiro dia | Compromisso próprio vale mais que meta imposta | ✅ **Entra** | "O que mais te atrapalha?" + quantos dias por semana você quer treinar |
| Comemoração de progresso | Pico-fim: a sessão termina bem | ✅ **Entra** (já temos) | Vozi comemorando no fim; marcos ao fechar unidade |
| Pontos por atividade (XP) | Transforma esforço em número; base das ligas | 🔧 **Adapta** | Pontos só por esforço, nunca por qualidade da fala |
| Ligas semanais | Competição leve entre pessoas parecidas; motivo para voltar hoje | 🔧 **Adapta** | Ligas por esforço, opcionais (seção abaixo) |
| Sequência de dias (streak) | Aversão à perda segura o hábito | 🔧 **Adapta** | Trilha da semana que não zera; marcos por total de dias |
| Lembretes | Trazem a pessoa de volta no horário dela | 🔧 **Adapta** | Um lembrete por dia, no horário escolhido, que a pessoa liga se quiser |
| Corações ou energia que travam o uso | Empurra para a assinatura | ❌ **Fora** | Treino livre e ilimitado, sempre |
| Notificação de culpa | Funciona no curto prazo, corrói a relação | ❌ **Fora** | O Vozi nunca cobra. Faltou? "Que bom te ver" |
| Sequência que zera | Pune quem teve um dia ruim | ❌ **Fora** | Nada zera |
| Concorrentes falsos em liga | Enche a tabela artificialmente | ❌ **Fora** | Só gente de verdade; liga pequena se a base for pequena |

## As ligas do Vozi

**DECIDIDO (fundador, 14/11/2026): o Vozi terá ligas competitivas.** Elas dão motivo para entrar no app e abrem caminho para premiações no futuro. Isso revê o doc 01, que listava comparação social entre as coisas que não fazemos. A linha nova é: **liga por esforço, sim; ranking de quem fala melhor, não.**

O motivo da linha: o público do Vozi chega inseguro com a própria fala. Uma tabela de "quem fala melhor" espanta exatamente quem mais precisa. Uma tabela de "quem apareceu" premia o comportamento que melhora a fala de qualquer um.

Referência de impacto: Jorge Mazal, ex-diretor de produto do Duolingo, relatou que as ligas aumentaram o tempo total de estudo em cerca de 17% e triplicaram os usuários muito engajados. Número citado de memória; conferir antes de usar em material externo.

### Regras

| Regra | Como funciona | Por quê |
|---|---|---|
| O que pontua | Treino completo, minutos de fala livre, fechar unidade da trilha | Esforço, não talento |
| O que não pontua | Ritmo, muletas, clareza, qualquer nota da fala | Ninguém perde por falar rápido ou enrolado |
| Teto diário | Pontos de no máximo 2 treinos por dia | Evita maratona e trapaça; cinco minutos continuam bastando |
| Tamanho | 20 a 30 pessoas de nível de uso parecido | Posição alcançável, não um ranking de milhares |
| Ciclo | Semanal, zera toda segunda | Quem entra tarde ainda tem chance |
| Subida | Os primeiros sobem de liga | Progresso de longo prazo |
| Descida | Quem fica embaixo permanece; rebaixa só após 2 semanas sem treinar | Sem aviso vermelho, sem humilhação |
| Participação | Opcional, com apelido e o sabiá da pessoa | Autonomia e privacidade |
| Áudio | Nunca exposto a outros usuários | A gravação é de quem gravou |

**Pontuação inicial (proposta, a calibrar com uso):** 10 pontos por treino completo, 1 ponto por cada 10 segundos de fala livre, 20 pontos por fechar uma unidade.

**Nomes das ligas (proposta):** pássaros brasileiros, do comum ao raro. Pardal → Bem-te-vi → Sabiá → Tangará → Uirapuru.

### Premiações, em duas fases

| Fase | Prêmio | O que exige |
|---|---|---|
| **A — interna** (junto com as ligas) | Um mês de premium, acessórios para o Vozi, selo da semana | Nada além do próprio app |
| **B — externa** (com base e patrocinador) | Prêmio físico, vale ou dinheiro | Autorização legal, verificação de fala real, regulamento público |

Três cuidados da fase B:

1. **Lei.** No Brasil, distribuição de prêmios em promoção comercial é regulada (Lei 5.768/1971) e costuma exigir autorização do Ministério da Fazenda. Consultar advogado antes de anunciar qualquer prêmio.
2. **Trapaça.** Prêmio de verdade atrai quem deixa o microfone aberto sem falar. Os pontos passam a contar só com fala detectada pelo servidor.
3. **Lojas.** Apple e Google têm regras próprias para concursos dentro de apps. Verificar na fase de loja.

### O que as ligas exigem

Conta, servidor e uma base mínima de usuários ativos. Não cabem no protótipo atual, que guarda tudo no navegador. Entram na v1, depois da etapa 3 do doc 01.

### Critérios de passa ou não passa (primeiro mês de ligas)

- **Adesão:** pelo menos 30% dos usuários ativos escolhem entrar.
- **Efeito:** quem entra treina mais dias por semana do que treinava antes de entrar.
- **Segurança:** em pesquisa dentro do app, menos de 5% dizem que a liga os fez sentir pior sobre a própria fala. Se passar disso, a liga volta para a prancheta.

## A trilha de 30 dias (esboço)

Hoje o conteúdo é sorteado pela data. A trilha troca o sorteio por progressão: os mesmos 5 passos todo dia, com uma ênfase por semana.

| Unidade | Dias | Foco | O que muda no treino | Marco |
|---|---|---|---|---|
| 1. Fôlego | 1–7 | Respirar baixo e desacelerar | Respiração mais longa; leitura a 110 palavras/min | Dia 1: gravação "antes" |
| 2. Pausa | 8–14 | Parar nas vírgulas e nos pontos | Leitura com pausas marcadas; fala livre com "pause depois de cada ideia" | Fecha a unidade: Vozi comemora |
| 3. Clareza | 15–21 | Articular sem correr | Trava-línguas mais longos; leitura a 130 palavras/min | Reescuta comparada com o dia 1 |
| 4. Estrutura | 22–28 | Saber o que falar | Um molde por dia; temas de situação real (reunião, apresentação) | Fecha a unidade: Vozi comemora |
| Fechamento | 29–30 | Antes e depois | Mesmo tema do dia 1, regravado | Dia 30: ouvir as duas gravações lado a lado |

Regras da trilha, na filosofia da casa: o dia da trilha avança quando a pessoa treina, não quando o calendário anda. Quem falta três dias volta no mesmo ponto. Nada zera.

**A trilha cabe no protótipo atual**, sem servidor. É a próxima coisa a construir quando a etapa 0 trouxer a lista de incômodos do uso real.

## O que muda no plano

- [x] Decisão: ligas por esforço entram no produto (v1)
- [x] Doc 01 revisto (auditoria de gatilhos, monetização, v1)
- [ ] Trilha de 30 dias no protótipo (próxima construção, após a etapa 0)
- [ ] Ligas + pontos + premiação interna (v1, após a etapa 3)
- [ ] Consulta jurídica sobre premiação externa (antes de anunciar qualquer prêmio)
