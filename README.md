# Classificação de Imagens do Dataset Fruits 360

## Descrição
Este projeto desenvolve um sistema para a classificação de frutas utilizando redes neurais convolucionais (CNNs) treinadas no dataset **Fruits 360**, amplamente utilizado em visão computacional. Foram implementados os modelos **ResNet18** e **AlexNet**, comparando seu desempenho em termos de precisão, perda e matrizes de confusão. O código inclui pré-processamento, treinamento, validação e visualização dos resultados.

Confira o vídeo explicativo sobre redes neurais convolucionais e a utilização de PyTorch:  
[Introdução às Redes Neurais Convolucionais](https://www.youtube.com/watch?v=dwh7w9s6SCQ&feature=youtu.be)

---

## Dependências
Antes de executar o projeto, certifique-se de ter as seguintes bibliotecas instaladas:
- **torch**: Framework para redes neurais profundas.
- **torchvision**: Conjunto de ferramentas e datasets para visão computacional.
- **matplotlib**: Plotagem de gráficos e visualização de resultados.
- **numpy**: Manipulação de arrays e cálculos matemáticos.
- **scikit-learn**: Avaliação e métricas de classificação.
- **kagglehub**: Para o download do dataset Fruits 360 diretamente do Kaggle.

### Instalação das dependências:
```bash
pip install torch torchvision matplotlib numpy scikit-learn kagglehub
