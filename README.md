# 📈 ATNF Pulsar Catalogue - Análise Estatística Exploratória

**Autoria:** Sofia Job - UFSC  
**Disciplina:** Estatística Aplicada I

---

## 1. Visão Geral

Análise estatística exploratória do catálogo de pulsares do ATNF (Australia Telescope National Facility), investigando distribuições e relações entre propriedades físicas dessas estrelas de nêutrons para a disciplina de Estatística Aplicada I

---

## 2. Objetivos

- Descrever a distribuição das variáveis selecionadas
- Construir tabelas de frequência para variáveis de interesse
- Calcular medidas de resumo (média, mediana, desvio padrão, etc.)
- Visualizar relações entre variáveis duas a duas

---

## 3. Variáveis Selecionadas

| Tipo | Variável | Descrição |
|------|----------|-----------|
| Qualitativa | `TYPE` | Tipo de pulsar (normal, millisecond, AXP, etc.) |
| Qualitativa | `TEM_ASSOC` | Associação a remanescentes de supernova ou aglomerados |
| Quantitativa | `P0` | Período de rotação (segundos) |
| Quantitativa | `DM` | Medida de dispersão (pc/cm³) |
| Quantitativa | `AGE` | Idade característica (anos) |

**Fonte dos dados:** ATNF Pulsar Catalogue (acessado via biblioteca `psrqpy`) 
add link pra fonte 

---

## 4. Metodologia

- **Coleta:** Biblioteca `psrqpy` em Python
- **Ambiente:** Google Colab
- **Análise:** `pandas` para tabelas, `matplotlib`/`seaborn` para vizualizações
- **Tamanho da amostra:** 4.351 pulsares

---

## 5. Hipóteses Investigadas

### Hipótese 1 (P0 vs AGE)
Pulsares mais velhos têm períodos de rotação mais longos devido à perda de energia rotacional.

### Hipótese 2 (DM vs DIST)
Pulsares mais distantes apresentam maior medida de dispersão, pois o sinal atravessa mais matéria interestelar.

### Hipótese 3 (P0 vs DM)
Não há relação direta entre período de rotação e medida de dispersão, pois são determinados por fatores físicos distintos.

### Hipótese 4 (Millissegundos)
Pulsares millissegundo formam uma subpopulação distinta, com idades elevadas mas períodos muito curtos (objetos "reciclados").

---

## 6. Resultados Principais (transformar 6 e 7 em um unico tópico --> Resultados e Discussões)

### 6.1 Tabelas de Frequência
- `TEM_ASSOCIACAO`: coluna feita a partir da variavel `ASSOC`, onde os pulsares foram classificados de acordo com a presença ou não de associação com objeto astronomico catalogado. 'S' para os que possuem, 'N' caso contrario. 84,3% sem associação, 15,7% com associação
- `TYPE`: 86% não classificados, 7% HE, 2,8% RRAT, etc.

### 6.2 Medidas de Resumo 
(add print das tabelas)

### 6.3 Relações entre Variáveis
add graficos e explicação

- **P0 vs AGE:** Correlação global baixa (r = -0,027), mas gráfico revela duas populações distintas
- **P0 vs DM:** Correlação fraca positiva (r = 0,216)
- **Pulsares normais vs millissegundos:** Comportamentos opostos no diagrama P0-AGE

### 6.4 Vizualizar Notebook da EDA
---

## 7. Principais Insights

1. **Duas populações distintas:** Pulsares normais e millissegundos ocupam regiões diferentes do diagrama P0-AGE
2. **Millissegundos são "anômalos":** Muito velhos (10⁸-10¹⁰ anos) mas com períodos extremamente curtos (0,001-0,02s)
3. **Limitação da correlação de Pearson:** A correlação global baixa esconde uma estrutura bimodal importante
4. **Escala log é essencial:** A relação entre variáveis só é visível em escala logarítmica
5. > loading


## 8. Referências Bibliograficas

>add link para o ATNF

>add csv do df que usei (?)

>add artigo usado de ref pelo ATNF

>add aqueles outros dois artigos sobre pulsares
