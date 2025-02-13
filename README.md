# Transfer Learning com MobileNetV2 - Classificação de Gatos e Cachorros

Este projeto implementa Transfer Learning utilizando a rede MobileNetV2 para classificar imagens de gatos e cachorros, utilizando o dataset cats_vs_dogs do TensorFlow Datasets.

📌 Requisitos

Antes de executar o projeto, certifique-se de ter os seguintes pacotes instalados:

Python 3.x

TensorFlow

TensorFlow Datasets

NumPy

Matplotlib

Caso esteja rodando no Google Colab, os pacotes já estão pré-instalados.


🚀 Como Executar o Projeto

Clone este repositório:

git clone https://github.com/OctavioSB11/transfer-learning-cats-dogs.git

Acesse o diretório do projeto:

cd transfer-learning-cats-dogs

Abra o notebook transfer_learning_cats_dogs.ipynb no Jupyter Notebook ou Google Colab.

Execute todas as células para:

Carregar o dataset

Preparar as imagens

Aplicar Transfer Learning com MobileNetV2

Treinar o modelo

Avaliar os resultados

📊 Resultados

Durante o treinamento, o modelo aprende a distinguir entre gatos e cachorros com alta precisão. As métricas são plotadas para avaliar seu desempenho.

💾 Salvando e Exportando o Modelo

Para reutilizar o modelo treinado:

model.save('cats_vs_dogs_model.h5')

Isso permitirá carregar o modelo posteriormente para inferência em novas imagens.
