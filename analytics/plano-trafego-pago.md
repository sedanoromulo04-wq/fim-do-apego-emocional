# Fim do Apego Emocional — Plano de Tráfego Pago para Conversão
### Estudo das métricas do Meta Ads + estratégia de segmentação, orçamento e estrutura de campanha

**Data:** 2026-07-03
**Contexto corrigido:** a campanha rodou apenas **2 dias** (iniciada na madrugada de 02/07), com orçamento de **R$ 167,50/dia**. Os "82 finalizações de compra / R$ 285,21" que a interface do Meta mostrava eram de uma janela de exibição de 30 dias, não do tempo real de veiculação — a campanha em si é nova. O quiz já está rodando em teste no Conjunto 3 (cópia), com verificação de anunciante do Meta já liberada.

---

## 0. O fato que muda a ordem de prioridade — e a urgência real

Com 2 dias de campanha e ~R$ 335 investidos até agora, **zero vendas ainda não é um sinal definitivo de funil quebrado — é o esperado numa campanha nova em fase de aprendizado.** O Meta costuma levar de 3 a 7 dias (ou ~50 conversões do evento otimizado) para sair da fase de aprendizado e estabilizar. Julgar performance de venda com 2 dias de dados é cedo demais para decisões drásticas.

**Isso não invalida o achado do checkout** — ele foi confirmado na unha (testamos o fluxo completo, PIX gerando corretamente, mas a arte destoando da landing) e continua sendo uma correção válida e necessária. O que muda é a leitura da urgência: não é "30 dias sem vender, algo está grave", é "2 dias sem vender, dentro do esperado, mas com uma causa concreta já identificada e em correção".

A ordem de prioridade segue a mesma, mas com expectativa de tempo mais realista:

1. **Fechar o vazamento do checkout** (já em andamento — ajuste visual solicitado à Lu)
2. **Deixar a campanha completar a fase de aprendizado** (mínimo 3-4 dias corridos, ou ~50 conversões do evento otimizado) antes de julgar performance
3. **Confirmar a primeira venda real** dentro dessa janela
4. **Só depois** ajustar segmentação de forma definitiva e escalar orçamento

Com R$ 167,50/dia, você já está investindo em ritmo suficiente para gerar sinal rápido — o que falta é tempo de maturação da campanha, não mais verba.

---

## 1. Sobre cortar o público masculino — não é a prioridade que parece ser

### O dado, e por que ele engana

| Gênero | Resultados (finalização de compra) | Custo por resultado |
|---|---:|---:|
| Homens | 41 (50%) | R$ 3,35 |
| Mulheres | 39 (48%) | R$ 3,73 |

Isolado, esse número sugere que homens performam melhor. **É o oposto.** Você mesmo confirmou: a maioria dos homens que clicam não é público-alvo real (não é presente para parceira, é curiosidade/anúncio abrindo pra audiência ampla). Um clique de homem "custando menos" não é eficiência — é a métrica de topo de funil sendo inflada por gente que nunca teria intenção de comprar um produto que fala com "ele" na terceira pessoa, escrito da perspectiva de "você, mulher".

**Isso não aparece na métrica de custo por resultado porque "finalização de compra iniciada" é só o clique — não filtra por quem tem intenção real.** Com zero vendas fechadas nesses 2 dias, não dá pra saber ainda se as vendas que eventualmente vierem serão de homens ou mulheres — mas a lógica do produto (linguagem, dor, oferta) é 100% voltada pra mulher. Manter o público misto está diluindo a verba em gente que estruturalmente não converte no fim.

### Ação recomendada
**Sim, restrinja a segmentação para público feminino.** Não porque o custo por resultado dos homens seja ruim isoladamente, mas porque a taxa de conversão de clique→venda desse segmento tende a ser próxima de zero, dado que o produto não fala com eles. Isso é uma correção de eficiência de verba, não uma perda de volume que importa.

---

## 2. CBO ou ABO — qual estrutura usar

**Contexto rápido:**
- **CBO (Campaign Budget Optimization):** você define o orçamento na campanha, e o Meta distribui automaticamente entre os conjuntos, priorizando o que performa melhor em tempo real.
- **ABO (Ad Set Budget Optimization):** você define o orçamento manualmente em cada conjunto, controle total, mas exige mais gestão ativa.

### Diagnóstico do seu caso
Você tem hoje **5 conjuntos com performance extremamente desigual** (Conjunto 3 = 48-74 resultados; Conjuntos 4 e 5 = zero). Isso é justamente o cenário onde **CBO tende a ajudar**: ele identifica automaticamente que o Conjunto 3 performa e desloca verba pra lá, sem você precisar pausar manualmente os fracos.

**Porém**, há uma armadilha: como você ainda não tem vendas reais (só finalizações de compra), o algoritmo do CBO está otimizando para o evento errado — ele está otimizando para "clique no botão de comprar", não para "venda". Isso pode fazer o CBO alimentar ainda mais os conjuntos que geram clique barato mas não convertem (como o público masculino).

### Recomendação
1. **Agora, com o problema do checkout ainda não confirmado como resolvido:** mantenha **ABO** nos testes (Conjunto 3 original + Conjunto 3-quiz), com orçamento pequeno e igual nos dois, para comparar performance de forma limpa e controlada.
2. **Depois de confirmar que o checkout converte** (pelo menos 3-5 vendas reais): migre para **CBO**, mas troque o evento de otimização de "Iniciar Checkout" para **"Compra"** (Purchase) no Gerenciador de Anúncios — isso faz o algoritmo aprender a buscar quem *paga*, não quem só clica. Esse é o ajuste técnico mais importante depois do checkout: otimizar pelo evento certo.

---

## 3. Quanto investir

### O orçamento atual já é suficiente para gerar sinal — o que falta é tempo, não dinheiro
R$ 167,50/dia distribuídos entre 5 conjuntos já é um ritmo de teste robusto: em 2 dias isso gerou 82 finalizações de compra, volume mais que suficiente para começar a enxergar padrão. **Não aumente o orçamento agora.** Duas razões:

1. **A campanha ainda está na fase de aprendizado** (normal até o dia 3-7, ou ~50 conversões do evento otimizado). Aumentar orçamento nesse momento reinicia esse processo em vez de acelerá-lo.
2. **Ainda não existe taxa de conversão clique→venda conhecida.** Sem isso, não dá pra saber se R$ 167,50/dia é muito, pouco, ou adequado em relação ao que o produto realmente devolve em receita.

### O que fazer com o orçamento atual, nos próximos dias
1. Deixe a campanha rodar pelo menos até o **dia 4-5** no mesmo ritmo de investimento, sem mexer — interromper ou trocar configuração agora joga fora o aprendizado que o algoritmo já acumulou.
2. Em paralelo, **corrija o checkout** (a variável que pode estar zerando a conversão independente do tráfego).
3. Rode o **Conjunto 3 original** (landing direta) e o **Conjunto 3-quiz** (cópia) lado a lado, mesmo orçamento, mesmo criativo, para isolar se o quiz melhora a taxa de fechamento.
4. Se, depois do checkout corrigido e da fase de aprendizado completa (dia 5-7), ainda não houver nenhuma venda com esse volume de cliques — aí sim é sinal de que o problema é mais profundo que o checkout (pode ser preço, oferta, ou desconfiança residual), e vale revisitar a oferta em si.

### Por que não dá pra cravar um valor de escala agora
Nenhum estudo de tráfego pago (nem o meu, nem o de um gestor humano) consegue dizer "escale para X reais" sem primeiro saber o **ticket médio real de conversão** — quantas finalizações de compra geram 1 venda paga. Assim que a primeira venda acontecer, dá pra calcular: se, por exemplo, a cada 20 cliques 1 vira venda, e o produto custa R$ 67, você sabe exatamente quanto pode gastar por clique e ainda ter lucro. Até lá, qualquer número de escala seria chute.

---

## 4. O quiz — o que ele muda na estratégia

O quiz já está rodando em teste (Conjunto 3-quiz, 3 finalizações de compra por R$ 13,80 até agora — amostra pequena, cedo pra concluir).

**Por que ele importa mais do que parece:** o quiz naturalmente filtra por intenção antes mesmo de chegar na landing — quem responde 14 perguntas sobre o próprio relacionamento não é o homem clicando por curiosidade, é alguém genuinamente se reconhecendo na dor. Isso deve, em teoria, **melhorar a proporção de mulheres reais no funil sem precisar de segmentação agressiva por gênero**, porque o próprio formato já desqualifica quem não tem motivo pra continuar.

**Ação:** quando comparar Conjunto 3 (direto) vs. Conjunto 3-quiz, a métrica que decide não é custo por clique — é: **das pessoas que chegam na landing via quiz, quantas realmente compram**, comparado ao mesmo número vindo direto. Isso está rastreável no Supabase que já configuramos (funil por etapa) cruzado com vendas na Cakto.

**Criativos estáticos que você já tem prontos:** use-os no Conjunto 3-quiz e no Conjunto 3 original em paralelo, mesma imagem, mesmo público — assim a única variável que muda é "quiz ou direto", isolando o que realmente queremos medir.

---

## 5. Plano de ação, em ordem

| Ordem | Ação | Prazo estimado |
|---|---|---|
| 1 | Confirmar correção visual do checkout com a Lu | Já solicitado — priorizar conclusão em 24-48h |
| 2 | Trocar segmentação para público feminino nos conjuntos ativos | Pode fazer agora, não reseta aprendizado de forma grave |
| 3 | Deixar a campanha atual completar a fase de aprendizado (não mexer no orçamento) | Até dia 4-5 de veiculação |
| 4 | Rodar Conjunto 3 (direto) vs. Conjunto 3-quiz em paralelo, mesmo orçamento, mesmo criativo | Em paralelo ao passo 3 |
| 5 | Monitorar Cakto diariamente até a primeira venda real aparecer | A partir de agora |
| 6 | Se zero vendas persistir após checkout corrigido + fase de aprendizado completa (dia 5-7) | Reavaliar oferta/preço, não só tráfego |
| 7 | Assim que a 1ª venda confirmar, calcular taxa de conversão clique→venda | Assim que acontecer |
| 8 | Trocar evento de otimização do Meta de "Iniciar Checkout" para "Compra" | Depois do passo 7, com volume mínimo de compras |
| 9 | Migrar de ABO para CBO, com o evento de Compra como meta | Depois do passo 8 |
| 10 | Escalar orçamento em incrementos de 20-30% a cada 3-4 dias | Só no conjunto vencedor, depois do passo 9 |

---

## 6. O que este documento não substitui

Este é um estudo baseado nos dados que temos (Meta Ads, Clarity, Supabase). Ele não substitui:
- **Confirmação de vendas reais na Cakto** — sem isso, qualquer decisão de escala é aposta, não estratégia
- **Gravações de sessão da Clarity** (heatmap/recordings) — só existem no painel visual, ainda não assistidas
- **Feedback qualitativo de quem eventualmente comprar** — o motivo real da compra, quando existir, vale mais que qualquer inferência estatística
