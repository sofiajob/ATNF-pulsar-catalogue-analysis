# 📈 ATNF Pulsar Catalogue - Análise Estatística Exploratória

## Sobre o Projeto

### Análise estatística exploratória do catálogo de pulsares do Australia Telescope National Facility, investigando distribuições e relações entre propriedades físicas desses objetos para a disciplina de Estatística Aplicada I

### Principais Descobertas
- **4.351 pulsares** na versão 2.7.0 do catálogo
- **Duas subpopulações distintas**: pulsares normais (período ~0.5-5s) e millissegundos (~0.001-0.02s)
- Têndencia na correlação entre idade e período rotacional para pulsares normais
- Apenas **13.9%** dos pulsares possuem classificação por tipo catalogada
- **84.3%** não têm associação conhecida a objetos astronômicos

### 🔗 Acesse o código aqui: ___

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

## Discussão Breve dos Resultados

### Add imagens dos principais graficos 

- **Distribuição bimodal** do período de rotação → duas populações distintas: normais (0,5-5s) e millissegundos (<0,02s)
- **84%** dos pulsares não possuem associação conhecida
- **15,7%** possuem associação catalogada (GRS, GC, SNR, XRS)
- **Correlação fraca** entre período e idade (r = -0,027) devido à separação das populações

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

## Referências

>add link para o ATNF

>add artigo principal usado de ref pelo ATNF

>add aqueles outros dois artigos sobre pulsares
