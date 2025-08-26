# desafio-caed-data-mining

# Principais Etapas
1. Exploração e Limpeza dos Dados
- Remoção de duplicatas e registros irrelevantes
- Tratamento de outliers em ano de produção (year)
- Normalização de variáveis numéricas (views, year)
- Limpeza textual das letras
- Padronização de nomes de artistas e colaboradores
- Amostragem balanceada por gênero musical
2. Rede de Colaboração de Artistas
- Construção de grafo não direcionado com artistas e colaborações
- Filtragem por popularidade e top 20% de visualizações
- Detecção de comunidades via algoritmo de Louvain
- Métricas: centralidades, modularidade, comprimento médio de caminho
- Visualização e análise de comunidades
3. Geração de Letras de Música
- Fine-tuning de modelo GPT-2
- Tokenização em janelas de 128 tokens
- Avaliação com perplexidade
- Experimentos com subconjuntos balanceados e com restrição a um gênero
4. Predição de Gênero Musical
- Representação TF-IDF (unigramas, bigramas, trigramas)
- Modelos de classificação: Regressão Logística, Random Forest
- Avaliação com acurácia, precisão, recall, F1-score
5. Análise de Polaridade
- Uso de TextBlob para cálculo de polaridade (-1 a 1)
- Análise de evolução temporal do sentimento por artista
- Relação entre polaridade e popularidade (views)
- Identificação de artistas com maior variação emocional ao longo do tempo
# Como Executar
Requisitos
- Python 3.x
- Bibliotecas: pandas, numpy, matplotlib, seaborn, scikit-learn, networkx, textblob, transformers
# Resultados
- Rede de colaboração revelou comunidades bem conectadas, com modularidade Louvain > 0.5
- Geração de letras apresentou perplexidade inicial ~37, reduzida para ~25 ao restringir a um gênero
- Predição de gênero musical alcançou ~64% de acurácia (Random Forest e Regressão Logística)
- Análise de polaridade evidenciou evolução emocional de artistas como Kanye West e variação de senti
# Referências
- Notas de aula da disciplina Mineração de Dados - DCC127 (UFJF, 2025)
- Relatório do desafio Edital 015/2025 (CAEd)