Transfer Learning com MobileNetV2 - Classificação de Gatos e Cachorros

Este projeto implementa Transfer Learning utilizando a rede MobileNetV2 para classificar imagens de gatos e cachorros, utilizando o dataset cats_vs_dogs do TensorFlow Datasets.

📌 Requisitos

Antes de executar o projeto, certifique-se de ter os seguintes pacotes instalados:

Python 3.x

TensorFlow

TensorFlow Datasets

NumPy

Matplotlib

Caso esteja rodando no Google Colab, os pacotes já estão pré-instalados.

📂 Estrutura do Projeto

📁 transfer-learning-cats-dogs
    │── 📄 transfer_learning_cats_dogs.ipynb  # Notebook com a implementação
    │── 📄 README.md  # Documentação do projeto
    │── 📄 cats_vs_dogs_model.h5  # Modelo treinado salvo (gerado após o treinamento)

🚀 Como Executar o Projeto

Clone este repositório:

git clone https://github.com/seu-usuario/transfer-learning-cats-dogs.git

Acesse o diretório do projeto:

cd transfer-learning-cats-dogs

Abra o notebook transfer_learning_cats_dogs.ipynb no Jupyter Notebook ou Google Colab.

Execute todas as células para:

Carregar o dataset

Preparar as imagens

Aplicar Transfer Learning com MobileNetV2

Treinar o modelo

Avaliar os resultados

🧪 Testando o Modelo

Após o treinamento, você pode testar o modelo com imagens do próprio dataset:

from tensorflow.keras.models import load_model
import tensorflow as tf
import numpy as np
import matplotlib.pyplot as plt

# Carregar o modelo treinado
model = load_model('cats_vs_dogs_model.h5')

# Obter um lote de imagens do dataset de validação
ds_sample = ds_val.take(1)

for images, labels in ds_sample:
    for i in range(5):
        img = images[i].numpy()
        img_array = np.expand_dims(img, axis=0)
        prediction = model.predict(img_array)
        predicted_label = "Cachorro 🐶" if prediction[0] > 0.5 else "Gato 🐱"
        true_label = "Cachorro 🐶" if labels[i].numpy() == 1 else "Gato 🐱"
        plt.imshow(img)
        plt.axis('off')
        plt.title(f"Pred: {predicted_label} | Real: {true_label}")
        plt.show()

📊 Resultados

Durante o treinamento, o modelo aprende a distinguir entre gatos e cachorros com alta precisão. As métricas são plotadas para avaliar seu desempenho.

💾 Salvando e Exportando o Modelo

Para reutilizar o modelo treinado:

model.save('cats_vs_dogs_model.h5')

Isso permitirá carregar o modelo posteriormente para inferência em novas imagens.

📜 Licença

Este projeto é de código aberto e pode ser utilizado livremente para fins educacionais e de pesquisa. Sinta-se à vontade para contribuir! 🚀
