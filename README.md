# Análise de Dados e Predição com Machine Learning

## Descrição:

O objetivo principal deste projeto é identificar padrões no comportamento de usuários e prever sua categorização utilizando técnicas de aprendizado de máquina. Para isso, utilizamos um conjunto de dados que contém informações sobre chamadas, mensagens enviadas, uso de internet e classificação de usuários.

Com base nesses padrões, buscamos fornecer insights que auxiliem na tomada de decisão estratégica e na otimização de recursos.

Os dados analisados abrangem diferentes variáveis, possibilitando a construção de modelos de classificação para prever se um usuário pertence a uma determinada categoria (`is_ultra`). O projeto tem como foco o desenvolvimento de modelos preditivos robustos e eficientes.

---

## Conjunto de Dados:

Atualmente, o conjunto de dados utilizado neste projeto inclui as seguintes colunas:

- `calls` - Quantidade de chamadas realizadas.
- `minutes` - Duração total das chamadas em minutos.
- `messages` - Quantidade de mensagens enviadas.
- `mb_used` - Uso total de dados (MB).
- `is_ultra` - Classificação binária do usuário (0 ou 1).

Os dados foram carregados do arquivo `users_behavior.csv` e passaram por um processo de limpeza e normalização para garantir a qualidade e a consistência das análises.

---

## Arquitetura e Tecnologias Utilizadas

Este projeto segue princípios de **arquitetura modular**, garantindo escalabilidade e reuso eficiente de código. A estrutura adota uma abordagem **camada por camada**, separando **dados, processamento, modelagem e avaliação**.

🔹 **Camada de Dados**: Tratamento e preparação dos dados utilizando `Pandas` e `NumPy`.

🔹 **Camada de Modelagem**: Implementação e ajuste de algoritmos de aprendizado de máquina.

🔹 **Camada de Avaliação**: Validação dos modelos com métricas de desempenho.

🔹 **Camada de Visualização**: Geração de relatórios gráficos e dashboards para apresentação dos resultados.

As principais tecnologias e bibliotecas utilizadas incluem:

- **Python 3.8+** – Linguagem base para análise e processamento de dados.
- **Pandas / NumPy** – Manipulação e tratamento de dados estruturados.
- **Matplotlib / Seaborn** – Criação de visualizações gráficas avançadas.
- **Scikit-Learn** – Modelos de aprendizado de máquina e avaliação de desempenho.
- **Jupyter Notebook** – Desenvolvimento e apresentação de insights.

---

## Modelos Utilizados:

Dois modelos de classificação foram testados para a predição da variável `is_ultra`:

### 1. Random Forest Classifier
- Melhor configuração de hiperparâmetros obtida via **GridSearchCV**:
  - `n_estimators`: 100
  - `max_depth`: 10
  - `min_samples_leaf`: 1
  - `min_samples_split`: 2
- **Acurácia no conjunto de teste**: 84.29%

### 2. Regressão Logística
- Melhor configuração de hiperparâmetros obtida via **GridSearchCV**:
  - `C`: 0.01
  - `solver`: liblinear
- **Acurácia no conjunto de teste**: 70.61%

🔍 **Conclusão**: O modelo **Random Forest Classifier** apresentou melhor desempenho e foi selecionado como a solução final.

---

## Execução do Projeto

### 🔧 Pré-requisitos
Certifique-se de que possui o **Python 3.8+** instalado em sua máquina. Em seguida, instale as dependências do projeto utilizando:

```bash
pip install -r requirements.txt
```

### 🚀 Execução do modelo
Para rodar a análise de dados e treinamento do modelo, execute o script principal:

```bash
python main.py
```
