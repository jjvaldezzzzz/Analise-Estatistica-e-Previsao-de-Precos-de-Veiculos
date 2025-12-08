# Análise Estatística e Previsão de Preços de Veículos (CarDekho)

![Python](https://img.shields.io/badge/Python-3.12-blue)
![Status](https://img.shields.io/badge/Status-Concluído-success)
![License](https://img.shields.io/badge/License-MIT-green)

Este projeto aplica conceitos de Estatística Descritiva e Machine Learning para analisar o mercado de carros usados, utilizando o *Vehicle Dataset from CarDekho*. O objetivo é prever o preço de revenda de veículos e classificar o tipo de transmissão com base em características técnicas.

## 📋 Índice
- [Sobre o Projeto](#-sobre-o-projeto)
- [Objetivos](#-objetivos)
- [Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [Metodologia e Workflow](#-metodologia-e-workflow)
- [Resultados Alcançados](#-resultados-alcançados)
- [Como Executar](#-como-executar)
- [Autor](#-autor)

## 🧐 Sobre o Projeto
O projeto foi desenvolvido como parte de um requisito acadêmico para demonstrar proficiência em Python para Ciência de Dados. Ele aborda desde a limpeza de dados até a otimização de hiperparâmetros, enfrentando desafios reais de compatibilidade de versões (Python 3.12 vs PyCaret) e engenharia de features.

## 🎯 Objetivos
1.  **Análise Exploratória (EDA):** Identificar padrões de depreciação e correlações entre variáveis.
2.  **Regressão:** Desenvolver modelos (Linear, Múltiplo e Polinomial) para prever o `Selling_Price` (Preço de Venda).
3.  **Classificação:** Implementar modelos (Regressão Logística e Naive Bayes) para prever a `Transmission` (Manual vs Automático).
4.  **Otimização:** Ajustar hiperparâmetros para maximizar a performance do modelo.

## 🛠 Tecnologias Utilizadas
* **Linguagem:** Python 3.12
* **Manipulação de Dados:** Pandas, Numpy
* **Visualização:** Seaborn, Matplotlib
* **Machine Learning:** Scikit-Learn (Sklearn)
    * *Nota:* A biblioteca PyCaret foi substituída por `GridSearchCV` devido a incompatibilidades com o Python 3.12+, demonstrando adaptação técnica.

## ⚙️ Metodologia e Workflow

### 1. Preparação dos Dados
* Carregamento do dataset `car data.csv`.
* Padronização de nomes de colunas (Snake Case).
* Criação da feature `car_age` (2024 - Ano de Fabricação).
* Encoding de variáveis categóricas (`fuel`, `seller_type`, `transmission`).

### 2. Modelagem Preditiva
* **Regressão:** Comparação entre Regressão Linear Múltipla e Polinomial (focada na idade). O foco foi entender como `present_price` e `km_driven` impactam o valor final.
* **Classificação:** Uso de Regressão Logística e Gaussian Naive Bayes para inferir se um carro é automático baseado em seu preço e quilometragem.

### 3. Otimização
* Implementação de **Grid Search** com **Random Forest Regressor** para superar as limitações da Regressão Linear simples e capturar não-linearidades nos dados.

## 📊 Resultados Alcançados

| Modelo | Tarefa | Métrica Principal | Observação |
| :--- | :--- | :--- | :--- |
| **Regressão Linear Múltipla** | Prever Preço | **R² > 0.80** | Forte correlação linear com o Preço de Tabela. |
| **Regressão Logística** | Prever Transmissão | **Acurácia Alta** | Eficaz na distinção Manual/Automático. |
| **Random Forest (Tuned)** | Prever Preço | **Menor RMSE** | Melhor generalização para outliers. |

**Insights Principais:**
* A depreciação de veículos segue uma curva acentuada nos primeiros anos, validando o teste de regressão polinomial.
* Carros automáticos possuem um preço de revenda significativamente superior e quilometragem média distinta dos manuais.

## 🚀 Como Executar

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/SEU-USUARIO/NOME-DO-REPO.git](https://github.com/SEU-USUARIO/NOME-DO-REPO.git)
    ```
2.  **Instale as dependências:**
    ```bash
    pip install pandas numpy seaborn matplotlib scikit-learn
    ```
3.  **Execute o Notebook:**
    Abra o arquivo `.ipynb` no Jupyter Notebook, VS Code ou Google Colab.
    *Certifique-se de que o arquivo `car data.csv` esteja na mesma pasta.*

## 🧑‍💻 Autor

Desenvolvido por **[SEU NOME AQUI]**

[![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white)](LINK_DO_SEU_LINKEDIN)
[![Gmail Badge](https://img.shields.io/badge/-Gmail-c14438?style=flat-square&logo=Gmail&logoColor=white)](mailto:SEU_EMAIL@GMAIL.COM)
