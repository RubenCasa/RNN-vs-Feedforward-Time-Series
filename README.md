# Análisis Comparativo: Redes Feedforward (MLP) vs. Redes Recurrentes (RNN)

Este repositorio contiene un análisis práctico y teórico que compara el rendimiento y la arquitectura de un Perceptrón Multicapa (MLP) frente a una Red Neuronal Recurrente (RNN Vanilla) en una tarea de predicción de series de tiempo. Proyecto desarrollado usando **PyTorch**.

##  Descripción del Proyecto

El objetivo de esta práctica es demostrar empíricamente por qué las redes recurrentes son superiores para procesar datos secuenciales en comparación con las redes feedforward. 

Se generó una serie de tiempo sintética (señal sinusoidal con ruido) de 1000 observaciones. Se entrenaron ambos modelos para predecir el siguiente valor basándose en una ventana temporal (lookback) de 20 pasos. 

A pesar de tener un tercio de los parámetros, la **RNN logró una reducción del 9.4% en el Error Cuadrático Medio (MSE)** respecto al MLP, demostrando su capacidad intrínseca para mantener la "memoria" del estado temporal secuencial.


##  Resultados Principales

| Métrica | MLP (Feedforward) | RNN Vanilla |
| :--- | :---: | :---: |
| **Parámetros Totales** | 3,457 | **1,153** |
| **MSE (test)** | 0.003065 | **0.002777** |
| **MAE (test)** | 0.045381 | **0.042841** |

> La RNN superó al MLP en precisión utilizando una arquitectura significativamente más liviana (reducción del 9.4% en MSE).

##  Tecnologías Utilizadas

*   **Python 3.10+**
*   **PyTorch**: Construcción y entrenamiento de redes neuronales (Módulo `nn.RNN` y `nn.Linear`).
*   **Matplotlib / Scikit-learn**: Visualización de métricas de pérdida, evaluación y predicciones temporales.
*   **Python-docx**: Automatización de reportería estilo APA 7.

##  Autor
* **Rubén Casa** - Proyecto de Machine Learning 2 (Deep Learning) - 2026.
