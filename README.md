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


## Instruções de Execução

1. **Clone o repositório ou copie o código para sua máquina.**

2. **Baixe o dataset Fruits 360 utilizando o Kaggle
     ```

3. **Configure o ambiente de execução:**
   - Execute o script em uma máquina com GPU disponível para melhores resultados.
   - O dispositivo será detectado automaticamente:
     ```python
     device = torch.device("cuda" if torch.cuda.is_available() else "cpu")
     ```

4. **Treinamento dos modelos:**
   - O treinamento é realizado para 10 épocas por padrão, com os DataLoaders configurados para treino, validação e teste.
   - Para treinar e avaliar os modelos, execute:
     ```python
     train_model(resnet18, train_loader, val_loader)
     evaluate_model(resnet18, test_loader)
     train_model(alexnet, train_loader, val_loader)
     evaluate_model(alexnet, test_loader)
     ```

5. **Visualize os resultados:**
   - Gráficos de perda e acurácia são gerados para análise do desempenho dos modelos:
     ```python
     plt.show()
     ```

6. **Saída esperada:**
   - Matrizes de confusão e relatórios de classificação serão exibidos no terminal, detalhando o desempenho de cada modelo.

---

## Estrutura do Projeto
- **Dataset:** Fruits 360 (automático via KaggleHub)
- **Modelos:** ResNet18 e AlexNet
- **Pré-processamento:**
  - Redimensionamento para 100x100 pixels.
  - Normalização no intervalo [-1, 1].
  - Aumento de dados com flips horizontais.
- **Métricas:** Precisão, recall, F1-score e matrizes de confusão.
- **Resultados:** Comparação detalhada do desempenho dos modelos.

---

## Resultados

### **ResNet18:**
- Alta precisão e baixa perda de validação.
- Melhor capacidade de generalização e diferenciação entre classes.

### **AlexNet:**
- Desempenho moderado, com mais erros em classes visualmente semelhantes.
- Útil em cenários com restrições computacionais.

