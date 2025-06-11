# 🚀 Fitness Overload Risk Predictor

Este projeto aplica técnicas de **Ciência de Dados** e **Inteligência Artificial** para prever o risco de **sobrecarga física ou exaustão** com base em dados diários de atividades monitoradas por dispositivos vestíveis (wearables), como smartwatches.

O objetivo é demonstrar, de forma prática, como uma **Rede Neural Artificial (RNA)** pode ser usada para apoiar o bem-estar físico, prevenindo estados de fadiga ou desgaste físico.

---

## 📊 Sobre o Dataset

O conjunto de dados utilizado é o:

📌 **Fitness Track Daily Activity Dataset in DS**  
🔗 Disponível no [Kaggle](https://www.kaggle.com/datasets/sheemazain/fitness-track-daily-activity-dataset-in-ds)

Contém registros diários detalhados de:

- Contagem de passos
- Calorias queimadas
- Tempo sedentário
- Tempo de atividade (leve, moderada, intensa)
- Distância percorrida

---

## 🔍 Etapas do Projeto

1. **Carregamento e limpeza de dados**
2. **Análise exploratória de dados (EDA)**
3. **Criação da variável alvo simulada `overload_risk`**
   - Definida como 1 (com risco) se:
     - Calorias queimadas > 3500 _ou_
     - Passos > 17.000
4. **Pré-processamento e normalização dos dados**
5. **Balanceamento das classes usando `RandomOverSampler`**
6. **Treinamento de um modelo `MLPClassifier` (Rede Neural MLP)**
7. **Avaliação do modelo com métricas de classificação**
8. **Interface interativa de input para predição personalizada**

---

## 🧠 Modelo Utilizado

Foi implementado um **MLPClassifier** do `scikit-learn`, com:

- Arquitetura: 2 camadas ocultas (64 e 32 neurônios)
- Função de ativação: ReLU
- Otimizador: Adam
- Estratégia de parada: `early_stopping=True`
- Normalização: `MinMaxScaler`

---

## 📈 Resultados

O modelo foi avaliado com:

- **Precision**, **Recall** e **F1-Score**
- **Matriz de confusão**
- Importância do recall alto na classe de risco (minimizar falsos negativos)

⚠️ Nota: A variável alvo `overload_risk` é **simulada** com base em regras empíricas. Em um cenário real, seria necessário integrar dados fisiológicos e validar os critérios com especialistas.

---

## 🧪 Como Usar

Você pode executar o script final e usar a função `predict_overload_risk()` para inserir manualmente seus dados de atividade física diária e obter uma predição instantânea:

```bash
python nome_do_arquivo.py
