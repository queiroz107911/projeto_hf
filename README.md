# Análise Exploratória de Dados (EDA) — Dataset de Emendas Parlamentares

## Descrição

Este exercício tem como objetivo aplicar comandos básicos da biblioteca **pandas** para realizar uma **Análise Exploratória de Dados (EDA)** em um dataset de emendas parlamentares.

Foram utilizadas operações simples para entender a estrutura da base de dados, identificar possíveis problemas e extrair informações iniciais.

## Dataset

O dataset utilizado contém informações sobre **emendas parlamentares**, incluindo dados do autor, localidade de aplicação do recurso, função orçamentária e valores financeiros relacionados às emendas.

A base possui:

* **88.596 linhas**
* **28 colunas**

## Etapas da análise

### 1. Carregamento dos dados

O dataset foi carregado utilizando `pandas.read_csv()` e as **10 primeiras linhas** foram exibidas para visualizar a estrutura inicial da base.

### 2. Dimensão do dataset

Foi utilizado `df.shape` para identificar a quantidade de **linhas e colunas**.

### 3. Estrutura das colunas

Foram listadas todas as colunas com `df.columns` e realizada uma breve descrição do significado de cada uma.

### 4. Verificação de valores nulos

Foi utilizado `df.isnull().sum()` para verificar se existiam valores ausentes na base.

Resultado: **não foram encontrados valores nulos**.

### 5. Tipos das variáveis

Utilizando `df.dtypes`, foram analisados os tipos de dados de cada coluna.

Observações:

* A coluna **Ano da Emenda** poderia estar em formato de data.
* A coluna **Código UF IBGE** poderia ser armazenada como string.

### 6. Atualização do dataset

Ordenando o dataframe pela coluna **Ano da Emenda** de forma decrescente, foi possível identificar que a base está atualizada até **2025**.

### 7. Estatísticas descritivas

Foi executado `df.describe()` para visualizar estatísticas básicas das colunas numéricas.

Observação:
Colunas do tipo **object/string** não aparecem nesse resumo estatístico, pois o método analisa apenas variáveis numéricas.

### 8. Últimas linhas do dataset

Com `df.tail()` foram exibidas as **5 últimas linhas**, indicando que a última linha aparenta estar **completa e sem valores ausentes**.

### 9. Verificação de duplicatas

Foi utilizado `df.duplicated().sum()` para identificar registros duplicados.

Resultado: **não foram encontrados registros duplicados**.

## Conclusão

A base de dados apresenta uma estrutura organizada, sem valores nulos ou duplicados. A análise inicial permitiu compreender melhor os tipos de dados e a atualização do dataset, servindo como primeiro passo para análises mais aprofundadas.
