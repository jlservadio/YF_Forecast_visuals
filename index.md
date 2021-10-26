---
title: "Yellow Fever Forecasts for Brazil"
output: 
  html_document:
    keep_md: true
---




This page shows predictions of future burden, or forecasts, of Yellow Fever across all municipalities of Brazil. 

## Forecast creation

The forecasts created in this document were generated form a statistical model developed through a letter of agreement from the Pan American Health Organization. The model form is a Gamma hurdle model, a two-stage model that produces two forecasted values:

  1. Probability of observing any Yellow Fever cases
  2. Estimated number of cases per 100,000 population under the condition that any cases are seen. 
  
The model uses environmental conditions to produce forecasts for eevery week. The forecasted probability of seeing any Yellow Fever cases uses, as predictors: average temperature two weeks prior, calendar month, previous occurrence of Yellow Fever two weeks prior, and World Wildlife Foundation ecoregions. The forecasted incidence of Yellow Fever, conditioned on seeing any Yellow Fever cases, uses, as predictors: minimum rainfall seven weeks prior, minimum humidity seven weeks prior, previous occurrence of Yellow Fever seven weeks prior, and drainage density. 

The environmental predictors in this model were selected based on forecasting accuracy using weekly Yellow Fever case data collected between December 2016 and March 2018. Model fit was established using data from November 2016 through December 2017, and forecasts of Yellow Fever between January 2018 and March 2018 were compared to observed incidence to assess accuracy of forecasts. 

This model fitting process was also applied to data between January 2000 and November 2016. The results from this model fitting are not used for the forecasts presented here because they represent the time period prior to the recent epidemic. Complete details regarding the model fitting process are currently being prepared for publiction. 

## Yellow Fever forecasts for the week of 2-8 April, 2018

### Probability of observing any Yellow Fever cases

Forecasted probabilities of Yellow Fever occurrence for each municipality were produced using information from the week of 19-25 March, 2018.

![](index_files/figure-html/unnamed-chunk-2-1.png)<!-- -->

### Estimated incidence of Yellow Fever if any cases are observed

Forecasted incidences of Yellow Fever fore each municipality were produced using information from the week of 12-18 February, 2018. The forecasted incidences were estimated separately form the forecasted probabilities of occurrence, so forecasted incidence values are produced even when the probability of occurrence is very low. 

![](index_files/figure-html/unnamed-chunk-3-1.png)<!-- -->

## Interpretation of results

The first map shows a forecasted probability that any Yellow Fever cases will occur. If Yellow Fever cases were to occur, the second map shows the forecasted number of cases per 100,000 population. 

### The following municipalities have the highest predicted probability of Yellow Fever occurrence:


```
##                          Municipality Probability
## 1           Rio Claro, Rio de Janeiro        0.51
## 2                    Aruja, São Paulo        0.51
## 3    São João da Boa Vista, São Paulo        0.51
## 4       Barão de Cocais, Minas Gerais        0.50
## 5        Belo Horizonte, Minas Gerais        0.50
## 6             Belo Vale, Minas Gerais        0.50
## 7            Brumadinho, Minas Gerais        0.50
## 8                 Caeté, Minas Gerais        0.50
## 9              Carandaí, Minas Gerais        0.50
## 10            Congonhas, Minas Gerais        0.50
## 11 Conselheiro Lafaiete, Minas Gerais        0.50
## 12           Consolação, Minas Gerais        0.50
## 13 Diogo de Vasconcelos, Minas Gerais        0.50
## 14              Guarani, Minas Gerais        0.50
## 15              Itabira, Minas Gerais        0.50
## 16            Itabirito, Minas Gerais        0.50
## 17            Itaverava, Minas Gerais        0.50
## 18       João Monlevade, Minas Gerais        0.50
## 19         Juiz de Fora, Minas Gerais        0.50
## 20        Lagoa dourada, Minas Gerais        0.50
```

### If any Yellow Fever cases occur, the following municipalities have the highest forecasted incidence:


```
##                                 Municipality Incidence
## 1                     Laguna, Santa Catarina    420.15
## 2          Capivari de Baixo, Santa Catarina    416.70
## 3                Simão Pereira, Minas Gerais    231.38
## 4  Comendador Levy Gasparian, Rio de Janeiro    156.51
## 5                    Alpercata, Minas Gerais    116.92
## 6              Derrubadas, Rio Grande do Sul    104.48
## 7            Alto Bela Vista, Santa Catarina     66.87
## 8                      Chiador, Minas Gerais     65.82
## 9             Formosa do Sul, Santa Catarina     57.57
## 10       Barra do Guarita, Rio Grande do Sul     48.97
## 11           Coronel Freitas, Santa Catarina     47.31
## 12                  Piratuba, Santa Catarina     47.29
## 13                 Tunápolis, Santa Catarina     45.01
## 14                  Quilombo, Santa Catarina     42.23
## 15                      Campo Bonito, Paraná     41.53
## 16                          Contenda, Paraná     37.72
## 17               Belmiro Braga, Minas Gerais     37.40
## 18                         Araucária, Paraná     37.17
## 19                            Ouvidor, Goiás     37.16
## 20              São José dos Pinhais, Paraná     36.30
```



