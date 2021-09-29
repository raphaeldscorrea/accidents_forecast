
##Predição de acidentes em Recife

###Objetivo

Baseado nos registros de ocorrência de acidentes em Recife (2015-2019), criar um modelo de previsão de séries temporais. Para isso, os dados de 2015 à 2018 serão utilizados como treinamento do modelo. Já os dados de 2019 serão utilizados para validação do modelo aplicando-se a validação walk-foward.  


###Dados

O dataset é constituído de 5 arquivos .csv:

**acidentes-transito-2015.csv**: 7273 linhas x 24 colunas
**acidentes_2016.csv**: 11263 linhas x 47 colunas
**acidentes_2017.csv**: 11758 linhas x 32 colunas
**acidentes_2018.csv**: 11411 linhas x 45 colunas
**acidentes-2019.csv**: 12062 linhas x 47 colunas

Tais arquivo nos gera um total **53767** para serem analisados.


###Estacionariedade

Para análise da estacionariedade são utilizadas três abordagens diferentes, porém complementares:

1. Análise de tendência: verificação do gráfico de tendência da série decomposta (tendência, sazonalidade e resíduo)
2. Distribuição da série temporal: análise da série para verificar se a mesma possui um comportamento normal dos registros. 
3. Teste de hipótese Dickey-Fuller: teste de em que a hipótese nula afirma a presença de raíz unitária na série. Em caso de rejeição da hipótese nula, a série é tida como estacionária pois refuta a raíz unitária.

###Sazonalidade

Para análise da sazonalidade são utilizadas duas abordagens diferentes, porém complementares:

1. Análise gráfico boxplot: verificação da disperção dos dados a cada dia da semana
2. Análise de sazonalidade: verificação do gráfico de sazonalidade da série decomposta (tendência, sazonalidade e resíduo)

###Modelos

Em termos de modelos, são utilizadas quatro abordagens distintas:

1. ARIMA: derivações de modelos considerando auto-regressão, média móvel e diferenciação
2. SARIMA: aplicação de sazonalidade em modelos ARIMA. 
3. Holt Winters: aplicação de nível, tendência e sazonalidade para predição da série.
4. SARIMAX: aplicação de sazonalidade em modelos ARIMA com variáveis exógenas. 

###Análise dos modelos

Para análise da acurácia e performance do modelo, foi utilizados três métricas distintas:

1. RMSE: Raiz do Erro Quadrático Médio
2. MAE: Erro absoluto médio
3. BIC: Critério de informação Bayseano
