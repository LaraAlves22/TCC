# 🩺 Classificação de Lesões de Pele com Deep Learning

Projeto de pesquisa que compara modelos de Deep Learning para classificação de lesões dermatológicas utilizando o dataset HAM10000.

## 📖 Visão Geral

Este projeto implementa e avalia duas arquiteturas de redes neurais para classificação de imagens de lesões de pele:

- 🧠 DenseNet201 (CNN)
- 👁️ Vision Transformer (ViT)

Além da comparação de desempenho, o trabalho inclui técnicas de interpretabilidade para análise das regiões da imagem utilizadas pelos modelos durante a classificação.

---

## 🎯 Objetivos

- Classificar lesões de pele em múltiplas categorias.
- Comparar o desempenho de CNNs e Transformers.
- Avaliar métricas clínicas relevantes.
- Aplicar técnicas de Explainable AI (XAI).
- Comparar mapas de ativação com máscaras ground truth.

---

## 📂 Dataset

### HAM10000

O conjunto de dados HAM10000 contém imagens dermatoscópicas de lesões de pele distribuídas em diferentes categorias diagnósticas.

Fonte:

- Dataset: https://www.kaggle.com/datasets/kmader/skin-cancer-mnist-ham10000

Download realizado via Kaggle API.

---

## 🏗️ Arquitetura do Projeto

```text
TCC_HAM10000.ipynb
│
├── Download do Dataset
├── Organização das Classes
├── Split Treino/Validação
├── Data Augmentation
├── Treinamento DenseNet201
├── Treinamento Vision Transformer
├── Avaliação de Métricas
├── Curvas de Aprendizado
├── Grad-CAM
├── Attention Rollout
├── Comparação Visual
└── Avaliação IoU com Máscaras Ground Truth
```

---

## 🔬 Modelos Utilizados

### DenseNet201

Rede convolucional profunda pré-treinada no ImageNet.

Características:

- Transfer Learning
- Fine-tuning
- Extração hierárquica de características

### Vision Transformer (ViT)

Modelo Transformer especializado para imagens.

Características:

- Self-Attention
- Pré-treinamento em imagens dermatológicas
- Attention Rollout para interpretabilidade

---

## 🧪 Pré-processamento

- Redimensionamento das imagens
- Normalização com estatísticas do ImageNet
- Data Augmentation
- Balanceamento das classes
- Divisão treino/validação

---

## 📊 Métricas Avaliadas

O projeto calcula:

- Accuracy
- Precision
- Recall
- F1-Score
- Sensibilidade
- Matriz de Confusão
- Intersection over Union (IoU)

---

## 🔍 Interpretabilidade

### Grad-CAM

Aplicado ao modelo DenseNet201 para destacar regiões relevantes da imagem durante a classificação.

### Attention Rollout

Aplicado ao Vision Transformer para visualizar o fluxo de atenção entre os patches da imagem.

---

## 📈 Análises Realizadas

- Curvas de treinamento
- Curvas de validação
- Comparação visual entre Grad-CAM e Attention Rollout
- Boxplots estatísticos
- Avaliação quantitativa dos mapas de atenção
- Comparação com máscaras ground truth do ISIC 2018

---

## ⚙️ Tecnologias Utilizadas

- Python
- PyTorch
- Torchvision
- Hugging Face Transformers
- OpenCV
- NumPy
- Pandas
- Matplotlib
- Scikit-Learn
- Kaggle API

---

## 🚀 Como Executar

### Instalar dependências

```bash
pip install torch torchvision transformers
pip install opencv-python scikit-learn matplotlib pandas
pip install kaggle kagglehub
```

### Configurar Kaggle API

1. Acesse sua conta Kaggle.
2. Vá em **Settings → API**.
3. Clique em **Create New Token**.
4. Faça upload do arquivo `kaggle.json`.

### Executar o notebook

```bash
jupyter notebook TCC_HAM10000.ipynb
```

ou

```bash
Google Colab
```

---

## 📋 Resultados Esperados

- Comparação entre CNN e ViT na classificação de lesões de pele.
- Avaliação quantitativa de desempenho.
- Análise visual da explicabilidade dos modelos.
- Comparação dos mapas gerados com máscaras de referência.

---

## 👩‍💻 Autoria

Projeto desenvolvido como Trabalho de Conclusão de Curso (TCC) na área de Ciência da Computação aplicada ao diagnóstico dermatológico.

---

## 📄 Licença

Projeto desenvolvido para fins acadêmicos e de pesquisa.
