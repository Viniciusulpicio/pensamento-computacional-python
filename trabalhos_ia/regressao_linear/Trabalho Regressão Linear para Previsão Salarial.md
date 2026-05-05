# Trabalho: Regressão Linear para Previsão Salarial

# Objetivo

Aplicar na prática conceitos de **EDA, limpeza de dados, engenharia de variáveis e regressão linear** para *prever o salário dos estudantes* com base em atributos acadêmicos e profissionais.

Dataset utilizado: Student Placement Prediction Dataset 2026

---

# Etapa 1: Aquisição dos dados

Baixar o dataset no Kaggle:

[https://www.kaggle.com/datasets/sehaj1104/student-placement-prediction-dataset-2026](https://www.kaggle.com/datasets/sehaj1104/student-placement-prediction-dataset-2026)

Carregar utilizando **pandas**.

---

# Etapa 2: Análise Exploratória (EDA)

Utilizando pandas:

- Visualização inicial:
    - `head()`
    - `info()`
    - `describe()`
- Identificar:
    - Tipos de variáveis (numéricas vs categóricas)
    - Distribuição das variáveis, principalmente da `salary_package_lpa`
    - Relações iniciais com:
    - `cgpa`
    - `internships_count`
    - `projects_count`
    - `communication_skill_score`
    - E outras colunas relevantes
- Verificar:
    - Outliers
    - Escalas diferentes entre variáveis
    - Distribuições (normalidade, distorção)

---

# Etapa 3: Visualização

Criar pelo menos 5 gráficos relevantes, por exemplo:

- Histograma do salário
- Scatter: `cgpa` vs salário
- Scatter: `internships_count` vs salário
- Boxplot por `branch`
- Heatmap de correlação
- Lembre de criar os gráficos que achar relevante, esses foram sugestões

Regras:

- Todos os gráficos devem ter título e rótulos
- Escolher visualizações que ajudem na modelagem

---

# Etapa 4: Limpeza e Preparação dos Dados

Mesmo sem valores ausentes, ainda há preparação importante:

- Remover colunas irrelevantes, como `student_id`
- Tratar variáveis categóricas, como `gender`
- Verificar necessidade de normalização ou padronização

---

# Etapa 5: Engenharia de Variáveis

Criar pelo menos 2 novas variáveis, por exemplo:

- Score técnico combinado:
    - média de `coding_skill_score`, `aptitude_score`, `logical_reasoning_score`
- Experiência prática:
    - `internships_count + projects_count`
- Engajamento profissional:
    - combinação de `linkedin_connections` e `github_repos`

Justificar as escolhas.

---

# Etapa 6: Modelagem com Regressão Linear

Utilizar regressão linear para prever:

- Variável alvo: `salary_package_lpa`

Separar dados:

- Treino e teste (ex: 80/20, 70/30)

Treinar modelo usando `LinearRegression` do **scikit-learn**

---

# Etapa 7: Avaliação do Modelo

Avaliar com métricas apropriadas:

- RMSE (erro quadrático médio)
- MAE (erro absoluto médio)
- R²

Analisar:

- O modelo está performando bem?
- Existe overfitting?
- Quais variáveis parecem mais importantes?

---

# Etapa 8: Interpretação

Responder:

- Quais fatores influenciam mais o salário?
- Existe relação forte entre desempenho acadêmico e salário?
- Experiência prática impacta mais que [notas](https://moodle.unimar.br/mod/url/view.php?id=304709)?
- Comunicação influência salário?

---

# Etapa 9: Conclusão

---

# Observação importante

A variável `placement_status` **não deve ser usada como target**

---

# Entrega

- Notebook Jupyter (.ipynb)

Deve conter:

- Nome e RA dos integrantes
- Separação clara entre: Aquisição (Download), Exploratory Data Analaysis (EDA), Engenharia de Variáveis e Treinamento do Modelo
- Código organizado
- Explicações claras
- Gráficos com interpretação (não apenas exibição)

---

# Avaliação

**Nota final = Organização × Qualidade do EDA × Qualidade da Engenharia de Variáveis × Resultado do Treinamento**

# Organização

Avalia a clareza e estrutura do notebook:

- Código bem organizado e segmentado por etapas
- Uso adequado de títulos e explicações
- Legibilidade (nomes de variáveis, comentários quando necessário)
- Execução sequencial sem erros

---

# Qualidade do EDA

Avalia a profundidade da análise exploratória:

- Uso correto de `head`, `info`, `describe`
- Identificação de padrões e distribuições
- Uso de gráficos relevantes (não apenas quantidade e nem apenas o que citei como exemplo)
- Interpretação dos gráficos (não apenas exibição)
- Identificação de possíveis relações com o salário

---

# Qualidade da Engenharia de Variáveis

Avalia a capacidade de criar variáveis úteis:

- Criação de variáveis com justificativa
- Uso de combinações relevantes (ex: scores, experiência)
- Tratamento adequado de variáveis categóricas
- Evidência de que as novas variáveis ajudam o modelo

---

# Resultado do Treinamento

Avalia o desempenho e a análise do modelo:

- Separação correta entre treino e teste
- Uso de métricas apropriadas (RMSE, MAE, R²)
- Interpretação dos resultados

---

# Observação

Como os critérios são multiplicativos, desempenho muito baixo em qualquer um dos itens impacta significativamente a nota final.