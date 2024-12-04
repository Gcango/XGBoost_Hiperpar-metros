# XGBoost_Hiperparâmetros
 

Predição de Preços de Venda de Carros com XGBoost


Este projeto tem como objetivo prever os preços de venda de carros utilizando o algoritmo XGBoost disºoniveis nos artigos (https://dl.acm.org/doi/abs/10.1145/2939672.2939785) e (https://www.sciencedirect.com/science/article/pii/S2215016123001206), amplamente reconhecido por sua eficiência em tarefas de aprendizado supervisionado. O desafio envolve desde o treinamento inicial do modelo até a otimização de hiperparâmetros, comparando diferentes estratégias de otimização para melhorar o desempenho preditivo.


Descrição do Projeto
Objetivo: Desenvolver um modelo preditivo eficiente para estimar preços de venda de carros com base em suas características.
Algoritmo Utilizado: XGBoost, implementado com a biblioteca Scikit-Learn.
Etapas Realizadas:
Divisão de Dados: O dataset foi dividido em:
75% para treinamento.
25% para testes.
Treinamento Inicial: Modelo XGBoost treinado com hiperparâmetros padrão para estabelecer uma linha de base.
Avaliação do Modelo:
RMSE (Root Mean Squared Error): Mede o erro absoluto médio.
R² (Coeficiente de Determinação): Mede o percentual de variância explicada pelo modelo.
Otimização de Hiperparâmetros:
Grid Search: Exploração exaustiva de combinações de max_depth, learning_rate, n_estimators e colsample_bytree.
Random Search: Seleção aleatória de combinações de hiperparâmetros, com 100 iterações.
Bayesian Optimization: Uso de métodos probabilísticos para otimizar max_depth, learning_rate e n_estimators, com 100 iterações.
Comparação de Resultados: Análise do impacto de cada estratégia de otimização.


Resultados Obtidos
Método	RMSE	R²	Observações
Sem Otimização	8800.31	0.7742	Desempenho inicial, com maior erro e menor R².
Grid Search	5062.828	0.9253	Melhor desempenho, mas com maior custo de tempo.
Random Search	5062.828	0.9253	Mesmo desempenho do Grid Search, mais eficiente.
Bayesian Optimization	6001.263	0.8861	Desempenho intermediário, com potencial de melhoria.


Conclusões
Melhor Desempenho: Grid Search e Random Search apresentaram resultados idênticos e superiores à otimização bayesiana.
Maior Eficiência: Random Search alcançou os mesmos resultados do Grid Search com menor custo computacional.
Otimização Bayesiana: Mostrou-se promissora, mas requer ajustes adicionais (e.g., maior número de iterações ou melhor definição do espaço de busca).


Repositório
Tecnologias Utilizadas:
Python
Bibliotecas: Scikit-Learn, XGBoost de Hipeparametro(Grid Search 
, Randomized Search e Bayesian Optimization)

Estrutura:
dataset/: Contém o conjunto de dados utilizado no projeto.
notebooks/: Scripts para análise exploratória, treinamento e otimização.
results/: Comparação de métricas.
