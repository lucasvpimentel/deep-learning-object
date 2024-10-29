# Fine-Tuning de Modelo Pré-Treinado com Aumento de Dados

Este projeto realiza o treinamento de um modelo de rede neural convolucional (CNN) usando uma base pré-treinada (VGG16) para classificar imagens em duas categorias. Utilizamos técnicas de **fine-tuning** e **aumento de dados** para melhorar a generalização do modelo.

## Estrutura do Projeto

- **`train_images`**: Conjunto de imagens de treinamento.
- **`train_labels`**: Labels correspondentes às imagens de treinamento.
- **`test_images`**: Conjunto de imagens para validação.
- **`test_labels`**: Labels correspondentes às imagens de validação.
- **`model`**: Arquitetura do modelo CNN com base pré-treinada (VGG16) e camadas personalizadas no topo.
- **`train_datagen_augmented`**: Gerador de dados com aumento, usado para gerar novas variações de imagens em tempo real.

## Funcionalidades

- **Fine-Tuning de Camadas Finais**: Congelamos as camadas iniciais da base convolucional para preservar as características genéricas (bordas, texturas) e ajustamos as camadas finais para o problema específico.
- **Aumento de Dados**: Utilizamos o `ImageDataGenerator` para aplicar transformações aleatórias (rotações, deslocamentos, zoom, etc.) nas imagens de treinamento, gerando variações que ajudam a evitar overfitting.

## Configuração

### Dependências

- `tensorflow` (>= 2.x)
- `numpy`
- `matplotlib` (opcional, para visualização)

Instale as dependências com:

```bash
pip install tensorflow numpy matplotlib
