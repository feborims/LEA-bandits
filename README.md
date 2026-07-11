# Trabalho LEA — Bandits

**Aluna:** Fernanda Borim  
**RA:** 770291

Este repositório reúne o código e o relatório do trabalho de LEA sobre **bandits e decisões sequenciais**.

## Objetivos

O trabalho é dividido em duas partes:

1. **Inferência após seleção:** avaliação da cobertura de intervalos de confiança após a escolha do braço com maior média amostral.
2. **Recompensa acumulada com dados de contagem:** comparação de políticas de bandits em um modelo Poisson para campanhas de divulgação.

## Políticas analisadas

- Alocação uniforme aleatória
- Greedy
- UCB
- Thompson Sampling
- Epsilon-greedy, na Parte 2

## Estrutura do repositório

```text
trabalho-lea-bandits/
├── README.md
├── requirements.txt
├── codigos/
│   └── codigos_bandits.ipynb
└── relatorio/
    └── relatorio_bandits.pdf
```

## Como executar o notebook

O código foi desenvolvido em **Python** e organizado em um notebook `.ipynb`, compatível com Google Colab e Jupyter Notebook.

### Google Colab

1. Abra o Google Colab.
2. Selecione **Arquivo > Fazer upload de notebook**.
3. Envie o arquivo `codigos/codigos_bandits.ipynb`.
4. Execute as células na ordem apresentada.

### Ambiente local

Instale as dependências:

```bash
pip install -r requirements.txt
```

Depois, abra o notebook com Jupyter Notebook ou JupyterLab.

## Configuração das simulações

Nos experimentos principais, foi utilizado horizonte `T = 500`.

- Parte 1: 5.000 repetições por política.
- Parte 2: 1.000 repetições por política.
- Semente global: `770291`.

O notebook contém as justificativas metodológicas, as simulações, as tabelas e os gráficos utilizados no relatório.

## Principais resultados

Na Parte 1, os intervalos usuais aplicados ao braço selecionado apresentaram cobertura inferior à nominal em várias políticas, evidenciando o efeito da seleção sobre a inferência.

Na Parte 2, Thompson Sampling obteve a maior recompensa acumulada média, seguido por UCB. A análise também mostrou o compromisso entre maximizar recompensa e estimar com precisão todos os parâmetros dos braços.
