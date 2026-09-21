# 🛡️ CreditGuard: Detecção de Fraudes com Foco em Impacto Financeiro

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://www.python.org/)
[![XGBoost](https://img.shields.io/badge/Model-XGBoost-orange.svg)](https://xgboost.readthedocs.io/)
[![Status](https://img.shields.io/badge/Status-Conclu%C3%ADdo-brightgreen.svg)]()

Este projeto desenvolve uma solução completa de Machine Learning para detecção de fraudes em transações de cartão de crédito. O diferencial desta abordagem está na **otimização de custos de negócio**, indo além de métricas estatísticas tradicionais para otimizar o limiar financeiro da operação.

---

## 📌 Problema de Negócio

Em cenários reais de detecção de fraude:
1. **Desbalanceamento Extremo:** As fraudes representam menos de **0.2%** do total de transações.
2. **Matriz de Custo Assimétrica:** 
   * **Falso Negativo (Fraude não pega):** Prejuízo alto (estimado em ~R$ 500/transação).
   * **Falso Positivo (Alerta Falso):** Custo baixo de atrito/verificação (~R$ 10/transação).

Avaliar modelos apenas por *Acurácia* ou *F1-Score* tradicional não maximiza o retorno financeiro da instituição.

---

## 📊 Principais Resultados

* **Recall de Fraudes:** **87.7%** das fraudes detectadas no modelo final.
* **Redução de Custos Operacionais:** Economia direta de **21.6%** no custo total de risco em comparação ao modelo padrão (Threshold 0.50).
* **Threshold Ótimo Encontrado:** **0.01**, priorizando a captura de fraudes e minimizando o prejuízo por falsos negativos.

---

## 🛠️ Tecnologias Utilizadas

* **Linguagem:** Python
* **Manipulação & Visualização:** Pandas, NumPy, Matplotlib, Seaborn
* **Pré-processamento & ML:** Scikit-Learn, XGBoost, Imbalanced-Learn (SMOTE)

---

## 📈 Otimização de Limiar Financeiro (Threshold Tuning)

Ao ajustar o limiar de decisão de 0.50 para 0.01, o modelo passou a priorizar a captura de fraudes críticas sem sobrecarregar a operação com alertas falsos indevidos.

| Métrica / Cenário | Threshold Padrão (0.50) | Threshold Ótimo (0.01) | Impacto |
| :--- | :---: | :---: | :---: |
| **Custo Estimado** | R$ 8.600,00 | **R$ 6.740,00** | **- R$ 1.860,00** |
| **Fraudes Pegas (TP)** | 81 | **86** | +5 fraudes evitadas |
| **Falsos Positivos (FP)** | 10 | **74** | Atrito controlado |

---

## 🚀 Como Executar o Projeto

1. Clone este repositório:
   ```bash
   git clone [https://github.com/taymarinho700/credit-card-fraud-detection.git](https://github.com/taymarinho700/credit-card-fraud-detection.git)