# 📈 ATNF Pulsar Catalogue - Análise Estatística Exploratória
### Análise estatística exploratória do catálogo de pulsares do Australia Telescope National Facility, investigando distribuições e relações entre propriedades físicas desses objetos para a disciplina de Estatística Aplicada I

## Visão Geral e Variáveis Selecionadas

- **4.351 pulsares** analisados
- **Objetivo:** Estudar a distribuição dos dados e relacionar as variaveis de interesse.

| Variável | Descrição |
|------|-----------|
| `TYPE` | Classificação quanto ao tipo de pulsar (normal, millisecond, AXP, etc.) |
| `TEM_ASSOC` | Associação a remanescentes de supernova ou aglomerados catalogada |
| `P0` | Período de rotação (segundos) |
| `DM` | Medida de dispersão (quantidade de elétrons livres entre a Terra e o pulsar em pc/cm³) |
| `AGE` | Idade característica (anos) |

> Nota: `TEM_ASSOC` foi derivada da coluna ASSOC -- explicar

---

## Principais Resultados

### Add imagens dos principais graficos 

- **Distribuição bimodal** do período de rotação → duas populações distintas: normais (0,5-5s) e millissegundos (<0,02s)
- **84%** dos pulsares não possuem associação conhecida
- **15,7%** possuem associação catalogada (GRS, GC, SNR, XRS)
- **Correlação fraca** entre período e idade (r = -0,027) devido à separação das populações

### Link para Google Colab: ___
---

## Tecnologias e Ferramentas Utilizadas

| Ferramenta | Finalidade |
|------------|------------|
| Google Colab | Ambiente de desenvolvimento em nuvem |
| Python | Linguagem de programação |
| psrqpy | Acesso ao catálogo ATNF (Pitkin, 2018) |
| pandas e numpy | Bibliotecas para processamento e análise dos dados |
| matplotlib e seaborn | Bibliotecas para visualizações gráficas |

---

## Referências

>add link para o ATNF

>add artigo principal usado de ref pelo ATNF

>add aqueles outros dois artigos sobre pulsares
