#  Análise de Anúncios e Avaliações de Propriedades (Airbnb)

Este projeto tem como objetivo realizar a limpeza, tratamento e análise exploratória de dados relacionados a anúncios de propriedades e avaliações de hóspedes, com foco em preparar um dataset limpo, consistente e pronto para modelagem ou geração de insights estratégicos.

O trabalho foi desenvolvido utilizando Python e bibliotecas de análise de dados, seguindo boas práticas de Data Analysis e Data Preparation.

---

##  Conjunto de Dados

O projeto utiliza dois datasets principais:

### Listings (Anúncios de Propriedades)

| Coluna | Descrição |
|------|---------|
| `id` | Identificador único do imóvel |
| `neighbourhood_cleansed` | Bairro onde o imóvel está localizado |
| `room_type` | Tipo de acomodação |
| `accommodates` | Número máximo de hóspedes |
| `bathrooms` | Quantidade de banheiros |
| `bedrooms` | Número de quartos |
| `beds` | Número de camas |
| `price` | Preço da diária |

---

### Reviews (Avaliações)

| Coluna | Descrição |
|------|---------|
| `id` | Identificador do imóvel |
| `number_of_reviews` | Total de avaliações |
| `review_scores_rating` | Nota média dos hóspedes |

---

##  Objetivo do Projeto

- Consolidar dados de anúncios e avaliações
- Garantir qualidade e consistência dos dados
- Identificar e tratar outliers
- Transformar variáveis categóricas
- Preparar o dataset para análises futuras ou modelos de Machine Learning
- Gerar insights que auxiliem anfitriões na tomada de decisão

---

##  Tecnologias Utilizadas

- **Python 3**
- **Pandas**
- **Matplotlib**
- **Seaborn**
- **Jupyter Notebook**

---

## Etapas do Desenvolvimento

###  Etapa 01 — Carregamento dos Dados
- Importação dos arquivos CSV
- Inspeção inicial com `.head()` e `.info()`
- União dos datasets utilizando `pd.merge()` com chave `id`

---

###  Etapa 02 — Limpeza e Tratamento
- Verificação de valores ausentes com `isnull().sum()`
- O dataset já se encontrava **sem valores nulos**, não sendo necessário tratamento adicional nesta etapa
- Conferência e validação de tipos de dados

---

###  Etapa 03 — Tratamento de Outliers
- Identificação de outliers na variável `price` utilizando boxplot
- Aplicação do método **IQR (Intervalo Interquartil)**
- Remoção de registros fora dos limites aceitáveis

---

###  Etapa 04 — Transformação de Dados Categóricos
- Conversão de variáveis categóricas (`room_type`, `neighbourhood_cleansed`) para valores numéricos
- Utilização de `astype('category').cat.codes`
- Remoção das colunas categóricas originais

---

###  Etapa 05 — Conferência Final
- Verificação da integridade do dataset
- Análise estatística com `describe()`
- Conferência de colunas e tipos de dados
- Dataset final pronto para modelagem ou análises avançadas

---

##  Resultados Esperados

- Dataset limpo, padronizado e consistente
- Redução de distorções causadas por outliers
- Base pronta para:
  - Análises exploratórias
  - Modelos preditivos
  - Geração de insights para anfitriões

---
