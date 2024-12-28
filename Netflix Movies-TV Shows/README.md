# Welcome to own dashboard about Netflix movies and TV shows! 👋


[<img src="https://icon-library.com/images/link-icon-svg/link-icon-svg-29.jpg" width="300" height="200" alt="Netflix Dashboard">](https://github.com/RodriNico2206/Power-BI/blob/master/Netflix%20Movies-TV%20Shows/Netflix%20Movies-TV%20Shows.pdf)


## Introduction
In this case, supposing that data set of netflix is cleaning, i performed several insights and visualizations useful to getting conclusion for this data base.

## information of data set



## Development

- DAX Language:

<div id="badges" align="center">
  <img src="https://www.ati-mirage.com.au/wp-content/uploads/2021/03/powerbidax.png" alt="Profile Image" style="width: 80px; height: 80px;"/>
</div>

- Measures developed:
It has been developed through usage DAX language for the purpose of get information about data

  - % de Películas en la plataforma = [N° de películas dentro de la plataforma]/[N° total de contenido disponible en la plataforma]

  - % de Shows de televisión en la plataforma = [N° de Shows de televisión dentro de la plataforma]/[N° total de contenido disponible en la plataforma]

 - N° de películas dentro de la plataforma = CALCULATE([N° total de contenido disponible en la plataforma],
  netflix_titulos[type]="Movie")

 - N° de Shows de televisión dentro de la plataforma = CALCULATE([N° total de contenido disponible en la plataforma],
  netflix_titulos[type]="TV Show")

 - N° total de contenido disponible en la plataforma = COUNT(netflix_titulos[listed_in])

 - Recuento de directores sin otros = CALCULATE(COUNTA(netflix_titulos[director]), 
  FILTER(netflix_titulos, netflix_titulos[director]<>"Others") )
