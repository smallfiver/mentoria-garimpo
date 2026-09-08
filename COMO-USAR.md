# Como usar — guia do dia a dia

Leia o PLAYBOOK uma vez para entender o método. Este aqui é o que você consulta enquanto
trabalha.

---

## Instalação (uma vez só)

Copie a pasta `garimpar-ofertas` para dentro de `.claude/skills/` do seu projeto:

```
<seu-projeto>/.claude/skills/garimpar-ofertas/SKILL.md
```

Feche e abra a sessão. Pronto — não precisa colar nada nunca mais.

**Teste se instalou certo:** digite `garimpa ofertas`. Se o Claude responder perguntando
nicho, país e quantidade, está funcionando.

---

## O básico: dois jeitos de começar

### Jeito 1 — deixa ele perguntar

Você digita:

```
garimpa ofertas
```

Ele responde perguntando as 4 coisas:

1. **Nicho** — emagrecimento, renda extra, relacionamento, espiritualidade...
2. **País** — BR, US, LatAm (ES)
3. **Quantas ofertas** nesta rodada
4. **Formato** — só VSL ou VSL + quiz

Você responde e ele trabalha. Use quando estiver explorando sem alvo definido.

### Jeito 2 — manda tudo de uma vez (mais rápido)

```
garimpa 10 ofertas de emagrecimento no BR, só VSL
```

Ele não pergunta nada e já começa. Use quando você já sabe o que quer — é o que você vai
usar 90% das vezes.

---

## Os 4 comandos que resolvem quase tudo

| O que você quer | O que digitar |
|---|---|
| **Garimpo normal** | `garimpa 10 ofertas de reconquista no BR` |
| **Validar um link** | `esse link é VSL real? <cole a url>` |
| **Achar concorrente de uma oferta boa** | `acha concorrentes dessa oferta: <url>` |
| **Testar se um nicho vale a pena** | `testa o nicho de zumbido nos EUA, vale a pena?` |

O de **validar link** é o mais subestimado. Sempre que alguém te mandar uma oferta, jogue
lá antes de perder tempo estudando — em 30 segundos você sabe se é VSL ou loja disfarçada.

---

## O que esperar de volta

Uma lista assim, por oferta:

```
*Código da Reconquista* — relacionamento/reconquista
Método de reconexão em 3 fases, ângulo "ele volta sozinho"
Formato: VSL (VTurb)
📊 ~260 anúncios
Oferta: https://cdr.exemplo.com
Biblioteca: https://facebook.com/ads/library/?...
```

E no fim: ranking por número de anúncios + lista do que foi descartado com o motivo.

**Leia a lista de descarte.** Ela vale quase tanto quanto a de achados: saber que um nicho
inteiro virou e-commerce te economiza voltar lá semana que vem.

---

## Como saber se ele está trabalhando direito

Confira estes três sinais. Se algum falhar, cobre.

**1. Ele abriu a página da oferta?** Se declarou "VSL VTurb" sem ter aberto o site, está
chutando. Pergunte: *"você confirmou o player abrindo a página ou só viu no HTML?"*

**2. Ele conferiu quem são os anunciantes na contagem?** Número alto em domínio de palavras
comuns costuma ser falso. Pergunte: *"os anunciantes que apareceram batem com essa oferta?"*

**3. Ele disse o que descartou?** Lista só com achados e sem descartes é suspeita — em
garimpo real a maioria dos candidatos cai fora.

---

## Quando ele disser "não consegui"

Isso é resposta boa, não desculpa. Três casos legítimos:

| Ele diz | Significa | O que fazer |
|---|---|---|
| **"não medido — anúncio via tracker"** | Os links passam por RedTrack/Voluum, o domínio não aparece no texto do anúncio. Impossível contar. | Aceite. A oferta pode ser ótima, só não dá para medir por aí. |
| **"página em branco / cloaker"** | O site detectou automação e devolveu página vazia. | Aceite e peça para documentar. **Nunca peça para furar cloaker.** |
| **"contagem poluída"** | O número existe mas é de outros anunciantes. | Aceite o "não confiável". Melhor sem número que com número errado. |

**Nunca peça para ele "estimar" ou "chutar" um número.** Número inventado vira decisão de
investimento errada — foi assim que um domínio de 470 anúncios se revelou ter quase nada.

---

## Erros que o iniciante comete

**Pedir keyword longa.** "acha ofertas de tratamento natural para perda de memória em
idosos" volta vazio. Peça o nicho, deixe ele escolher as palavras — a skill já sabe que
2-3 palavras funcionam melhor.

**Achar que escala grande = oferta boa.** Joelheira com 640 anúncios, pulseira magnética
com 2.000: é e-commerce Shopify. Escala enorme e zero VSL para modelar.

**Caçar VTurb nos EUA.** VTurb é fenômeno BR/LatAm. Nos EUA é Wistia, Vidalytics ou mp4
self-hosted. Pedir "acha VTurb nos EUA" é ciclo perdido.

**Descartar oferta boa por não ter player conhecido.** Se ele disser "tem tag `<video>`
nativa", isso **é** VSL — muita oferta americana é mp4 hospedado no próprio site.

**Insistir num nicho seco.** Se dois ciclos voltaram só e-commerce, o nicho está saturado.
Troque em vez de insistir.

---

## Ritmo de trabalho sugerido

- **Um ciclo = um nicho + um país.** Não misture, a busca fica confusa.
- **5 a 10 ofertas por ciclo.** Mais que isso a qualidade da validação cai.
- **Anote os descartes** numa aba separada. Em duas semanas você tem seu próprio mapa de
  onde tem ouro e onde é deserto.
- **Revisite os A+ a cada 15 dias.** Oferta que salta de 100 para 300 anúncios está
  escalando agora — é a hora de modelar.
