# R pour les journalistes
R est un programme et un langage gratuit et open-source. Pensé par et pour des statisticiens, il accueille aujourd'hui aussi bien des biologistes, des sismologues et... des datajournalistes.
L'idée de cette page est d'encourager les journalistes français, curieux des outils utilisés pour le datajournalisme, à choisir R comme solution pour réaliser leurs traitements statistiques et leurs visualisations.

# Comment ça marche ?

## C'est quoi le principe ? 

Le principe de base, c'est qu'un logiciel qui fonctionne par script permet de contrôler davantage les différentes étapes d'un traitement de données. Récupérer ou retrouver un tableur dans lequel les entêtes ne sont pas clairs et dans lequel les formules ont été effacées suffit pour percevoir les grands avantages qu'il peut y avoir a transmettre ou conserver un script.
S'il y a une incohérence finale, il suffit de repasser pas à pas sur les différentes étapes du script.


# R pour la création et manipulation de bases de données

R est un langage particulièrement utile pour réaliser des opérations sur de grandes bases de données et pour les maintenir dans des formats accessibles pour le plus grand nombre.

La structure la plus importante de R, au niveau débutant en tous cas, est le dataframe. C'est notre tableur. Il faut simplement tenter d'y penser légèrement différemment. La bonne pratique du dataframe, c'est de ranger une observation (un individu, une année, etc) par ligne et d'indiquer l'ensemble de ses caractéristiques dans les colonnes du dataframe.

On peut appeler son contenu en utilisant les coordonnées des cellules qui nous intéresse, dans l'ordre ligne, colonne. Par exemple tableur[1,2]. De la même façon, on peut appeler toutes les valeurs de la première ligne avec tableur [1,] et toutes celles de la première colonne avec tableur [,1]
On peut aussi sélectionner toutes les valeurs d'une variable avec le $, par exemple tableur$variable.
Autre point important de R : le signe *<-* : il permet d'attribuer une valeur à un objet. Par exemple : 

## Base R : subset, t, str, as.ch, as.num, as.POSIX


## Tidyverse : Dplyr: group_by, filter

# R for stats

## Base R
### Tables &  proptables
### Summary
### Max, min, which, mean
## Dplyr
### Group_y, select
### Summarise
### Mutate

# R for article creationo

## Rmarkdown for text : word/pdf/HTML/blog/bookdown

## R data to video

## R data to audio

# R for dataviz

## Static dataviz
### Base: plot, hist, boxplot, points
### Ggplot2 : geom_bar, geom_line, geom_point, geom_jitter, facet_grid

## animated dataviz

# R for cartography
Geocode, distance
## Simple rgdal
## Package gmap
## Package leaflet
# R for interactive dataviz

# R for everything else (?)
## Text mining with Iramuteq
## Web scraping with Rvest
## Pdf scraping
## Typo writing with extrafont
