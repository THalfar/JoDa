# JoDa
Joda kurssin repo.

Kurssi työnä on ennustaa Tampereella olevien asuntojen hintojen määrää annetusta datasta. 
Opetusdata löytyy [JoDa 2024 repo](https://github.com/InfoTUNI/joda2024/tree/main/assignment/6.2%20Price%20Prediction/data).

## Ensimmäiset tulokset XGBoost 

Siistin dataa tampere_reg skriptillä ja kokeilin ensimmäisiä XGBoost ajoja. 
Tarkoituksena hakea hyvin suoriutuva NN verkko eri k-fold osituksille ja käyttää näiden featureja XGBoost opetusaineistonta. 
Baselinenä käytän pelkkää XGBoost puhdistettuun dataan.

## Baseline XGBoost tuloksia

Koska datasetti on pieni ja en vielä ole saanut JoDa repon testiaineiston hintoja, toteutin train test splitin 10% testiaineistolla. 
Sovitettua mallia verrattiin tähän testiaineistoon ja tämän hetkiset tulokset siitä alla.

[XGBoost MAE tavoitteella](/output.png)

| Mittari               | Arvo    |
|-----------------------|---------|
| Mean squared error    | 2558.37 |
| Mean absolute error   | 29.52   |
| Parhaan mallin R²-arvo| 0.8902  |

[XGBoost MSE tavoitteella](/output_2.png)


| Mittari               | Arvo    |
|-----------------------|---------|
| Mean squared error    | 2236.98 |
| Mean absolute error   | 29.79   |
| Parhaan mallin R²-arvo| 0.9040  |
