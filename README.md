# Classificação de Imagens CIFAR-10 com Redes Convolucionais (CNN) em Keras

Este repositório apresenta um projeto de **classificação de imagens** utilizando o dataset [CIFAR-10](https://www.cs.toronto.edu/~kriz/cifar.html) e uma **rede neural convolucional (CNN)** implementada com Keras. O objetivo é treinar um modelo capaz de identificar corretamente a classe de imagens coloridas de 32x32 pixels, distribuídas em 10 categorias diferentes.

---

## Sobre o Dataset

O **CIFAR-10** é um conjunto de dados amplamente utilizado em tarefas de visão computacional, composto por:

- **60.000 imagens coloridas** (32x32 pixels)
- **10 classes**: avião, automóvel, pássaro, gato, cervo, cachorro, sapo, cavalo, navio e caminhão
- **50.000 imagens para treino** e **10.000 para teste**

---

## Etapas do Projeto

### 1. Pré-processamento dos Dados

- **Carregamento:** Utilização do dataset CIFAR-10 via Keras.
- **Normalização:** Conversão dos pixels para o intervalo [0, 1].
- **To_categorical:** Conversão dos rótulos para o formato categórico.

### 2. Construção do Modelo

A arquitetura da CNN utilizada é composta por:

- **Camadas Convolucionais (Conv2D):** Extraem características espaciais das imagens.
- **Camadas de Pooling (MaxPooling2D):** Reduzem a dimensionalidade espacial.
- **Camada Flatten:** Achata a saída para um vetor 1D.
- **Camada Densa (Dense):** Realiza a classificação final.
- **Dropout:** Ajuda a evitar overfitting.


### 3. Compilação

- **Otimizador:** Adam (`learning_rate=0.001`)
- **Função de perda:** Categorical Crossentropy
- **Métrica:** Acurácia

### 4. Treinamento

- **Épocas:** 20
- **Batch size:** 128
- **Validação:** Utiliza o conjunto de teste para validação durante o treinamento

### 5. Avaliação

Após o treinamento, o modelo é avaliado no conjunto de teste para medir a acurácia final.

### 6. Conclusão

Com a arquitetura proposta, foi possível atingir uma acurácia de aproximadamente 76% no conjunto de teste.

### 7. Arquivos

redes_neurais_cifar10.ipynb - Arquitetura da Rede Neural escolhida.

modelagem_redes_neurais.ipynb - Performance de todas as redes simuladas.

