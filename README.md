# Visualização de Dados com Matplotlib

Este repositório contém a solução completa dos Exercícios 1 e 2 da atividade de Visualização de Dados com Matplotlib, utilizando o dataset **London Weather**.

Todo o código foi implementado em Python, com separação modular em scripts (`main.py`, `ler_csv.py`, `carregar_dados.py`, `analise_ultimos10.py`, `analise_primeiros10.py`, `grafico_bolhas.py` etc.). Além disso, cada etapa solicitada no enunciado está respondida e explicada.

---------------------------------------------------------------------------------

# Exercício 1

## **1. Carregamento do Dataset**

O dataset foi carregado diretamente para um DataFrame Pandas usando `pd.read_csv()` com os parâmetros corretos de encoding e separador.

Link do dataset utilizado:

```
https://github.com/alanjones2/dataviz/raw/master/londonweather.csv
```

## **2. Visualização inicial dos dados**

Após o carregamento, foram exibidas:

* As primeiras linhas do DataFrame
* Tipos de dados com `df.dtypes`
* Memória usada com `df.memory_usage()`

Essa etapa permite compreender colunas, formatos e possíveis conversões necessárias.

---------------------------------------------------------------------------------

## **3. Seleção dos últimos 10 anos**

* O último ano encontrado no dataset foi identificado com:
  `df["Year"].max()`
* A partir dele, os **10 anos anteriores** foram selecionados usando `between()`.

### **a. Último ano do dataset**

O último ano registrado no dataset é **2019**.

### **b. Os 10 anos anteriores**

Intervalo resultante da filtragem: **2010 a 2019**.

---------------------------------------------------------------------------------

## **4. Gráfico de séries sobreposto (Tmax dos últimos 10 anos)**

Foi construído um gráfico de linha onde:

* Cada ano possui uma **cor diferente**.
* Cada ano possui um **marcador diferente**.
* O eixo X representa os meses (1 a 12).
* O eixo Y representa a temperatura máxima.

O gráfico permite comparar visualmente a evolução anual da temperatura.

---------------------------------------------------------------------------------

### **6a. Existe tendência de aumento ou diminuição da temperatura máxima?**

Com base nos cálculos e no gráfico:

Sim, existe tendência de aumento, porque a média de `Tmax` do último ano (2019) está acima da média do primeiro ano do intervalo (2010).

### **6b. O gráfico sugere aquecimento global?**

Sim, porque as temperaturas máximas anuais mostram um crescimento gradual ao longo dos 10 anos.

### **6c. Mês/Ano mais quente no período analisado**

O pico de temperatura ocorreu em:

* **Ano:** 2018
* **Mês:** 7 (Julho)
* **Temperatura máxima:** **34.5°C**

Esse valor foi obtido usando:
`dados10.loc[dados10["Tmax"].idxmax()]`

---------------------------------------------------------------------------------

## **7. Gráfico com anotação do pico de temperatura**

Foi adicionado ao gráfico:

* Uma **seta (annotate)** destacando o ponto mais quente
* A mensagem: "34.5°C é a maior temperatura registrada nos últimos 10 anos"

O valor é automaticamente formatado com `f"{tmax_valor:.1f}°C"`.

---------------------------------------------------------------------------------

#  Exercício 2 — Gráfico de Bolhas

## **1. Gráfico de bolhas com todos os anos (1957–2019)**

Foi construído um gráfico onde:

* Eixo X = meses (1 a 12)
* Eixo Y = temperatura máxima
* O tamanho da bolha representa o valor da temperatura (`Tmax * 10`)
* Cada bolha representa um mês de um ano

---------------------------------------------------------------------------------

## **2. Existe um período mais quente no ano?**

Sim, apenas observando o gráfico é possível identificar.

Justificativa:

* A maior concentração de bolhas grandes ocorre entre **junho e agosto**.
* Isso indica que os meses **6, 7 e 8** são os mais quentes ao longo de todos os anos.

---------------------------------------------------------------------------------
