# Relatório Microsoft Clarity — Fim do Apego Emocional

**Página:** https://fim-do-apego.vercel.app/
**Fonte:** Clarity Data Export API (`project-live-insights`)
**Janela:** últimos 3 dias (a API só devolve 1–3 dias por chamada)
**Extraído em:** 2026-07-03

> Nota de leitura: a Clarity mede **comportamento na página** (tráfego, scroll, tempo, cliques de fricção). Ela **não mede conversão/checkout**. Para vendas, cruzar com Kiwify/Meta Ads.

---

## 1. Números do topo (3 dias)

| Métrica | Valor |
|---|---|
| Sessões totais | **385** (16 bots → **369 reais**) |
| Usuários distintos | 384 |
| Páginas por sessão | 1,14 |
| **Scroll médio** | **37,1%** |
| Tempo total médio / sessão | 132 s |
| **Tempo ativo médio / sessão** | **61 s** |
| País | Brasil (≈100%) |

## 2. O achado principal: a página não segura o leitor

**Scroll médio de 37%.** Em média, a pessoa lê pouco mais de um terço da página e sai. Numa long page de oferta, o preço, os bônus e o CTA ficam **na metade de baixo** — ou seja, a maioria **nunca chega à oferta**.

**Tempo ativo de 61s** contra 132s de tempo total: a pessoa deixa a aba aberta, mas só interage metade do tempo. Combinado com scroll de 37%, o padrão é **bateu → leu o topo → saiu**.

O ponto de decisão está no topo. O hero e o primeiro bloco de dor precisam carregar todo o peso — se não fisgam ali, o resto da página não é visto.

## 3. De onde vem o tráfego (por parâmetro `utm_source`)

| Origem | Sessões | Scroll médio | Tempo ativo |
|---|---:|---:|---:|
| **Instagram (`ig`)** | 161 | 36,7% | 46 s |
| **Facebook (`fb`)** | 149 | 38,4% | **81 s** |
| **Audience Network (`an`)** | 61 | 32,0% | 57 s |

Leitura:
- **Instagram traz o maior volume**, mas engaja menos (46s ativo, scroll 37%).
- **Facebook traz volume quase igual e engaja quase o dobro** (81s ativo). Proporcionalmente, o público do FB lê mais a página.
- **Audience Network (61 sessões) é o pior dos três**: menor scroll (32%) e volume baixo. É o primeiro candidato a cortar/isolar no gerenciador de anúncios — costuma ser tráfego barato e frio.

## 4. Dispositivo e navegador

| Dispositivo | Sessões |
|---|---:|
| **Mobile** | 374 (97%) |
| PC | 11 (3%) |

| Sistema | Sessões |
|---|---:|
| Android | 262 (68%) |
| iOS | 112 (29%) |

| Navegador (onde a página abre) | Sessões |
|---|---:|
| **App do Instagram (in-app)** | 160 |
| **App do Facebook (in-app)** | 140 |
| Chrome Mobile | 70 |

**Implicação prática:** ~78% do tráfego abre a página **dentro do navegador embutido do Instagram/Facebook** (in-app browser), quase todo em Android. Esse ambiente é mais lento e restrito. Duas consequências:
1. Otimização de mobile e peso da página não é detalhe — é o caso principal.
2. O checkout precisa funcionar liso dentro do in-app browser (alguns gateways brigam com ele). Vale testar o fluxo de compra abrindo pelo app do Instagram no Android, não pelo Chrome do desktop.

## 5. Fricção técnica (sinais de erro)

| Sinal | % das sessões | Ocorrências |
|---|---:|---:|
| Erros de script (JS) | 3,4% | 23 |
| Quickback click (clicou, voltou na hora) | 1,8% | 7 |
| Rage click | 0% | 0 |
| Dead click | 0% | 0 |

Nada crítico. Zero rage/dead click é bom sinal — a página não tem botão quebrado óbvio. Os 3,4% de erro de JS valem uma olhada nas gravações de sessão que apresentam `ScriptErrorCount`, mas não é o gargalo. **O gargalo é atenção, não bug.**

---

## 6. O que os dados sugerem fazer

1. **Concentrar a decisão no topo.** Com scroll de 37%, tudo que importa (promessa, primeira prova, primeiro gancho de oferta) tem que estar acima da dobra ou logo abaixo. Considerar um CTA/preço mais cedo na página, não só no fim.
2. **Testar cortar a Audience Network** no Meta Ads. É o pior canal em scroll e volume. Realocar verba para Facebook feed, que engaja mais.
3. **Validar o checkout dentro do in-app browser do Instagram/Facebook no Android** — é onde 78% do público está. Se o checkout tropeça ali, a página pode estar convertendo menos por um problema fora dela.
4. **Assistir 5–10 gravações de sessão** filtradas por quem saiu antes de 40% de scroll — a Clarity grava vídeo do que a pessoa fez. É onde o "porquê" do abandono aparece.

---

## Anexos
Dados brutos (JSON) em `analytics/clarity-raw/`:
- `clarity-3d.json` — visão geral 3 dias
- `clarity-3d-source.json` — quebra por origem de tráfego
- `clarity-3d-os.json`, `clarity-3d-device.json`, `clarity-3d-multi.json`

**Como reextrair:** `GET https://www.clarity.ms/export-data/api/v1/project-live-insights?numOfDays=3` com header `Authorization: Bearer <token>`. Parâmetros: `numOfDays` (1–3), `dimension1..3` (OS, Browser, Device, Country, Source, Channel, URL, ReferrerUrl). Limite: 10 chamadas/projeto/dia.
