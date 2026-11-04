# Voz — treino diário de fala

> **O problema, nas palavras do fundador:** "as palavras somem, eu falo rápido, enrolado, não sei o que falar… parece que tá tudo errado."

Esse protótipo usa a mesma filosofia da casa (sessão curta, ritual diário sem punição, o usuário fecha o app melhor do que abriu) para um problema que não é jogo: **falar com clareza e calma**. Está em `index.html`. Funciona no celular, sem backend, sem conta.

## O diagnóstico por trás do desenho

Os três sintomas descritos são, na prática, um sintoma só em três lugares:

| Sintoma | O que geralmente está acontecendo | O que treina |
|---|---|---|
| "Falo rápido" | Respiração curta e alta (peito), e a boca correndo atrás do pensamento | Respiração baixa; leitura com ritmo-alvo e pausas marcadas |
| "Falo enrolado" | Articulação preguiçosa: língua, lábios e mandíbula não acompanham a velocidade | Trava-línguas **devagar e exagerado** antes de acelerar |
| "As palavras somem / não sei o que falar" | Começar do zero, sem molde; o branco vira pânico, o pânico acelera a fala | Molde fixo (ponto, porque, exemplo, ponto) + permissão explícita de pausar |

E o multiplicador de tudo: **ninguém melhora a fala sem se ouvir.** A reescuta é o passo mais importante e o mais evitado. Por isso ela é obrigatória no fluxo, e por isso o app grava.

## O treino (≈5 minutos, todo dia, sempre a mesma ordem)

1. **Respira (45s)** — 4 ciclos de 4-2-6 (inspira, segura, solta) com um orbe que cresce e encolhe. Mão na barriga.
2. **Articula (60s)** — um trava-língua do dia: 3x bem devagar mastigando sílabas, depois 2x normal.
3. **Lê no ritmo (90s)** — texto curto com marcação que avança no ritmo-alvo (padrão 130 palavras/min, ajustável de 90 a 180) e **para nas vírgulas e pontos**. Ler acompanhando a marca ensina velocidade constante e pausa no lugar certo. Depois, ler uma vez sem a marca.
4. **Fala livre (60s)** — tema do dia + molde do dia, gravado pelo microfone. "Pausar é permitido. Silêncio não é erro." Se o navegador suportar reconhecimento de fala (Chrome), o app conta palavras e muletas ("tipo", "né", "aí", "então"...).
5. **Reescuta** — ouvir o áudio inteiro; ver tempo falado, palavras por minuto e muletas; se avaliar em ritmo, clareza e pausas; anotar "uma coisa que foi bem" e "uma coisa pra amanhã".

Conteúdo sorteado pela data (igual à Feira do Dia): mesmo dia, mesmo tema/texto/trava-língua. Isso dá sensação de "edição de hoje" sem precisar de servidor.

## Sistemas (as regras da casa aplicadas)

| Sistema | Como funciona | Linha ética |
|---|---|---|
| Trilha da semana S-T-Q-Q-S-S-D | Marca o dia feito | **Sem streak, sem zerar, sem punição por faltar** ("a trilha não zera, ela só espera") |
| Estatísticas | Total de treinos, dias da semana, ritmo médio dos últimos 5 | Nada de ranking; a comparação é com você mesmo |
| Diário | Uma entrada por treino, com notas; exportar como texto | Fica no `localStorage`; os áudios **não** são salvos (somem ao fechar) |
| Dica do dia | 12 dicas práticas, uma no início e uma no fim | Linguagem de amigo, não de coach |

## O que a ciência sustenta (resumo honesto)

- **Ritmo:** conversa calma em português fica na faixa de ~120–150 palavras por minuto. O app rotula acima de 165 como "acelerado" e abaixo de 115 como "bem calmo". Treinar *abaixo* do alvo é desejável: quem treina a 120 fala a 140 sob pressão.
- **Pausas:** a percepção de "fala clara e segura" depende mais de pausas nas fronteiras de ideia do que de velocidade média. Por isso a leitura guiada para nas vírgulas e pontos, não só anda devagar.
- **Auto-monitoramento:** gravar e reescutar é a intervenção mais consistente em treinamentos de fala em público; o ganho vem da calibração ("soo melhor do que achava, e o rápido tem lugares específicos").
- **Estrutura reduz branco:** moldes do tipo PREP (Point, Reason, Example, Point) são padrão em treinamento de comunicação justamente porque eliminam o "por onde começo".
- **Respiração diafragmática** reduz ativação do sistema nervoso simpático e aumenta o ar disponível por frase, que é o que permite terminar frases sem acelerar no fim.

## Limites (e por que estão escritos no app)

Este treino mira fluência e segurança no dia a dia. **Gagueira, bloqueios fortes ou ansiedade que paralisa pedem fonoaudiólogo** (e, no caso da ansiedade, psicólogo). O app é bom complemento e não substitui. Está dito na tela "Como funciona".

## Como medir se está funcionando (4 semanas)

- A métrica que importa: **dias treinados** (não ritmo, não muletas). Vinte dias em quatro semanas já muda a fala.
- Métricas secundárias no diário: ritmo médio caindo pra faixa de conversa; muletas por minuto caindo; auto-avaliação de "pausas" subindo.
- Teste de campo: numa conversa real, usar conscientemente **uma** coisa do app (respirar antes de responder, ou terminar a frase com o tom descendo). Uma de cada vez.

## Roadmap

- [x] Protótipo completo dos 5 passos, trilha, diário, dicas, ajuste de ritmo
- [ ] Uma semana de uso real pelo fundador (a métrica: apareceu 5 de 7?)
- [ ] Ajustar durações e textos a partir do uso (talvez 3 min seja o tamanho certo)
- [ ] Modo "antes de uma conversa importante": só respira + primeira frase ensaiada (90s)
- [ ] Mais textos e temas; temas enviados pelo próprio usuário
- [ ] Se vingar: PWA instalável (ícone na tela inicial, funciona offline)
