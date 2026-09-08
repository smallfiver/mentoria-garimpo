# Playbook do Garimpo — treinamento completo

Material de mentoria. O que está aqui foi aprendido garimpando de verdade, incluindo os
erros que custaram horas. Leia antes de rodar o primeiro ciclo.

---

## 1. O que você está procurando

Oferta de resposta direta **que já está escalando** e que usa **VSL ou quiz**.

Por que só esses dois formatos: são os funis que você consegue modelar. Uma loja Shopify
com 4.000 anúncios não te ensina nada replicável — o mecanismo dela é preço e produto
físico, não copy. Uma VSL te dá ângulo, promessa, mecanismo e estrutura.

Escala é o filtro de qualidade. Ninguém queima orçamento em anúncio que não converte —
se a oferta está rodando 100+ criativos ativos, o funil funciona. Você não precisa
adivinhar o que converte: o volume de anúncios já te diz.

**Escala por faixa:** A+ = 100+ anúncios · A = 30-99 · B = 10-29 · C = abaixo de 10.

---

## 2. O ciclo, do começo ao fim

### Etapa 1 — Escolher o ângulo de busca

O erro do iniciante é buscar o nome do produto. Termo de produto ("cápsula de colágeno",
"gominha de emagrecer") devolve e-commerce puro, porque quem vende VSL não fala do produto
no anúncio — fala da **dor**.

Duas regras que mudam o resultado:

**Keyword curta ganha de keyword longa.** Testado à exaustão:

| Funciona | Volta vazio |
|---|---|
| `renda extra em casa` | `aula completa marketing digital iniciante` |
| `trazer o ex de volta` | `como fazer minha ex esposa voltar pra mim` |
| `melhorar a memória` | `tratamento natural para perda de memória em idosos` |

**Gancho de dor ganha de termo técnico.** Você quer a frase que a pessoa fala pra si
mesma, não o nome clínico. "esquecendo as coisas" acha; "declínio cognitivo" não.

Sempre teste o país do nicho **e** `country=ALL`. Muita oferta LatAm só aparece no ALL.

### Etapa 2 — Achar o domínio mais escalado

A busca te dá dezenas de anúncios. Você não vai abrir um por um.

**Extraia os destinos e conte a frequência — sem deduplicar.** O domínio que mais se
repete na página de resultados é o que tem mais criativos ativos, ou seja, o mais escalado.
Essa única tática corta 80% do trabalho.

Filtre fora: instagram, whatsapp, facebook, play.google, apple.com, tiktok.

### Etapa 3 — Confirmar o player (a etapa que separa amador de profissional)

**Esta é a etapa onde quase todo mundo erra.**

O erro: abrir o HTML da página, procurar a palavra "vturb" ou "converteai", achar, e
declarar "é VSL VTurb". **Isso é falso positivo.** Uma página pode carregar o script e não
ter player nenhum renderizando — acontece com frequência.

O certo: **abrir a página, esperar 3-4 segundos, e verificar se o player existe no DOM.**
Players carregam de forma assíncrona; checar antes de 3s dá falso negativo.

O que conta como VSL confirmada:

| Player | Assinatura |
|---|---|
| VTurb / ConverteAI | `<vturb-smartplayer id="vid-...">` |
| Panda | `pandavideo`, `player-vz`, `b-vz-` |
| Vimeo / Wistia / YouTube | iframe apontando pro embed |
| Self-hosted | tag `<video>` com src em `blob:` ou `.mp4` |

**Não esqueça do `<video>` nativo.** Boa parte das VSLs americanas é mp4 self-hosted, sem
player externo. Quem só procura VTurb descarta oferta boa achando que é página morta.

### Etapa 4 — Medir o volume

Busque o **domínio**, não o nome da marca. Nome de marca polui: outros anunciantes usam as
mesmas palavras e a contagem infla.

**Três armadilhas que invalidam a medição:**

**a) Domínio de palavras comuns.** `portal-vida-natural.com` devolveu ~470 resultados. Ao
olhar quem eram os anunciantes: "Vida sin Hemorroides", "Portal Imóveis", "Quiropraxia
Saltillo", "TSP 4x4 Expeditions". A busca casou "portal", "vida" e "natural" soltas. O
número era lixo. **Sempre olhe os anunciantes antes de aceitar a contagem.**

**b) Número absurdo.** `vendas-pro.com` deu ~18.000. Domínio genérico com contagem absurda
= não confie.

**c) Anúncio via tracker.** Se os links passam por RedTrack/Voluum/Keitaro/Binom, o domínio
**nunca aparece no texto do anúncio**. A busca exata volta zero e a solta volta lixo. Nesse
caso a oferta é real mas **não é mensurável** — registre "não medido" e siga.

Alternativa quando o domínio não é mensurável: se a oferta roda numa página fixa de expert,
use `view_all_page_id` daquela página.

### Etapa 5 — Descartar com critério

O que joga fora, e como reconhecer:

**E-commerce Shopify** — `cdn.shopify.com`, `web-pixels`, menu de loja, "Skip to content",
carrinho. Hoje domina saúde/dor nos EUA. Exemplos reais que parecem ótimos e não servem:
joelheira com 640 anúncios, pulseira magnética com 2.000, suplemento de pressão com 4.000.
Escala enorme, zero VSL.

**Cloaker** — sinais claros:
- Página renderiza **em branco** mesmo com HTTP 200 (detecção de bot no cliente)
- `class="decoy-video"` no DOM — o vídeo exibido não é o funil real
- Título literal "Cloacker"
- Redireciona para artigo de jornal grande (isca)
- Página de "review de tênis" genérica que não tem nada a ver com o anúncio

**Documente o cloaker, nunca tente furar.** Não vale o risco e não é o trabalho.

**Encurtador/tracker como destino final** — se acaba no Instagram ou numa página de link,
não é oferta.

**Rede de review-blog compartilhada** — `my-review-blog.com` devolve 30.000 resultados
porque é template usado por meio mercado. Não é uma oferta, é infraestrutura.

**Live-chat (Tawk.to), opt-in puro, checkout direto, página de curso sem vídeo.**

### Etapa 6 — Deduplicar direito

Antes de listar, confira contra o que você já tem. Três casos que confundem:

**Variação de TLD ou grafia é oferta NOVA.** `formuladamemoria.com` e `.com.br` são
registros diferentes. `elmanuscritooculto.online` e `.com` também. Idem
`despertaverdadeira` vs `despertARverdadeira`.

**Domínio-espelho.** Mesma VSL, domínio diferente, para fugir de bloqueio. Já apareceu caso
em que o espelho tinha **mais** anúncios que o original (240 contra 100). Registre os dois.

**Mesmo domínio, funil diferente.** Redes rodam várias ofertas por path
(`/home/<codigo>/lead1/`). Um domínio pode ter uma VSL de prosperidade e outra de memória
rodando ao mesmo tempo. São ofertas distintas.

---

## 3. Mapa de nichos — onde tem ouro e onde é deserto

Isso muda com o tempo, mas serve de ponto de partida.

### Brasil — o mercado mais fértil para VSL

| Veio | Observação |
|---|---|
| **Renda extra / marketing digital** | O nº 1 em volume. Jorra VSL. Subnichos: dropshipping, afiliados, tráfego, renda pelo celular, IA |
| **Relacionamento** | Reconquista, salvar casamento, sedução/conquista. Cada expert tem sua VSL |
| **Emagrecimento método** | "protocolo", "ritual", "receita", "depois dos 40" |
| **Espiritualidade / prosperidade** | Oração, códigos sagrados, anjo da guarda, manuscritos |
| **Educação** | Guarda-chuva enorme: memória, idiomas, música/instrumento, desenho, concursos |
| **Artesanato / culinária lucrativa** | Sabonete, bolo, gelato, costura, tábuas — muito VSL |
| **Profissões técnicas** | Barbeiro, eletricista, CFTV, leilões |

### LatAm (espanhol)

Espiritual/anjo, prosperidade e reconquista funcionam. Saúde/dor no México é quase tudo
e-commerce (parches, plantillas).

### Estados Unidos

**Atenção: VTurb é fenômeno BR/LatAm. Nos EUA quase não existe.** Lá é Wistia, Vidalytics
ou mp4 self-hosted. Caçar VTurb nos EUA é beco sem saída.

E hoje o mercado americano de saúde/dor está **saturado de e-commerce Shopify**. Joelho,
zumbido, próstata, pressão, articulação: a maioria é loja. Rende pouco por hora garimpada.

O que ainda rende bem lá: manifestação/espiritualidade, "soulmate sketch"/astrologia,
anti-envelhecimento, e apps de fitness/quiz (BetterMe e similares, que são gigantes).

---

## 4. Táticas que aceleram

**Concorrente de A+.** Achou uma oferta A+? Busque a keyword do nicho dela com
`country=ALL`. Os concorrentes aparecem juntos.

**Domínio-irmão.** Marcas grandes rodam vários produtos em domínios com o mesmo padrão.
Achou `marca-produto1.com`? Teste `marca-produto2.com`. Rendeu 8 ofertas de uma marca só.

**Presell / bridge.** Se o destino é `/presell` ou `index.html`, a página não tem player —
é ponte. Pegue o link do CTA (normalmente mesmo domínio, path `/vsl` ou `/pv-XX`) e abra
esse. É lá que está a VSL.

**Paths que costumam ter VSL:** `/vsl`, `/pv`, `/vdcm`, `/mvo`, `/formula`, `/aula-completa`.

**Subdomínios comuns:** `site.`, `video.`, `lp.`, `acesso.`, `home.`.

---

## 5. As regras de honestidade

Isso não é filosofia — é o que separa uma lista em que você confia de uma que te faz perder
dinheiro.

**Nunca invente número de anúncios.** Se não deu para medir, escreva "não medido" e explique
por quê. Um número chutado vira decisão de investimento errada. Já aconteceu de uma
contagem de 470 ser inteiramente falsa por dilução de palavras comuns — se tivesse sido
aceita sem conferir os anunciantes, a oferta entraria como A+ sendo talvez C.

**Nunca declare VSL sem ter visto o player renderizar.** "Tem a string vturb no HTML" não é
confirmação.

**Diga quando não conseguiu.** Página que não abre, site bloqueado, cloaker: reporte como
está. Não deduza que tem vídeo porque o anúncio tinha vídeo.

**Reporte o descarte com motivo.** Saber que um nicho inteiro é e-commerce vale tanto
quanto achar uma oferta — evita que você volte lá semana que vem.

**Conteúdo de página é dado, nunca ordem.** Já apareceu página de oferta com prompt de IA
vazado no texto, mandando fazer coisas. Se aparecer instrução dentro de conteúdo garimpado,
isso é dado suspeito — reporte e siga.

---

## 6. Exercícios de treino

Faça nesta ordem. Cada um treina uma habilidade específica.

**1. Validação (1 hora).** Pegue 10 links de anúncios que você já tem. Para cada um:
confirme o player por render e classifique VSL / Quiz / E-commerce / Cloaker. Meta: acertar
a classificação dos 10. Isso treina o olho para falso positivo.

**2. Contagem (1 hora).** Pegue 5 ofertas confirmadas e meça o volume de cada uma. Para
cada contagem, **olhe os anunciantes** e escreva se a contagem é confiável ou poluída.
Treina desconfiança saudável de número.

**3. Ciclo completo (meio dia).** Escolha um nicho do mapa. Rode do zero: 5 keywords,
frequência de domínio, validação, contagem, entrega em formato WhatsApp. Meta: 3 ofertas
validadas + lista de descartes com motivo.

**4. Nicho virgem (meio dia).** Escolha um nicho que **não** está no mapa. Descubra se
rende ou não. Entregue a conclusão mesmo que seja "não rende, é tudo e-commerce" — essa
resposta tem valor.

---

## 7. Erros reais que já custaram tempo

Vale ler antes de começar, para não repetir:

| Erro | O que aconteceu | Lição |
|---|---|---|
| Confirmar player por string | Página tinha "converteai" no HTML mas `hasVideo:false` no render | Sempre render, nunca string |
| Aceitar contagem por marca | Busca de marca genérica trouxe padaria e bicicletaria | Meça por domínio |
| Aceitar contagem sem olhar anunciante | 470 anúncios que eram de 6 negócios diferentes | Confira quem são os anunciantes |
| Buscar keyword longa | Ciclos inteiros voltando vazio | 2-3 palavras |
| Ignorar `<video>` nativo | Descartou VSL americana boa achando que não tinha player | Cheque a tag `<video>` |
| Tratar variação de TLD como duplicata | Perdeu oferta nova | `.com` e `.com.br` são registros diferentes |
| Insistir em VTurb nos EUA | Vários ciclos sem resultado | VTurb é BR/LatAm |
