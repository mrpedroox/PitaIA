# PitaIA — Aprendizado de Máquina na Prática

O **PitaIA** é um minicurso de aprendizado de máquina voltado a estudantes de Ciência da Computação. O projeto conecta fundamentos de estatística e matemática à implementação de algoritmos em Python, com exemplos práticos em notebooks.

A proposta é entender o que acontece por trás dos modelos: de onde vêm as fórmulas, como os parâmetros são aprendidos e como avaliar os resultados. Os algoritmos são construídos passo a passo com **NumPy**, enquanto o **pandas** auxilia na leitura e exploração dos dados. Implementações do **scikit-learn** servem como referência para comparação.

## O que você encontra aqui

- Notebooks com código e explicações detalhadas de cada etapa.
- Deduções matemáticas ligadas às operações implementadas.
- Exemplos com dados reais, gráficos e interpretação dos resultados.
- Comparações entre implementações próprias e modelos de biblioteca.

O repositório está em construção: os materiais serão acrescentados conforme o desenvolvimento do minicurso. A ementa abaixo descreve o percurso previsto, não uma lista de notebooks já disponíveis.

## Conteúdo previsto

| Módulo | Tópicos |
|---|---|
| Dados e estatística | Aprendizado supervisionado e não supervisionado; média, variância e fundamentos de probabilidade; valores ausentes; codificação de categorias; separação entre treino e teste. |
| Regressão linear | Regressão simples e polinomial; erro quadrático médio (MSE); descida do gradiente; implementação do treinamento com NumPy. |
| Generalização | Baselines; MAE, RMSE e R²; overfitting e underfitting; viés e variância; intuição sobre regularização L1 e L2. |
| Regressão logística | Classificação binária; probabilidades; sigmoide; função de perda; implementação com NumPy; fronteiras de decisão. |
| Métricas e KNN | Matriz de confusão; acurácia, precisão, recall e F1; cálculo de distâncias; escolha de k; implementação de K-vizinhos mais próximos. |
| Árvores e validação | Árvores de decisão; Gini e entropia; critérios de divisão; validação cruzada K-fold; comparação de modelos. |
| Aprendizado não supervisionado | K-Means: centroides, atribuição e atualização; PCA: variância, componentes principais e redução de dimensionalidade. |
| Redes neurais | Neurônio artificial; pesos, bias e funções de ativação; perceptron; perceptron multicamadas (MLP); intuição de backpropagation; aplicação integradora. |

## Organização dos materiais

Os notebooks são acrescentados progressivamente e abordam os temas do minicurso. Cada arquivo `.ipynb` reúne a explicação dos conceitos, as fórmulas, a implementação e os resultados de seus exemplos.

Os conjuntos de dados e as orientações específicas de cada atividade são apresentados no respectivo notebook. As fontes dos dados também são indicadas nos materiais em que são utilizados.

## Como executar

### 1. Obtenha o projeto

Clone este repositório ou baixe seu conteúdo pelo botão **Code → Download ZIP** no GitHub. Abra um terminal dentro da pasta do projeto.

### 2. Crie um ambiente virtual

Use **Python 3.12**, versão utilizada para validar os notebooks e as dependências atuais.

```bash
python -m venv venv
```

No Linux ou macOS, caso o comando seja `python3`, use `python3 -m venv venv`.

Ative o ambiente no Linux ou macOS:

```bash
source venv/bin/activate
```

Ou no Windows, usando o PowerShell:

```powershell
.\venv\Scripts\Activate.ps1
```

O ambiente virtual mantém as dependências do projeto separadas das demais instalações de Python do computador.

### 3. Instale as dependências

Com o ambiente ativado:

```bash
python -m pip install -r requirements-aula.txt
```

O arquivo registra as versões das bibliotecas usadas para executar e validar o material.

### 4. Abra e execute os notebooks

**No VS Code:**

1. Instale as extensões **Python** e **Jupyter**.
2. Abra a pasta do projeto e escolha o notebook `.ipynb` que deseja estudar.
3. Em **Select Kernel**, escolha o Python do ambiente `venv`.
4. Execute as células de cima para baixo ou use **Restart Kernel and Run All**.

**Como alternativa, no JupyterLab:**

Instale a interface no mesmo ambiente e inicie-a:

```bash
python -m pip install jupyterlab
python -m jupyterlab
```

Na interface do navegador, escolha um notebook e execute suas células em ordem.

Antes de executar um notebook, confira suas instruções e a localização dos arquivos de dados utilizados. Preserve os caminhos esperados pelo código e use a pasta indicada no material como diretório de execução.

Execute as células na ordem apresentada. Se alterações deixarem variáveis de etapas anteriores inconsistentes, reinicie o kernel e execute todas as células novamente.

A pasta `venv/` é criada localmente e deve ficar fora do controle de versão, por meio do `.gitignore`.

## Referências

- Christopher M. Bishop. *Pattern Recognition and Machine Learning*. Springer, 2006.
- Documentação do [NumPy](https://numpy.org/doc/), [pandas](https://pandas.pydata.org/docs/), [Matplotlib](https://matplotlib.org/stable/) e [scikit-learn](https://scikit-learn.org/stable/).
