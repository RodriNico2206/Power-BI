# Welcome to own dashboard about Netflix movies and TV shows! 👋


[<img src="https://icon-library.com/images/link-icon-svg/link-icon-svg-29.jpg" width="25" height="25" alt="Netflix Dashboard">](https://github.com/RodriNico2206/Power-BI/blob/master/Netflix%20Movies-TV%20Shows/Netflix%20Movies-TV%20Shows.pdf) [Netflix Dashboard](https://github.com/RodriNico2206/Power-BI/blob/master/Netflix%20Movies-TV%20Shows/Netflix%20Movies-TV%20Shows.pdf)


## Introduction
In this case, supposing that data set of netflix is cleaning, i performed several insights and visualizations useful to getting conclusion for this data base.

## Information of data set



## Development

- DAX Language:

<div id="badges" align="center">
  <img src="https://www.ati-mirage.com.au/wp-content/uploads/2021/03/powerbidax.png" alt="DAX Language" style="width: 100px; height: 60px;"/>
</div>

- Measures developed:
It has been developed through usage DAX language for the purpose of get information about data

  - % de Películas en la plataforma = [N° de películas dentro de la plataforma]/[N° total de contenido disponible en la plataforma]

    Calculates the percentage of movies relative to total content

  - % de Shows de televisión en la plataforma = [N° de Shows de televisión dentro de la plataforma]/[N° total de contenido disponible en la plataforma]

    Calculates the percentage of TV shows relative to total content

  - N° de películas dentro de la plataforma = CALCULATE([N° total de contenido disponible en la plataforma],
    netflix_titulos[type]="Movie")
  
    Counts only movies in the content, i use CALCULATE to filter where type = "Movie", based on the total content count

  - N° de Shows de televisión dentro de la plataforma = CALCULATE([N° total de contenido disponible en la plataforma],
    netflix_titulos[type]="TV Show")
  
    Counts only TV shows in the content, i uses CALCULATE to filter where type = "TV Show", based on the total content count

  - N° total de contenido disponible en la plataforma = COUNT(netflix_titulos[listed_in])

    Simple count of all items using the listed_in column, it was used COUNT function

  - Recuento de directores sin otros = CALCULATE(COUNTA(netflix_titulos[director]), 
    FILTER(netflix_titulos, netflix_titulos[director]<>"Others") )

    Counts the number of directors excluding "Others". It was used COUNTA for director column. Moreover, i'm applying a FILTER to exclude entries where director = "Others"
