# 📈 ATNF Pulsar Catalogue - Análise Estatística Exploratória

## Sobre o Projeto

### Análise estatística exploratória do catálogo de pulsares do Australia Telescope National Facility, investigando distribuições e relações entre propriedades físicas desses objetos para a disciplina de Estatística Aplicada I

## Principais Descobertas
- **4.351 pulsares** na versão 2.7.0 do catálogo
- **Duas subpopulações distintas**: pulsares normais (período ~0.5-5s) e millissegundos (~0.001-0.02s)
- Têndencia na correlação entre idade e período rotacional para pulsares normais
- Apenas **13.9%** dos pulsares possuem classificação por tipo catalogada
- **84.3%** não têm associação conhecida a objetos astronômicos

### 🔗 [Open in Colab - ATNF Pulsar Catalogue Análise e Vizualizações](notebooks/Cópia_de_estatistica_eda_extracao_dados.ipynb)

---

## Variáveis Selecionadas
  
| Variável | Descrição |
|------|-----------|
| `TYPE` | Classificação quanto ao tipo de pulsar (normal, millisecond, AXP, etc.) |
| `TEM_ASSOC` | Associação a remanescentes de supernova ou aglomerados catalogada |
| `P0` | Período de rotação (segundos) |
| `DM` | Medida de dispersão (quantidade de elétrons livres entre a Terra e o pulsar em pc/cm³) |
| `AGE` | Idade característica (anos) |

> Nota: `TEM_ASSOC` é derivada da váriavel original `ASSOC`, que foi simplificada para uma classificação binária (Sim/Não), indicando apenas se o pulsar possui qualquer tipo de registro de associação catalogado.

---

## Discussão das Principais Descobertas da Análise

### 1. Classificação e Associação dos Pulsares

💡 **Insight:** As categorias HE, RRAT e NRAD representam **93.8%** dos pulsares classificados. AXP e XINS são tipos raros ou de detecção recente.

| Associação | Frequência Absoluta | Frequência Relativa (%) |
|:----------:|:-------------------:|:-----------------------:|
| Com associação catalogada (S) | 683 | 15.7% |
| Sem associação conhecida (N) | 3.668 | 84.3% |
| **Total** | **4.351** | **100%** |

💡 **Insight:** A predominância de pulsares sem associação conhecida (84.3%) reflete o desafio de rastrear a origem desses objetos antigos, cujas evidências de formação frequentemente se dissipam.

---

### 2. Distribuição e Medidas de Resumo

| Variável | Média | Mediana | CV |
|:--------:|:-----:|:-------:|:---:|
| **P0** (período) | 0,85s | 0,37s | 220% |
| **DM** (dispersão) | 351 pc/cm³ | 163 pc/cm³ | 98% |
| **AGE** (idade) | ~2 bi anos | ~10 mi anos | 1570% |

💡 **Insight:** As variáveis apresentam distribuições assimétricas positivas (média > mediana), indicando maior diversidade comportamental entre os pulsares catalogados.

💡 **Insight:** em `AGE`, a enorme diferença entre média e mediana revela uma **forte assimetria à direita** (poucos pulsares extremamente velhos puxam a média para cima). O CV de 1570% confirma a alta heterogeneidade dos dados.

---

### 4. Distribuições Individuais

<img src="docs/Histograma_DM_AGE.png" width="600">

#### 📈 Medida de Dispersão (DM)
- **Maior concentração:** 100 – 1000 pc/cm³
- **Frequência decrescente** para valores mais altos
- **Viés observacional:** Pulsares com DM alto estão em regiões de alta densidade ou grandes distâncias, o que dificulta sua detecção

#### 📈 Idade Característica (AGE)
- **Pico principal:** 10⁶ – 10⁷ anos (1 a 10 milhões de anos)
- **Cauda à direita:** Estende-se até 10¹⁰ anos (pulsares muito velhos, rotação lenta)
- **Cauda à esquerda:** 10³ – 10⁵ anos (pulsares jovens, rotação rápida)

💡 **Insight:** A distribuição assimétrica da idade reforça a **existência de subpopulações** no catálogo.

---

### 5. Período de Rotação (P0) — Descoberta Principal

<img src="docs/Histograma_P0.png" width="400">
<center>Tabela 5: Populações identificadas no histograma de P0</center>

| População | Faixa de Período | Característica |
|:---------:|:----------------:|:--------------:|
| **Pulsares normais** | 0,5 – 5 segundos | Maioria da amostra, rotação lenta |
| **Millissegundos** | 0,001 – 0,02 segundos | Minoria, rotação extremamente rápida |

💡 **Insight:** Embora menos numerosos, os pulsares millissegundos evidenciam a existência de **duas populações com comportamentos rotacionais distintos**. A frequência decai progressivamente para períodos >5s, indicando que pulsares muito lentos são raros no catálogo.

---

### 6. Relação Período × Idade

<img src="docs/Dispercao_P0_AGE.png" width="400">
<center>Tabela 6: Comportamento das populações no gráfico P0 × AGE</center>

| População | Comportamento Observado |
|:---------:|:-----------------------:|
| **Pulsares normais** (P0 ≥ 0,02s) | Período **aumenta com a idade** — consistente com a perda gradual de energia rotacional |
| **Millissegundos** (P0 < 0,02s) | **Extremamente velhos (10⁸–10¹⁰ anos), mas muito rápidos (0,001–0,02s)** — comportamento anômalo |

💡 **Insight-chave:** A separação clara entre as duas populações confirma que **millissegundos evoluem de maneira completamente diferente** dos pulsares normais, consistente com a teoria de reaceleração por transferência de momento angular em sistemas binários (Lorimer, 2005).

---

## Tecnologias e Ferramentas Utilizadas

| Tecnologia | Finalidade |
|------------|-------------|
| Python | Linguagem principal |
| psrqpy | Interface para ATNF Pulsar Catalogue |
| pandas | Manipulação de dados |
| numpy | Computação numérica |
| matplotlib/seaborn | Visualizações |
| Google Colab | Ambiente de desenvolvimento em nuvem |

---

## Autoria 
Sofia Fernandes Job Junqueira

## Referências
> add psrqpy licença
>add link para o ATNF
>add artigo principal usado de ref pelo ATNF
