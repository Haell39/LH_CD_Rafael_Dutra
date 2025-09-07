# Resultados da Modelagem Preditiva

Para transformar os insights da análise em ferramentas preditivas, foram desenvolvidos modelos de Machine Learning com foco em duas áreas críticas: a identificação dos **fatores de faturamento** e a **previsão da nota do público (IMDB Rating)**.

### **Fatores do Faturamento**

Fiz um modelo preditivo que tem um ótimo desempenho para o faturamento. Fazendo uma análise de importancia das features, percebe-se uma clara hierarquia se formando e indicando os fatores de sucesso:

1.  **Gênero do filme**: o genero "aventura" é o fator de maior impacto preditivo.
2.  **Popularidade (No_of_Votes)**: O engajamento do público é um fator também fundamental para o faturamento.
3.  **Idade do Filme (Movie_Age)**: Filmes mais recentes tendem a performar melhor financeiramente do que aqueles mais antigos.

**Recomendação Estratégica:** A combinação de um filme de **Aventura** com uma forte campanha de marketing para gerar popularidade massiva é a fórmula certeira com maior potencial de retorno financeiro.

### **Previsão de Nota IMDB**

Desenvolvi um modelo para prever a recepção de um filme pelo público, alcançando um resultado de alta precisão:

* **Poder Explicativo de 63% (R²):** O modelo explica 63.1% da variação nas notas do IMDB, validando sua robustez.
* **Erro Médio de Apenas 0.14 pontos:** Em uma escala de 1 a 10, o modelo prevê a nota final com uma margem de erro mínima.

**Aplicação de Negócio:** Este modelo (modelo_nota_imdb.pkl) pode ser usado internamente como uma ferramenta de "quality check" para avaliar o potencial de recepção de um projeto em fase de desenvolvimento, guiando decisões criativas e de investimento.