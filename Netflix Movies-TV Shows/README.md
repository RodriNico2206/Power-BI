# Welcome to own dashboard about Netflix movies and TV shows! 👋

![Link to dashboard](link_to_profile_banner_image)

## Introduction
In this case, supposing that data set of netflix is cleaning, i performed several insights and visualizations useful to getting conclusion for this data base.



## Key Skills and Expertise

- DAX Language:

<div id="badges" align="center">
  <img src="https://www.ati-mirage.com.au/wp-content/uploads/2021/03/powerbidax.png" alt="Profile Image" style="width: 80px; height: 80px;"/>
</div>

- Measures developed:

  - % de Películas en la plataforma = [N° de películas dentro de la plataforma]/[N° total de contenido disponible en la plataforma]

  - % de Shows de televisión en la plataforma = [N° de Shows de televisión dentro de la plataforma]/[N° total de contenido disponible en la plataforma]

 - N° de películas dentro de la plataforma = CALCULATE([N° total de contenido disponible en la plataforma],
  netflix_titulos[type]="Movie")

 - N° de Shows de televisión dentro de la plataforma = CALCULATE([N° total de contenido disponible en la plataforma],
  netflix_titulos[type]="TV Show")

 - N° total de contenido disponible en la plataforma = COUNT(netflix_titulos[listed_in])

 - Recuento de directores sin otros = CALCULATE(COUNTA(netflix_titulos[director]), 
  FILTER(netflix_titulos, netflix_titulos[director]<>"Others") )
