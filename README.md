# PitaIA — Aprendizado de Máquina na Prática

O **PitaIA** é um minicurso de aprendizado de máquina voltado a estudantes de Ciência da Computação. O projeto conecta fundamentos de estatística e matemática à implementação de algoritmos em Python, com exemplos práticos em notebooks.

A proposta é entender o que acontece por trás dos modelos: de onde vêm as fórmulas, como os parâmetros são aprendidos e como avaliar os resultados. Os algoritmos são construídos passo a passo com **NumPy**, enquanto o **pandas** auxilia na leitura e exploração dos dados. Implementações do **scikit-learn** servem como referência para comparação.

## O que você encontra aqui

- Notebooks com código e explicações detalhadas de cada etapa.
- Deduções matemáticas ligadas às operações implementadas.
- Exemplos com dados reais, gráficos e interpretação dos resultados.
- Comparações entre implementações próprias e modelos de biblioteca.

O repositório está em construção. As aulas disponíveis estão listadas abaixo; a ementa completa apresenta também os temas que serão desenvolvidos nas próximas etapas.

## Aulas disponíveis

### Regressão logística — classificação binária

[Abrir o notebook de regressão logística](Regress%C3%A3o%20Log%C3%ADstica/regressao-logistica-livecoding.ipynb) · [Dataset: breast-cancer.csv](Regress%C3%A3o%20Log%C3%ADstica/breast-cancer.csv)

Classificação de amostras como benignas ou malignas a partir de 30 medidas celulares, com implementação em NumPy e comparação com `LogisticRegression` do scikit-learn.

- Separação de treino e teste e padronização com NumPy.
- Combinação linear, intercepto e representação matricial.
- Dedução da sigmoide, da perda logarítmica e do gradiente.
- Treinamento por descida do gradiente e verificação do critério de parada.
- Probabilidades, limiar de decisão, acurácia, falsos negativos e falsos positivos.
- Comparação das implementações sem regularização e interpretação dos gráficos.

### Regressão linear — OLS, GD e SGD

[Abrir o notebook de regressão linear](Regress%C3%A3o%20LInear/regressao-linear-livecoding.ipynb) · [Dataset: housing.csv](Regress%C3%A3o%20LInear/housing.csv)

Previsão do valor mediano das moradias de regiões da Califórnia com regressão linear múltipla. A aula retoma brevemente a preparação já apresentada na regressão logística e detalha as técnicas novas.

- Imputação de valores ausentes pela mediana e codificação one-hot com categoria de referência.
- Dedução do erro quadrático médio (MSE), de seu gradiente e das equações normais.
- Mínimos quadrados ordinários (OLS) com solução direta em NumPy.
- Implementações de descida do gradiente em lote (GD) e estocástica (SGD), com taxa decrescente no SGD.
- Gráficos de MSE, análise da convergência e comparação com a solução direta.
- Baseline pela média, MSE, RMSE, MAE e R² no treino e no teste.
- Treinamento com `LinearRegression` e `SGDRegressor` do scikit-learn.
- Interpretação dos coeficientes na escala original e diagnóstico dos resíduos.

### KNN — K-vizinhos mais próximos

[Abrir o notebook de KNN](KNN/knn-livecoding.ipynb) · [Dataset: breast-cancer.csv](KNN/breast-cancer.csv)

Classificação com as mesmas 30 características e a mesma convenção de rótulos da aula de regressão logística: benigno = 0 e maligno = 1. O CSV é uma cópia idêntica do arquivo daquela aula.

- Dedução da distância euclidiana, efeito da padronização e justificativa da votação.
- Implementação de distâncias, busca de vizinhos e previsão binária com NumPy.
- Explicações de cada linha de código e exemplos pequenos para conferir as contas à mão.
- Seleção de `k` em validação interna, com padronização aprendida apenas no ajuste e teste reservado para o final.
- Matriz de confusão, acurácia, precisão, recall, especificidade e F1 calculados manualmente.
- Comparação com `KNeighborsClassifier` usando os mesmos dados padronizados com NumPy.
- Código direto para iniciantes, gráfico de validação e interpretação dos resultados.
- Visualização dos vizinhos de uma consulta, do efeito de `k` nas fronteiras e comparação com regressão logística em duas luas artificiais.

Os três notebooks incluem explicações, fórmulas, código, resultados e gráficos salvos. Para acompanhar as referências aos conceitos já apresentados, siga a ordem acima.

## Ementa do minicurso

A ementa reúne o conteúdo já abordado e o planejamento das próximas aulas. A lista de aulas disponíveis acima indica o que já foi implementado; alguns tópicos dos módulos abaixo ainda serão acrescentados.

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
python -m pip install -r requirements.txt
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
