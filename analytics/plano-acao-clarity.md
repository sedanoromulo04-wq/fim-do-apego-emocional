# Plano de Ação — Fim do Apego Emocional
### Diagnóstico comportamental + correções priorizadas, ancorado nos dados da Clarity

**Base:** 369 sessões reais (3 dias), 97% mobile, 78% abrindo dentro do app do Instagram/Facebook no Android.
**Método:** cruzamento do comportamento medido (Clarity) com a estrutura real da página (mapeamento de scroll do HTML renderizado a 720px de viewport).

---

## PARTE 1 — O diagnóstico que muda tudo

Um número isolado não diz nada. Dois números cruzados dizem o problema inteiro:

| Fato medido | Fonte |
|---|---|
| Scroll médio morre em **37%** | Clarity `ScrollDepth` |
| A página tem **13.042px = 18 telas** de rolagem no celular | HTML renderizado |
| O **primeiro preço aparece só aos 77%** da página | Mapeamento de seções |
| Os **bônus aparecem aos 59%** | Mapeamento de seções |

**Conclusão dura: o visitante médio abandona a página 40 pontos percentuais antes de ver qualquer preço, e 22 pontos antes de ver os bônus.**

A oferta não está sendo rejeitada. Ela nunca está sendo vista. Você não tem um problema de oferta — tem um problema de arquitetura. Está pedindo que alguém role 18 telas para descobrir quanto custa, e a pessoa desiste na tela 7.

### Onde exatamente a atenção morre

O scroll de 37% cai **no meio da seção "Os 4 Passos"** (que começa em 46% e é precedida por 5 blocos de dor entre 15% e 46%). O trajeto do abandono é:

```
0%    HERO (vídeo + promessa)          ← todos veem
5%    Depoimentos                       ← ainda leem
15%   DOR — 5 blocos, um a um           ← começa a arrastar
37%   ▓▓▓ ABANDONO MÉDIO ▓▓▓            ← desiste no meio da dor / início dos passos
46%   4 Passos
59%   Bônus                             ← minoria vê
77%   PREÇO                             ← quase ninguém vê
100%  Garantia, caminhos, CTA final
```

A seção de dor tem **cinco blocos verticais empilhados**, cada um com título + parágrafo + imagem grande. Isso é muito peso emocional negativo em sequência, sem alívio e sem avanço. A pessoa sente a dor, não vê a saída chegando, e sai. É o ponto de sangria.

---

## PARTE 2 — Leitura psicológica e comportamental

### 2.1 O estado mental de quem chega
78% vêm de anúncio pago no Instagram/Facebook, abrindo **dentro do app** (in-app browser), no Android, no celular. Isso define o comportamento:

- **Atenção de rolagem infinita.** Ela veio de um feed onde o polegar desce sem parar. A página herda esse ritmo: se não avança rápido, o polegar continua o movimento que já estava fazendo — para fora.
- **Baixa intenção inicial.** Não procurou por você. Foi interrompida por um anúncio. A intenção de compra ainda não existe — precisa ser construída na página, rápido, antes que o impulso do anúncio esfrie.
- **Contexto emocional cru.** O público-alvo é mulher em sofrimento de relacionamento. Ela não está num estado analítico; está num estado de dor. Cinco blocos seguidos reforçando essa dor sem entregar alívio a fazem **fechar para se proteger**, não para comprar.

### 2.2 O que o tempo ativo revela
Tempo ativo de **61s** contra 132s de tempo total. Ela deixa a aba aberta mas só interage metade do tempo. Combinado com scroll de 37%: ela lê o topo com atenção real, depois **desengaja gradualmente** — não é um abandono brusco (isso seria quickback, que é só 1,8%). É desistência por fadiga. A página cansa antes de convencer.

### 2.3 A assimetria dor/solução
A estrutura atual dedica **31% da página inteira (de 15% a 46%) só a aprofundar a dor**, e empurra a solução, os bônus e o preço para depois. Psicologicamente isso inverte a curva: prolonga o desconforto e adia o alívio. Quem sente dor quer saber rápido *como sai dela e quanto custa*. A página faz o oposto.

### 2.4 Facebook engaja o dobro do Instagram — e isso é um sinal
- Instagram: 161 sessões, 46s ativo
- Facebook: 149 sessões, **81s ativo**

Volume quase igual, engajamento quase o dobro no FB. O público do Facebook tende a ser mais velho e a ter mais paciência de leitura de página longa. O do Instagram é mais jovem e mais impaciente. Isso não é sobre a página — é sobre **para quem o anúncio está sendo entregue**. Sugere realocar verba para o público que a página consegue segurar.

---

## PARTE 3 — Plano de ação priorizado

Ordenado por **impacto ÷ esforço**. Faça de cima para baixo.

### 🔴 P0 — Levar a oferta para antes da zona de morte (o de maior impacto)
**Problema:** preço aos 77%, abandono aos 37%.
**Ação:** inserir um **primeiro CTA + preço logo após o hero e a primeira prova social** (por volta dos 10–15% da página). Não precisa ser a caixa de oferta completa — basta um bloco curto: promessa + preço à vista + botão. Quem já está pronto compra ali; quem não está continua lendo. Hoje você não dá a opção de comprar cedo para ninguém.
**Por quê funciona:** captura a intenção no pico — logo depois do anúncio, quando o impulso está mais quente. Não force todos a percorrer 18 telas.
**Esforço:** baixo (é reordenar/duplicar um bloco que já existe).

### 🔴 P0 — Encurtar e reequilibrar a seção de dor
**Problema:** 5 blocos de dor empilhados = ponto de sangria em 37%.
**Ação:** cortar de 5 para **2 ou 3 blocos de dor mais fortes**, e intercalar a virada ("existe um caminho") mais cedo. A dor tem que ser reconhecível, não exaustiva. O objetivo é ela pensar "é exatamente isso que eu sinto" e já querer a saída — não afundar.
**Esforço:** baixo (remover HTML).

### 🟠 P1 — Cortar a página pela metade
**Problema:** 18 telas de rolagem. Ninguém termina.
**Ação:** meta de reduzir para **~8–10 telas**. Candidatos a corte ou compressão: "2 Caminhos" (85%), parte da recap (73%), e fundir "Para quem" + "Autora". Cada seção depois dos 40% está sendo vista por uma minoria — o custo de mantê-las é o cansaço que derruba o scroll de todo mundo.
**Esforço:** médio.

### 🟠 P1 — Garantir que a oferta apareça sem rolar até o fim (sticky)
**Problema:** o único caminho para o preço é rolar 77% da página.
**Ação:** já existe um `#sticky-cta`. Garantir que ele **apareça cedo** (depois do hero, não só perto do fim) e que o botão leve direto ao checkout. Assim o preço/compra está sempre a um toque, independente de onde ela parou.
**Esforço:** baixo (ajuste do gatilho de exibição do sticky que já está no código).

### 🟡 P2 — Investigar os erros de JS no Android
**Problema:** Android tem **4,58% de erro de script** vs 0,89% no iOS. E Android é 68% do tráfego.
**Ação:** assistir 5 gravações de sessão da Clarity filtradas por `ScriptErrorCount` em Android. Confirmar se algum erro trava o botão de compra dentro do in-app browser do Instagram/Facebook. Se travar, é conversão perdida por bug, não por copy.
**Esforço:** baixo (investigação); correção depende do que achar.

### 🟡 P2 — Testar o checkout dentro do app do Instagram no Android
**Problema:** 78% do público compra (ou tentaria) dentro do in-app browser, o ambiente mais problemático para gateways de pagamento.
**Ação:** abrir o anúncio pelo próprio app do Instagram num Android e ir até o final da compra. Não testar pelo Chrome do desktop — não é onde seu público está.
**Esforço:** baixo (teste manual).

### 🟢 P3 — Realocar verba de mídia por engajamento de página
**Problema:** Audience Network (61 sessões) tem o pior scroll (32%); Instagram engaja menos que Facebook.
**Ação:** no Meta Ads, **isolar/cortar Audience Network** e testar mais verba no público de Facebook feed, que a página segura melhor (81s ativo). Decisão do gestor de tráfego — os dados só apontam a direção.
**Esforço:** externo (fora da página).

---

## PARTE 4 — Como medir se funcionou

Depois de aplicar P0 e P1, reextrair a Clarity (mesmo endpoint) e comparar:

| Indicador | Hoje | Meta |
|---|---:|---:|
| Scroll médio | 37% | > 55% |
| Tempo ativo/sessão | 61s | > 90s |
| % que chega ao preço | ~mínima (preço aos 77%) | maioria (preço movido p/ ~15%) |

O sinal de sucesso não é "scroll subiu" — é **scroll subiu E a página ficou mais curta**. Se você encurta a página, 55% de scroll passa a significar muito mais gente vendo a oferta do que 55% na página atual.

> Ordem sugerida de execução: **P0 (oferta cedo + dor enxuta) → medir 3 dias → P1 (encurtar + sticky) → medir → P2/P3.**
> Um passo de cada vez, para saber o que moveu o número.

---

*Dados brutos em `analytics/clarity-raw/`. Relatório de métricas em `analytics/relatorio-clarity.md`.*
