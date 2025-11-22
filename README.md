# Visualização de Dados com Matplotlib

Este repositório contém a solução completa dos Exercícios 1 e 2 da atividade de Visualização de Dados utilizando Pandas e Matplotlib, totalmente desenvolvida dentro de um Google Colab Notebook.

Todos os passos solicitados no enunciado foram implementados diretamente no Colab, incluindo carregamento dos dados, visualização, análise e geração de gráficos.

---------------------------------------------------------------------------------

# Exercício 1

## **1. Carregamento do Dataset**

O dataset foi carregado diretamente para um DataFrame Pandas usando 'from google.colab import files' com os parâmetros corretos de encoding e separador.

Link do dataset utilizado:

```
https://github.com/alanjones2/dataviz/raw/master/londonweather.csv
```

## **3. Seleção dos últimos 10 anos**

### **a. Último ano do dataset**

O último ano registrado no dataset é **2019**.

### **b. Os 10 anos anteriores**

Intervalo resultante da filtragem: **2010 a 2019**.

---------------------------------------------------------------------------------

### **6a. Existe tendência de aumento ou diminuição da temperatura máxima?**

Com base nos cálculos e no gráfico:

Sim, existe tendência de aumento, porque a média de `Tmax` do último ano (2019) está acima da média do primeiro ano do intervalo (2010).

### **6b. O gráfico sugere aquecimento global?**

Sim, porque as temperaturas máximas anuais mostram um crescimento gradual ao longo dos 10 anos.

### **6c. Mês/Ano mais quente no período analisado:**

O pico de temperatura ocorreu em:

* **Ano:** 2018
* **Mês:** 7 (Julho)
* **Temperatura máxima:** **34.5°C**

---------------------------------------------------------------------------------

#  Exercício 2 — Gráfico de Bolhas

## **2. Existe um período mais quente no ano?**

Sim, apenas observando o gráfico é possível identificar.

* A maior concentração de bolhas grandes ocorre entre **junho e agosto**.
* Isso indica que os meses **6, 7 e 8** são os mais quentes ao longo de todos os anos.

---------------------------------------------------------------------------------
