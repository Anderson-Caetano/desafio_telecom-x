# 📊 Análise de Evasão de Clientes (Churn) - Telecom X

Este projeto tem como objetivo investigar os fatores que influenciam a evasão de clientes (churn) em uma operadora de telecomunicações fictícia chamada **Telecom X**. Através de análise de dados, visualizações, engenharia de atributos e modelagem preditiva, buscamos entender o comportamento dos clientes e prever quais têm maior probabilidade de deixar a empresa.

---

## 🧠 Objetivos

- Explorar e tratar os dados de clientes da Telecom X.
- Identificar padrões associados à evasão.
- Construir modelos preditivos capazes de antecipar o churn.
- Oferecer insights e recomendações para reduzir a perda de clientes.

---

## 📁 Estrutura do Projeto

O projeto foi desenvolvido em um **Jupyter Notebook**, dividido em etapas claras:

### 1. 📌 Extração
- Leitura dos dados diretamente de uma URL externa em formato JSON.
- Conversão para DataFrame com `pandas`.

### 2. 🧼 Transformação
- Expansão de colunas aninhadas com `json_normalize`.
- Remoção de colunas irrelevantes.
- Padronização dos nomes de colunas.
- Codificação da variável `churn` em valores binários (0 = ativo, 1 = evadiu).
- Aplicação de **One-Hot Encoding**.

### 3. 📊 Carga e Análise
- Verificação de nulos.
- Análise da distribuição da variável alvo (`churn`).
- Visualização de desequilíbrio e aplicação do SMOTE.

### 4. ⚖️ Normalização
- Aplicada somente em modelos que requerem (Regressão Logística).
- Dados foram padronizados com `StandardScaler`.

### 5. 🔁 Correlação
- Análise das variáveis numéricas com a variável alvo.
- Geração de matriz de correlação com `seaborn`.

### 6. 📈 Exploração Visual
- Visualizações com boxplots comparando `tenure` (tempo de contrato), `charges_monthly` (valor mensal) e `churn`.
- Análise adicional do número de serviços contratados.

### 7. ✂️ Divisão dos Dados
- Separação entre treino e teste (70/30).
- Preservação da proporção da variável `churn`.

### 8. 🤖 Modelagem
- Modelos aplicados:
  - **Regressão Logística**
  - **Random Forest**
- Avaliação com métricas:
  - Acurácia
  - Precisão
  - Recall
  - F1-score
  - ROC AUC
  - Matriz de Confusão

### 9. 💾 Salvamento e Predições
- Modelos salvos com `joblib`.
- Exemplo de carregamento dos modelos para prever novos dados.

### 10. 📝 Relatório Final
- Sumário contendo introdução, tratamento dos dados, análises, insights e recomendações.
- Documento inserido no próprio notebook.

---

## 🔍 Principais Insights

- Clientes com menor tempo de contrato têm maior probabilidade de evadir.
- Valores mensais mais altos estão associados a maiores taxas de churn.
- Clientes com menos serviços contratados têm menor engajamento e maior risco.
- O modelo **Random Forest** teve o melhor desempenho geral com ROC AUC ≈ 0.83.

---

## 📌 Tecnologias Utilizadas

- Python 3.11
- pandas
- seaborn
- matplotlib
- scikit-learn
- imblearn (SMOTE)
- joblib

---

## 📁 Como Executar

1. Clone o repositório:
```bash
git clone https://github.com/seuusuario/nome-do-repositorio.git
