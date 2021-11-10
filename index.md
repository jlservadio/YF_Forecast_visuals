---
title: "Yellow Fever Forecasts for Brazil"
output: 
  html_document:
    keep_md: true
---




This page shows predictions of future burden, or forecasts, of Yellow Fever across all municipalities of Brazil. 

## Forecast creation

The forecasts created in this document were generated from a statistical model developed through a letter of agreement from the Pan American Health Organization. The model form is a Gamma hurdle model, a two-stage model that produces two forecasted values:

  1. Probability of observing any Yellow Fever cases
  2. Estimated number of cases per 100,000 population under the condition that any cases are seen. 
  
The model uses environmental conditions to produce forecasts for eevery week. The forecasted probability of seeing any Yellow Fever cases uses, as predictors: average temperature two weeks prior, calendar month, previous occurrence of Yellow Fever two weeks prior, and World Wildlife Foundation ecoregions. The forecasted incidence of Yellow Fever, conditioned on seeing any Yellow Fever cases, uses, as predictors: minimum rainfall seven weeks prior, minimum humidity seven weeks prior, previous occurrence of Yellow Fever seven weeks prior, and drainage density. 

The environmental predictors in this model were selected based on forecasting accuracy using weekly Yellow Fever case data collected between December 2016 and March 2018. Model fit was established using data from November 2016 through December 2017, and forecasts of Yellow Fever between January 2018 and March 2018 were compared to observed incidence to assess accuracy of forecasts. 

This model fitting process was also applied to data between January 2000 and November 2016. The results from this model fitting are not used for the forecasts presented here because they represent the time period prior to the recent epidemic. Complete details regarding the model fitting process are currently being prepared for publication.

Predicted probability of Yellow Fever occurrence in each municipality is defined as

$logit^{-1}(Pr(YF\hspace{2mm}Occurrence)) = -7.576 - (0.038 \times MeanTemperature) \\ - (0.876 \times Feb) - (0.897 \times Mar) - (1.278 \times Apr) - (3.257 \times May) \\ - (4.679 \times Jun) - (4.309 \times Jul) - (4.707 \times Aug) - (4.670 \times Sep) \\ - (4.670 \times Oct) - (3.925 \times Nov) - (1.187 \times Dec) \\ + (3.006 \times Previous YF) + (0.718 \times Ecoregion)$

where $logit^{-1}(x) = \frac{1}{1 + exp(-x)}$

and the term for each month is a binary indicator for whether the forecasted week lies in each month, and ecoregion is dichotomized to represent two tropical ecoregions most associated with increased Yellow Fever burden.

Predicted incidence of Yellow Fever in each municipality is defined as 

$ln(Incidence) = -5.787 + (241.946 \times MinimumPrecipitation) \\ + (1119.650 \times MinimumHumidity) - (42145.567 \times MinimumHumidity^{2}) \\ - (0.507 \times Previous YF) + (9.530 \times DrainageDensity)$

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

<!-- html table generated in R 4.0.3 by xtable 1.8-4 package -->
<!-- Wed Nov 10 10:49:05 2021 -->
<table border=1>
<tr> <th>  </th> <th> Municipality </th> <th> Probability </th>  </tr>
  <tr> <td align="right"> 1 </td> <td> Rio Claro, Rio de Janeiro </td> <td align="right"> 0.51 </td> </tr>
  <tr> <td align="right"> 2 </td> <td> Aruja, São Paulo </td> <td align="right"> 0.51 </td> </tr>
  <tr> <td align="right"> 3 </td> <td> São João da Boa Vista, São Paulo </td> <td align="right"> 0.51 </td> </tr>
  <tr> <td align="right"> 4 </td> <td> Barão de Cocais, Minas Gerais </td> <td align="right"> 0.50 </td> </tr>
  <tr> <td align="right"> 5 </td> <td> Belo Horizonte, Minas Gerais </td> <td align="right"> 0.50 </td> </tr>
  <tr> <td align="right"> 6 </td> <td> Belo Vale, Minas Gerais </td> <td align="right"> 0.50 </td> </tr>
  <tr> <td align="right"> 7 </td> <td> Brumadinho, Minas Gerais </td> <td align="right"> 0.50 </td> </tr>
  <tr> <td align="right"> 8 </td> <td> Caeté, Minas Gerais </td> <td align="right"> 0.50 </td> </tr>
  <tr> <td align="right"> 9 </td> <td> Carandaí, Minas Gerais </td> <td align="right"> 0.50 </td> </tr>
  <tr> <td align="right"> 10 </td> <td> Congonhas, Minas Gerais </td> <td align="right"> 0.50 </td> </tr>
  <tr> <td align="right"> 11 </td> <td> Conselheiro Lafaiete, Minas Gerais </td> <td align="right"> 0.50 </td> </tr>
  <tr> <td align="right"> 12 </td> <td> Consolação, Minas Gerais </td> <td align="right"> 0.50 </td> </tr>
  <tr> <td align="right"> 13 </td> <td> Diogo de Vasconcelos, Minas Gerais </td> <td align="right"> 0.50 </td> </tr>
  <tr> <td align="right"> 14 </td> <td> Guarani, Minas Gerais </td> <td align="right"> 0.50 </td> </tr>
  <tr> <td align="right"> 15 </td> <td> Itabira, Minas Gerais </td> <td align="right"> 0.50 </td> </tr>
  <tr> <td align="right"> 16 </td> <td> Itabirito, Minas Gerais </td> <td align="right"> 0.50 </td> </tr>
  <tr> <td align="right"> 17 </td> <td> Itaverava, Minas Gerais </td> <td align="right"> 0.50 </td> </tr>
  <tr> <td align="right"> 18 </td> <td> João Monlevade, Minas Gerais </td> <td align="right"> 0.50 </td> </tr>
  <tr> <td align="right"> 19 </td> <td> Juiz de Fora, Minas Gerais </td> <td align="right"> 0.50 </td> </tr>
  <tr> <td align="right"> 20 </td> <td> Lagoa dourada, Minas Gerais </td> <td align="right"> 0.50 </td> </tr>
   </table>

### If any Yellow Fever cases occur, the following municipalities have the highest forecasted incidence:

<!-- html table generated in R 4.0.3 by xtable 1.8-4 package -->
<!-- Wed Nov 10 10:49:05 2021 -->
<table border=1>
<tr> <th>  </th> <th> Municipality </th> <th> Incidence </th>  </tr>
  <tr> <td align="right"> 1 </td> <td> Laguna, Santa Catarina </td> <td align="right"> 420.15 </td> </tr>
  <tr> <td align="right"> 2 </td> <td> Capivari de Baixo, Santa Catarina </td> <td align="right"> 416.70 </td> </tr>
  <tr> <td align="right"> 3 </td> <td> Simão Pereira, Minas Gerais </td> <td align="right"> 231.38 </td> </tr>
  <tr> <td align="right"> 4 </td> <td> Comendador Levy Gasparian, Rio de Janeiro </td> <td align="right"> 156.51 </td> </tr>
  <tr> <td align="right"> 5 </td> <td> Alpercata, Minas Gerais </td> <td align="right"> 116.92 </td> </tr>
  <tr> <td align="right"> 6 </td> <td> Derrubadas, Rio Grande do Sul </td> <td align="right"> 104.48 </td> </tr>
  <tr> <td align="right"> 7 </td> <td> Alto Bela Vista, Santa Catarina </td> <td align="right"> 66.87 </td> </tr>
  <tr> <td align="right"> 8 </td> <td> Chiador, Minas Gerais </td> <td align="right"> 65.82 </td> </tr>
  <tr> <td align="right"> 9 </td> <td> Formosa do Sul, Santa Catarina </td> <td align="right"> 57.57 </td> </tr>
  <tr> <td align="right"> 10 </td> <td> Barra do Guarita, Rio Grande do Sul </td> <td align="right"> 48.97 </td> </tr>
  <tr> <td align="right"> 11 </td> <td> Coronel Freitas, Santa Catarina </td> <td align="right"> 47.31 </td> </tr>
  <tr> <td align="right"> 12 </td> <td> Piratuba, Santa Catarina </td> <td align="right"> 47.29 </td> </tr>
  <tr> <td align="right"> 13 </td> <td> Tunápolis, Santa Catarina </td> <td align="right"> 45.01 </td> </tr>
  <tr> <td align="right"> 14 </td> <td> Quilombo, Santa Catarina </td> <td align="right"> 42.23 </td> </tr>
  <tr> <td align="right"> 15 </td> <td> Campo Bonito, Paraná </td> <td align="right"> 41.53 </td> </tr>
  <tr> <td align="right"> 16 </td> <td> Contenda, Paraná </td> <td align="right"> 37.72 </td> </tr>
  <tr> <td align="right"> 17 </td> <td> Belmiro Braga, Minas Gerais </td> <td align="right"> 37.40 </td> </tr>
  <tr> <td align="right"> 18 </td> <td> Araucária, Paraná </td> <td align="right"> 37.17 </td> </tr>
  <tr> <td align="right"> 19 </td> <td> Ouvidor, Goiás </td> <td align="right"> 37.16 </td> </tr>
  <tr> <td align="right"> 20 </td> <td> São José dos Pinhais, Paraná </td> <td align="right"> 36.30 </td> </tr>
   </table>

## Contributing factors to forecasts

The maps below show the predictors that were used to produce forecasts of Yellow Fever occurrence and incidence. 

**Mean temperature two weeks prior**

![ ](/Users/jjs7684/Desktop/YF_Forecast_visuals/MeanTemp.png){width=45%}

**Yellow Fever occurrence seven weeks prior**

![ ](/Users/jjs7684/Desktop/YF_Forecast_visuals/PrevOcc946.png){width=45%}

**Ecoregion**

![ ](/Users/jjs7684/Desktop/YF_Forecast_visuals/EcoReg_bin.png){width=45%}

**Minimum rainfall two weeks prior**

![ ](/Users/jjs7684/Desktop/YF_Forecast_visuals/MinRain.png){width=45%}

**Minimum humidity two weeks prior**

![ ](/Users/jjs7684/Desktop/YF_Forecast_visuals/MinHum.png){width=45%}

**Yellow Fever occurrence two weeks prior**

![ ](/Users/jjs7684/Desktop/YF_Forecast_visuals/PrevOcc951.png){width=45%}

**Drainage density**

![ ](/Users/jjs7684/Desktop/YF_Forecast_visuals/Drainage.png){width=45%}

### Probability of Yellow Fever occurrence

The model includes mean temperature two weeks prior, month of forecast, occurrence of Yellow Fever two weeks prior, and ecoregion to forecast probability of future Yellow Fever occurrence. This is defined as the probability of seeing any Yellow Fever cases in any quantity. Individual model effects are interpreted as the effects on forecasted probability assuming that no other factors change. For a particular factor, which can be denoted as $x$, changes in the value of $x$ change predicted probability by the following function: 

Change in probability = $\frac{1}{1 + exp(-x)}$

Individual effects are shown visually below. These plots assume other predictors are absent (if represented by binary indicators) or take their average observed value (if represented continuously).

**Mean temperature**

![](index_files/figure-html/unnamed-chunk-6-1.png)<!-- -->

**Month of forecast**

![](index_files/figure-html/unnamed-chunk-7-1.png)<!-- -->

**Previous Yellow Fever occurrence**

![](index_files/figure-html/unnamed-chunk-8-1.png)<!-- -->

**Ecoregion**

![](index_files/figure-html/unnamed-chunk-9-1.png)<!-- -->

### Forecasted Yellow Fever incidence if any cases occur

The model includes minimnum precipitation seven weeks prior, minimum humidity seven weeks prior, previous occurrence of Yellow Fever seven weeks prior, and drainage density as predictors. Estimated incidence is represented as cases per 100,000 population. Individual model effects are interpreted as the effects on forecasted probability assuming that no other factors change. For a particular factor, which can be denoted as $x$, changes in the value of $x$ change estimated incidence by $exp(x)$. Humidity is represented as a quadratic predictor, leading to a non-monotonic change in forecasted incidence from changes in humidity.

**Precipitation**

![](index_files/figure-html/unnamed-chunk-10-1.png)<!-- -->

**Humidity**

![](index_files/figure-html/unnamed-chunk-11-1.png)<!-- -->

**Previous occurrence**

![](index_files/figure-html/unnamed-chunk-12-1.png)<!-- -->

**Drainage density**

![](index_files/figure-html/unnamed-chunk-13-1.png)<!-- -->

# Notes for practical implementation

Using the produced forecasting model, a document such as this can be created each week to show predicted future burden of Yellow Fever. 

Producing weekly forecasts requires regularly updating the environmental data. Doing so requires downloads of the Modern-Era Retrospective Analysis for Research and Applications, version 2 (MERRA-2), which is available at no cost through the United States National Aeronautics and Space Administration. While these data can be accessed by the public, they are available in spatial grids that need to be matched to the municipalities of Brazil in order to produce the forecasts. An extension of this current framework could allow automatic downloading and cleaning of the environmental data to reduce the time needed to produce forecasts. 

The forecasting models were produced using data collected through March 2018. Following the end of the Yellow Fever outbreak in Brazil, replicating the methods used for more updated data is recommended to assure that the relationships between environmental predictors and future Yellow Fever occurrence and incidence have not changed recently. This was seen using data prior to and following the start of the recent epidemic. Using the same set of predictors, different models produced the most accurate forecasts between the two time periods.

