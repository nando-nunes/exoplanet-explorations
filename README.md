# Exoplanet Explorations 🪐

## Sobre o Projeto
Este repositório contém os Jupyter Notebooks desenvolvidos durante o projeto do curso de verão de Inteligência Artificial da **NSLC (National Student Leadership Conference)**. O objetivo principal deste projeto foi construir modelos computacionais para identificar e classificar exoplanetas utilizando dados reais do telescópio espacial Kepler, da NASA.

O trabalho foi desenvolvido de forma colaborativa em um grupo de 6 pessoas, passando desde a exploração inicial de dados astronômicos até a implementação de modelos de Deep Learning.

## Objetivos
- Compreender o método de **Trânsito Fotométrico** para a detecção de exoplanetas.
- Processar e visualizar grandes volumes de dados de curvas de luz estelares.
- Aplicar técnicas de pré-processamento para tratar dados altamente desbalanceados e ruidosos.
- Desenvolver e comparar modelos de **Machine Learning** e **Deep Learning** para automatizar a descoberta de novos planetas.

## Estrutura do Repositório

O projeto é dividido em três seções principais:

### [Section 1: Exoplanets & Transit Photometry](Section1_Exoplanets.ipynb)
- **Compreensão de Dados:** Carregamento e exploração inicial dos datasets (`exoTrain.csv` e `exoTest.csv`).
- **Análise Exploratória:** Visualização de curvas de luz (variação do fluxo luminoso das estrelas ao longo do tempo).
- **Identificação de Padrões:** Análise visual de quedas periódicas no brilho estelar (*folding* de curvas de luz) para detectar possíveis trânsitos de exoplanetas.

### [Section 2: Exoplanet Classification & Preprocessing](Section2_Exoplanets.ipynb)
- **Engenharia de Recursos e Filtros:** Aplicação de transformadas de Fourier e filtros Savitzky-Golay para suavizar ruídos nas curvas de luz.
- **Normalização:** Escalonamento de dados utilizando o `MinMaxScaler` da biblioteca Scikit-Learn.
- **Data Augmentation:** Resolução do problema de desbalanceamento severo de classes (poucos exoplanetas em relação a não-exoplanetas) gerando dados sintéticos com o algoritmo **SMOTE**.
- **Modelos Clássicos:** Treinamento e avaliação de vários algoritmos tradicionais de Machine Learning (K-Nearest Neighbors, Random Forest, Regressão Logística e Decision Trees) analisando matrizes de confusão e métricas de desempenho.

### [Section 3: Deep Learning & Neural Networks](Section3_Exoplanets.ipynb)
- **Redes Neurais Artificiais:** Introdução a arquiteturas mais complexas para lidar com dados de séries temporais estelares.
- **Multi-layer Perceptron (MLP) e CNNs:** Criação, treinamento e otimização de Redes Neurais Convolucionais 1D/2D utilizando a biblioteca Keras para melhorar a precisão da classificação de exoplanetas de forma automatizada.

## Tecnologias e Bibliotecas Utilizadas
- **Linguagem:** Python
- **Manipulação e Análise de Dados:** Pandas, NumPy, SciPy
- **Visualização:** Matplotlib
- **Machine Learning:** Scikit-Learn, Imbalanced-learn (SMOTE)
- **Deep Learning:** Keras / TensorFlow

## Como Executar
Os notebooks foram projetados para serem executados no Google Colab com aceleração de hardware via GPU. 
Para testar, basta abrir o respectivo arquivo `.ipynb` no Colab, certificar-se de ativar o ambiente GPU (`Runtime > Change runtime type > GPU`) e executar as células sequencialmente. Os dados necessários (arquivos CSV) serão baixados automaticamente nos blocos de inicialização.
