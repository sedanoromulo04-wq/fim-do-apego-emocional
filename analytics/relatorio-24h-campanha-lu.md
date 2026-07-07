# Fim do Apego Emocional — Relatório de 24h para a Lu
### Comportamento na página (Clarity) + desempenho da campanha (Meta Ads) + diagnóstico do checkout

**Data:** 2026-07-03
**Para:** Lucimar Freire (especialista/designer do funil)
**Objetivo deste documento:** mostrar com números o que está acontecendo na campanha, o que já foi corrigido, e por que a próxima correção (o checkout) é a prioridade.

---

## 1. O que a campanha do Meta Ads mostra (últimos 30 dias, 3 jun–2 jul)

| Conjunto | Finalizações de compra iniciadas | Valor gasto | Custo por resultado |
|---|---:|---:|---:|
| **Conjunto 3** | **48** | R$ 132,07 | **R$ 2,75** |
| Conjunto 1 | 2 | R$ 10,85 | R$ 5,43 |
| Conjunto 2 | 2 | R$ 4,32 | R$ 2,16 |
| Conjunto 4 | 0 | R$ 5,71 | — |
| Conjunto 5 | 0 | R$ 10,45 | — |
| **Total campanha** | **52** | **R$ 163,40** | **R$ 3,14** |

**O Conjunto 3 é o vencedor claro.** Não só pelo custo baixo — os Conjuntos 1 e 2 têm só 2 resultados cada, amostra pequena demais pra confiar no número. O Conjunto 3 é o único que provou em volume: 48 pessoas clicaram em comprar, gastando R$ 132 pra chegar lá. Os Conjuntos 4 e 5 gastaram dinheiro e não geraram nenhuma finalização de compra — candidatos a pausar ou reformular criativo.

**Ponto crítico: "finalização de compra iniciada" não é venda.** É o evento de quando a pessoa clica no botão de comprar na landing. Das 52 finalizações iniciadas em 30 dias, **zero viraram venda confirmada.** É esse o problema que motivou toda a investigação de hoje.

---

## 2. Como as pessoas se comportam na página (Microsoft Clarity, últimas 24h)

| Métrica | Valor |
|---|---:|
| Sessões reais | 338 (341 - 3 bots) |
| **Scroll médio** | **37,8%** |
| Tempo ativo médio | 62s |
| Mobile | 98% |
| Abrindo dentro do app Instagram/Facebook | 77% (261 de 338) |

**Leitura simples:** a maioria das pessoas lê só um terço da página e sai. Isso já vinha acontecendo há semana(s) — é o motivo da mudança que fizemos hoje na landing (ver seção 3).

Praticamente todo mundo (98%) acessa pelo celular, e a maior parte (77%) abre a página **dentro do próprio app** do Instagram ou Facebook, não no navegador normal do celular. Isso importa porque esse ambiente é mais restrito — é por isso que testamos o link de compra também dentro do app, e não só no navegador comum.

---

## 3. O que já foi corrigido hoje na landing page

Antes de mexer em qualquer coisa, temos o diagnóstico: com scroll médio de 37%, o preço só aparecia depois de **77% da página** — ou seja, quase ninguém rolava o suficiente pra ver quanto custava.

**Ação tomada:** movemos um bloco de preço + botão de compra para logo depois da primeira parte de identificação com a dor, por volta de **33% da página** (bem dentro da faixa que as pessoas realmente leem). Também reduzimos a parte de "dor" de 5 blocos para 2, pra não cansar antes da pessoa ver a oferta.

**Isso ainda não aparece nos números acima** porque a mudança é de hoje e a Clarity mistura o período de antes e depois numa métrica só. Vamos medir de novo em alguns dias, isolando só o período depois da mudança, pra confirmar se o scroll melhorou.

---

## 4. O achado de hoje: o checkout funciona, mas está "sujo" e destoa da landing

Passamos pelo caminho inteiro como uma cliente real faria: clique no anúncio → landing → botão de compra → checkout na Cakto → preenchimento → PIX. Resultado:

- **O checkout funciona tecnicamente.** PIX gera QR Code normal, cartão de crédito aceita os dados, nenhum travamento, nenhum erro. Confirmamos inclusive testando de dentro do app do Instagram no celular — sem problema técnico ali.
- **O problema é visual e de confiança no momento da decisão.** A página do checkout tem uma arte com várias provas sociais amontoadas, destoando do visual limpo e editorial que a landing tem hoje. Quem acabou de ler uma página cuidada, chega no checkout e vê algo "sujo" — isso gera hesitação bem na hora que a pessoa estava prestes a pagar.

**Ação em andamento:** já foi solicitado à especialista (você) o ajuste do checkout, deixando **uma imagem limpa**, sem empilhar provas sociais ali, mantendo a identidade visual que a landing já tem.

---

## 5. Resumo para decisão

| O que já sabemos | O que estamos fazendo |
|---|---|
| Conjunto 3 é o vencedor, com folga | Vamos usá-lo como base para testar o quiz de qualificação |
| Scroll médio baixo (37%) | Oferta antecipada + dor reduzida já implementadas hoje |
| Checkout tecnicamente ok | — |
| Checkout visualmente destoante da landing | Ajuste de design em andamento com a Lu |
| Zero vendas em 52 finalizações de compra | Hipótese principal: a quebra visual no checkout — vamos medir depois do ajuste |

**Próxima medição:** reextrair Clarity e conferir vendas reais na Cakto 2-3 dias depois do checkout ajustado, pra confirmar se o problema era esse.

---

*Dados brutos da Clarity em `analytics/clarity-raw/`. Este relatório complementa `relatorio-clarity.md` e `plano-acao-clarity.md`, já entregues anteriormente.*
