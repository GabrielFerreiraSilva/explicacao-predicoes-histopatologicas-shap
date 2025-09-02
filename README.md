# Explicando Previsões de Câncer de Mama com Redes Neurais e SHAP

Este repositório aborda o campo da **Inteligência Artificial Explicável (XAI)**, aplicando o framework SHAP para interpretar as previsões de um modelo de Deep Learning (ResNet-50) treinado para classificar imagens histopatológicas de câncer de mama.

## 🔍 O Problema: A "Caixa-Preta" em Deep Learning

Modelos de redes neurais profundas, apesar de sua alta acurácia, são frequentemente considerados "caixas-pretas". Suas decisões complexas são difíceis de interpretar por humanos, o que representa um grande obstáculo para sua adoção em áreas críticas como a medicina, onde a confiança e a validação do raciocínio do modelo são fundamentais.

## 💡 A Solução: Explainable AI com SHAP

Este projeto utiliza a biblioteca **SHAP (SHapley Additive exPlanations)** para trazer transparência ao processo de decisão do modelo. O SHAP calcula a contribuição de cada "feature" (neste caso, pixels ou regiões da imagem) para a previsão final, respondendo à pergunta:

> *"Quais partes da imagem levaram o modelo a classificar esta amostra como benigna ou maligna?"*

## 🔗 Pré-requisito: Modelo Treinado

Este notebook **não realiza o treinamento do modelo**. Ele carrega e utiliza o classificador ResNet-50 treinado e salvo no projeto anterior.

-   **Repositório do Modelo:** [classficacao-imagens-histopatologicas-resnet-50](https://github.com/GabrielFerreiraSilva/classficacao-imagens-histopatologicas-resnet-50)

## 🛠️ Pipeline de Execução

O processo detalhado no notebook segue quatro etapas principais:

1.  **Preparação do Ambiente:** Importação de bibliotecas e carregamento do modelo ResNet-50 já treinado.
2.  **Pré-processamento de Dados:** Seleção de imagens de exemplo (benignas e malignas) e aplicação das transformações necessárias.
3.  **Cálculo dos Valores SHAP:** Utilização do `GradientExplainer` para calcular a importância de cada pixel na decisão do modelo.
4.  **Visualização e Interpretação:** Geração de mapas de calor que sobrepõem as imagens originais, destacando as áreas de maior influência para a previsão.

## 🚀 Como Usar

1.  Certifique-se de ter o arquivo do modelo treinado do projeto anterior.
2.  Realize o upload do arquivo na pasta `/content/` do ambiente do Colab.
3.  Clone este repositório.
4.  Abra o notebook `SHAP_ResNet_50.ipynb` no Google Colab ou em um ambiente Jupyter.
5.  Execute as células para gerar as explicações visuais para as imagens de exemplo.
