# Análise de Vendas de E-commerce com Machine Learning

Este projeto tem como objetivo analisar dados de vendas de um e-commerce, extraindo insights com estatística básica e prevendo vendas futuras com modelos de Machine Learning.

## Principais Passos
1. **Limpeza de Dados**: Remoção de NAs e duplicatas.
2. **EDA**: Vendas mensais têm pico em novembro (Black Friday?).  
3. **Teste Estatístico**: Vendas no Reino Unido são significativamente maiores que na Alemanha (p-value < 0.05).  
4. **Modelagem**: Regressão Linear(RMSE = 426.43 vs. 303.10 do Random Forest).

## Dataset
O arquivo `ecommerce-data` está disponível na pasta `data/`.

## Como Reproduzir
- Execute o Jupyter Notebook `ecommerce-data` ou o script Python.