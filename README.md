# **Classificação de Imagens com Redes Convolucionais (CNN)**

## **Descrição do Projeto**

Este projeto visa implementar e avaliar modelos de redes neurais convolucionais (CNNs) para a tarefa de **classificação de imagens**. O dataset utilizado, "CUHK Face Sketch Database (CUFS)", contém imagens de rostos humanos, e o objetivo é classificar essas imagens como **Masculino** ou **Feminino**. O projeto envolve desde o preparo dos dados, a construção de um modelo CNN autoral, até a avaliação dos resultados com métricas de desempenho como **F1-Score**, **AUC-ROC** e **curva ROC**.

---

## **Objetivo**

O objetivo deste projeto é construir e treinar uma rede neural convolucional (CNN) para classificar imagens de rostos de pessoas em duas categorias: **Masculino** e **Feminino**. Durante o desenvolvimento, serão abordadas as etapas de **preparo de dados**, **treinamento do modelo** e **análise dos resultados**. O desempenho do modelo será avaliado utilizando métricas como **Acurácia**, **F1-Score**, **AUC-ROC**, entre outras.

---

## **Como Executar o Projeto**

Siga as instruções abaixo para configurar e rodar o projeto localmente:

### 1. **Clone o Repositório**

Clone este repositório utilizando o comando:
```bash
git clone <URL_do_repositório>
```

### 2. **Acesse o Diretório do Projeto**

Entre no diretório do repositório:
```bash
cd <diretório_do_repositório>
```

### 3. **Crie um Ambiente Virtual**

Crie e ative um ambiente virtual para isolar as dependências:
```bash
python -m venv venv
```

Ative o ambiente virtual:

- **No Windows**:  
  ```bash
  .\venv\Scripts\activate
  ```

- **No macOS/Linux**:  
  ```bash
  source venv/bin/activate
  ```

### 4. **Instale as Dependências**

Com o ambiente virtual ativado, instale as bibliotecas necessárias:
```bash
pip install -r requirements.txt
```

---

## **Passos para Executar o Código**

### 1. **Prepare o Dataset**

O dataset utilizado, "CUHK Face Sketch Database (CUFS)", contém 188 imagens. Após carregar as imagens, o código realiza a anotação das imagens (0 para **Masculino** e 1 para **Feminino**) e ajusta as imagens para o tamanho de **250x200 pixels**, além de normalizá-las no intervalo [0, 1].

### 2. **Divida o Dataset**

O conjunto de dados é dividido em 3 partes:  
- **50% para Treinamento**
- **30% para Validação**
- **20% para Teste**

A divisão é feita de forma aleatória, mas utilizando a semente `23` para garantir reprodutibilidade.

### 3. **Treinamento do Modelo**

Uma rede neural convolucional (CNN) é construída para a tarefa de classificação. O modelo utiliza 3 camadas convolucionais (`Conv2D`), camadas de pooling (`MaxPooling2D`), camadas de regularização (`Dropout`), e camadas densas (`Dense`). O modelo é compilado usando o **otimizador Adam** e a **função de perda categorical_crossentropy**.

### 4. **Avaliação do Modelo**

Após o treinamento, o modelo é avaliado no conjunto de teste. As métricas de desempenho incluem:
- **Acurácia**
- **F1-Score**
- **AUC-ROC**
- **Curva ROC**
- **Matriz de Confusão**

### 5. **Resultados**

Os resultados serão apresentados em forma de gráficos (como a curva ROC) e tabelas (como o relatório de classificação), permitindo uma análise detalhada sobre o desempenho do modelo.

---

## **Tecnologias Utilizadas**

Este projeto foi desenvolvido utilizando as seguintes tecnologias e bibliotecas:

- **Python**: Linguagem principal utilizada para a implementação do modelo CNN e manipulação dos dados.
- **TensorFlow / Keras**: Frameworks para construção e treinamento da rede neural convolucional (CNN).
- **Pandas**: Biblioteca para manipulação e análise dos dados.
- **NumPy**: Biblioteca para manipulação de arrays e operações matemáticas.
- **Scikit-learn**: Framework para avaliação do modelo, incluindo métricas como F1-Score, AUC-ROC e geração da matriz de confusão.
- **Matplotlib** e **Seaborn**: Bibliotecas para visualização de dados e criação de gráficos (curvas ROC, matriz de confusão).
- **OpenCV**: Biblioteca para carregamento e processamento de imagens.

---


## **Análise dos Resultados**

Após a execução do código, o modelo será avaliado com base nas métricas de desempenho:

- **Acurácia**: Proporção de classificações corretas no conjunto de teste.
- **F1-Score**: Métrica de equilíbrio entre precisão e recall.
- **AUC-ROC**: Área sob a curva ROC, uma medida de desempenho do modelo para classificação binária.
- **Curva ROC**: Gráfico que ilustra a relação entre a taxa de verdadeiros positivos e falsos positivos.

Além disso, será gerada uma **matriz de confusão**, que permitirá observar os erros cometidos pelo modelo na classificação das imagens.

---

## **Exemplos de Visualizações**

- **Curva ROC**: Visualiza o desempenho do modelo no conjunto de teste.
- **Matriz de Confusão**: Exibe a quantidade de acertos e erros para cada classe (Masculino e Feminino).

---

## **Autores e Colaboradores**

Este projeto foi desenvolvido por:

- **Gabriel Marçal**
- **Leon Santana**
