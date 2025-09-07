# Visão Geral Técnica do Projeto

Resumo técnico do projeto, incluindo a metodologia utilizada e um dicionário de dados completo das variáveis presentes no dataset final.

## Metodologia

Decidi estruturar o projeto utilizando o framework **CRISP-DM**, seguindo 6 fases principais:
1.  **Entendimento do Negócio:** Definição dos objetivos e das perguntas a serem respondidas para o estúdio "PProductions".
2.  **Entendimento dos Dados:** Analise exploratória inicial para entender a estrutura, qualidade e características dos dados brutos.
3.  **Preparação dos Dados:** Etapa intensiva de limpeza, tratamento de valores ausentes, engenharia de variáveis e processamento de texto.
4.  **Modelagem:** Construção e otimização de modelos preditivos para Faturamento e Nota IMDB.
5.  **Avaliação:** Análise de performance dos modelos utilizando métricas estatísticas (R², MAE, RMSE).
6.  **Entrega (Deployment):** Consolidação dos resultados em relatórios, documentação e uma aplicação web interativa.

## Dicionário de Dados Completo

#### Colunas Originais do Dataset

* **Series_Title**: O nome do filme.
* **Released_Year**: O ano de lançamento do filme.
* **Certificate**: A classificação etária indicativa.
* **Runtime**: A duração do filme em minutos.
* **Genre**: A string original contendo um ou mais gêneros.
* **IMDB_Rating**: A nota média do filme no site IMDB (variável alvo).
* **Overview**: A sinopse textual do filme.
* **Meta_score**: A nota da crítica especializada.
* **Director**: O diretor do filme.
* **Star1, Star2, Star3, Star4**: Os atores principais.
* **No_of_Votes**: O número de votos que o filme recebeu no IMDB.
* **Gross**: O faturamento bruto de bilheteria (em dólares).

#### Colunas Criadas (Engenharia de Variáveis)

* **Main_Genre**: O primeiro gênero listado na coluna `Genre`, usado para análises mais simples.
* **Director_clean**: Categoria do diretor ("Top 20" ou "Outro"), usada para medir a popularidade.
* **Movie_Age**: Idade do filme a partir do ano de lançamento.
* **Overview_clean**: Versão da sinopse com texto limpo (minúsculas, sem pontuação ou stopwords).
* **[Genre_*]** (ex: `Genre_Action`, `Genre_Drama`): Conjunto de colunas binárias (0 ou 1) indicando a presença de cada gênero no filme (one-hot encoding).
* **[Action, Drama, ...]**: Conjunto alternativo de colunas binárias de genero (one-hot encoding) criadas durante o pré-processamento.