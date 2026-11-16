# 05 — Sistema de design do Vozi: as três direções

> **Para ver no celular:** `https://ronaldojr-art.github.io/voz/docs/design/`
> As mesmas telas, com três direções visuais. O controle no rodapé troca entre elas.

Este doc registra o raciocínio, as três propostas e o que falta decidir. Depois da escolha do fundador, ele vira a especificação completa (escala de letra, espaçamentos, estados dos componentes) e a direção escolhida é aplicada no app.

## O ponto de partida

**O assunto:** um sabiá-laranjeira que ouve. O app ensina a falar com calma: fôlego, pausa, clareza, estrutura.
**Quem usa:** adultos inseguros com a própria fala, no celular, cinco minutos por dia.
**O trabalho do visual:** fazer a pessoa se sentir acolhida o bastante para falar em voz alta. Calma, não performance.

## O que o visual de hoje tem de genérico

O app atual herdou o azul escuro e o dourado do jogo de pescaria. Funciona, mas não é do Vozi. Olhando com o critério da skill de design:

- **Fundo quase preto com um único destaque brilhante.** É um dos padrões mais comuns de interface gerada por IA.
- **Tudo em cartões iguais**, com o mesmo raio e a mesma borda, sem hierarquia entre o que é principal e o que é apoio.
- **Emojis no lugar de ícones**, que mudam de desenho em cada celular.
- **Letra do sistema**, sem personalidade própria.
- **Informações coladas com pontinhos** ("Dia 18 · Clareza · ~5 min") em vez de frases.

## A assinatura: o pé de laranja

A skill pede para gastar a ousadia em um lugar só. O lugar é a trilha.

O Vozi é um sabiá-**laranjeira**. Então a trilha de 30 dias vira um galho de laranjeira: cada dia por vir é uma flor, cada dia treinado amadurece uma laranja, e o Vozi fica pousado no dia de hoje. "17 laranjas maduras" diz mais do que "17 de 30", e nenhum outro app tem isso.

A assinatura vale para as três direções. O resto da interface fica quieto em volta dela.

## O que é igual nas três

- **O pé de laranja** como trilha.
- **Ícones de traço** no lugar dos emojis (biblioteca Lucide, licença livre).
- **Hierarquia:** o dia de hoje e o botão principal em destaque, sem cartão em volta de tudo.
- **Frases no lugar de rótulos:** "Clareza: articular sem correr." "Leva uns cinco minutos."
- **Laranja como cor da marca**, tirada do peito do sabiá.
- **Fontes servidas pelo próprio app**, sem depender de serviço externo, o que também prepara o uso sem internet.
- **Contraste de texto dentro da norma de acessibilidade** (nível AA) nas três paletas, conferido por cálculo.

## As três direções

### Manhã

O sabiá canta cedo. Céu claro, laranja madura e botões com relevo, que dá vontade de apertar. É a mais leve e a mais próxima de um jogo.

| Cor | Valor | Uso |
|---|---|---|
| Céu | `#DCEEF7` | Fundo, descendo para um verde bem claro |
| Tinta | `#12324A` | Texto |
| Laranja | `#F58220` | Ação principal e laranjas |
| Folha | `#26784A` | Feito, concluído |
| Gema | `#FFCB3D` | Destaques pequenos |
| Papel | `#FFFFFF` | Superfícies |

**Letra:** Gabarito, uma família só, desenhada para aplicativos de aprender.
**Forma:** cantos bem redondos, botões com borda inferior que afunda ao toque.
**Risco:** é a que mais lembra o Duolingo no jeito, embora não nas cores.

### Mata

A sombra da laranjeira. Verde fundo, títulos com serifa macia e muito respiro. É a mais calma e a mais adulta.

| Cor | Valor | Uso |
|---|---|---|
| Mata | `#103A2D` | Fundo |
| Creme | `#F5F0E1` | Texto |
| Laranja | `#F68B2C` | Ação principal e laranjas |
| Broto | `#A3DDAE` | Feito, concluído |
| Gema | `#FFD166` | Destaques pequenos |
| Sombra | `#184837` | Superfícies |

**Letra:** Fraunces nos títulos, Figtree no texto.
**Forma:** botões em cápsula, superfícies planas, sem sombra.
**Risco:** verde é a cor do Duolingo. O tom aqui é escuro e bem diferente, mas a associação pode aparecer.

### Noite

O Vozi de hoje, arrumado. Mesmo azul escuro e mesmo dourado, com letra própria, ícones de verdade e o pé de laranja.

| Cor | Valor | Uso |
|---|---|---|
| Noite | `#071722` | Fundo |
| Lua | `#EAF1F4` | Texto |
| Dourado | `#FFD84D` | Ação principal |
| Vaga-lume | `#7DF28C` | Feito, concluído |
| Laranja | `#F68B2C` | Laranjas da trilha |
| Azul fundo | `#0E2431` | Superfícies |

**Letra:** Bricolage Grotesque, uma família só, com um pouco de sotaque.
**Forma:** como hoje, com menos caixas.
**Risco:** é a menos distinta. Continua no padrão "fundo escuro com um destaque".

## Como escolher

Abra a página no celular, de dia e à noite, e troque entre as três. Duas perguntas ajudam:

1. Qual delas você abriria com vontade às sete da manhã e às onze da noite?
2. Em qual delas o sabiá parece mais em casa?

Dá para misturar: por exemplo, a Manhã como padrão e a Noite como modo escuro, com a mesma letra nas duas.

## Decisão

- [x] **DECIDIDO (fundador, 16/11/2026): Manhã como padrão e Noite como modo escuro**, com a mesma letra nas duas (Gabarito). A direção Mata fica arquivada na prévia.

### Como ficou no app

- **Manhã é o padrão**, mesmo em celular configurado no modo escuro. O botão de lua no topo troca para a Noite, e a escolha fica guardada.
- **Automático** é uma terceira opção, em "Como funciona", para quem quer que o Vozi siga o claro ou escuro do celular.
- **Laranja é a cor da ação na Manhã. Na Noite, a ação continua dourada**, e o laranja fica nas frutas do pé.

## Depois da escolha

- [x] Aplicado no app inteiro (16/11/2026): tela inicial com o pé de laranja, os cinco passos, a tela de fim, diário e "como funciona"
- [x] Todos os emojis trocados por ícones de traço, inclusive nas notas da reescuta e no diário
- [x] As cores vivem em um só lugar do código, como variáveis com nome (céu, tinta, ação, feito, pausa), uma lista para cada pele
- [x] Contraste de texto conferido por cálculo nas duas peles, foco de teclado visível, movimento reduzido respeitado
- [x] O app carrega só a Gabarito, de `assets/fonts/`. A prévia em `docs/design/` mantém as quatro fontes, como registro da escolha
- [ ] Especificação escrita dos componentes: estados, tamanhos e espaçamentos, para quando o app deixar de ser um arquivo só
- [ ] Revisão dos textos da interface, tela por tela
- [x] Movimento (16/11/2026): ao voltar de um dia de trilha, a flor cai, a laranja cresce passando de verde a laranja, e o Vozi pula para o galho seguinte. Toca uma vez só, dura cerca de dois segundos, e é o único movimento não pedido do app. Quem ativou "reduzir movimento" no celular vê o resultado direto, sem animação

## Créditos

Fontes Gabarito, Fraunces, Figtree e Bricolage Grotesque, todas sob a licença aberta SIL OFL. Ícones Lucide, licença ISC.
