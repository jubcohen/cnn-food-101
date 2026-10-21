# Classificação de Alimentos com CNN (Food-101)

Este projeto implementa uma **Rede Neural Convolucional (CNN)** utilizando **Keras e TensorFlow** para classificar imagens de pratos de comida a partir do popular dataset **Food-101**. O projeto aborda desde o download automatizado dos dados via API até o pré-processamento, aumento de dados (*data augmentation*) e treinamento do modelo.

---

## Tecnologias Utilizadas
* **Python**
* **TensorFlow / Keras**
* **KaggleHub** (para download do dataset)
* **Matplotlib** (visualização de dados e gráficos de treinamento)

---

## Estrutura do Modelo
A arquitetura da CNN construída no projeto conta com:
* Camada de **Data Augmentation** (Flip horizontal, rotação e zoom) para evitar *overfitting*[cite: 3, 4].
* Camadas de **Rescaling** para normalização dos pixels[cite: 4].
* 4 blocos de **Conv2D** seguidos de **MaxPooling2D**[cite: 4].
* Camadas de **Dropout** (0.3 / 0.5) para regularização[cite: 4].
* Camadas densas (*Dense*) com ativação ReLU e Softmax na camada de saída para classificação multiclasse[cite: 4].
* Otimizador **Adam** e função de perda `categorical_crossentropy`[cite: 5].

---

## Resultados e Visualizações
O modelo foi treinado utilizando técnicas de *Early Stopping* para restaurar os melhores pesos e evitar o sobreajuste[cite: 5]. Durante os testes com subconjuntos e classes selecionadas, o modelo apresentou excelentes curvas de aprendizado na convergência da acurácia e redução da perda (*loss*).

---

##  Como Executar

1. Clone o repositório:
   ```bash
   git clone [https://github.com/jubcohen/cnn-food-101.git](https://github.com/jubcohen/cnn-food-101.git)
   cd cnn-food-101
