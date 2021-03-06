# R pour les journalistes
R est un programme et un langage gratuit et open-source. Pensé par et pour des statisticiens, il accueille aujourd'hui aussi bien des biologistes, des sismologues et... des datajournalistes.
L'idée de cette page est d'encourager les journalistes français, curieux des outils utilisés pour le datajournalisme, à choisir R comme solution pour réaliser leurs traitements statistiques et leurs visualisations.

# Comment ça marche ?

## C'est quoi le principe ? 

Le principe de base, c'est qu'un logiciel qui fonctionne par script permet de contrôler davantage les différentes étapes d'un traitement de données. Récupérer ou retrouver un tableur dans lequel les entêtes ne sont pas clairs et dans lequel les formules ont été effacées suffit pour percevoir les grands avantages qu'il peut y avoir a transmettre ou conserver un script.
S'il y a une incohérence finale, il suffit de repasser pas à pas sur les différentes étapes du script.

R est un langage particulièrement utile pour réaliser des opérations sur de grandes bases de données et pour les maintenir dans des formats accessibles pour le plus grand nombre.
S'il devait y avoir un seul élément à comprendre pour se mettre à R, et donc vraisemblablement pour permettre une transition sereine entre Excel et R, c'est qu'il n'est pas nécessaire d'avoir en permanence les données dont on s'occupe sous le nez. Excel permet donne la primeur à la vue des données, R à la clarté du traitement qui leur est imputé.

# R pour la création et manipulation de bases de données

La structure la plus importante de R, au niveau débutant en tous cas, est le dataframe. C'est notre tableur. Il faut simplement tenter d'y penser légèrement différemment. La bonne pratique du dataframe, c'est de ranger une observation (un individu, une année, etc) par ligne et d'indiquer l'ensemble de ses caractéristiques dans les colonnes du dataframe.

On peut appeler son contenu en utilisant les coordonnées des cellules qui nous intéresse, dans l'ordre ligne, colonne. Par exemple tableur[1,2]. De la même façon, on peut appeler toutes les valeurs de la première ligne avec tableur [1,] et toutes celles de la première colonne avec tableur [,1]
On peut aussi sélectionner toutes les valeurs d'une variable avec le $, par exemple tableur$variable.
Autre point important de R : le signe <- : il permet d'attribuer une valeur à un objet. Par exemple : resultat<-84/100 * tableur[1,2]

## Base R : subset, t, str, as.ch, as.num, as.POSIX
Ce petit exemple nous amène à un gros avantage de R, sa capacité à stocker dans un dataframe un ensemble de valeurs diverses, des dates, des valeurs numériques, du texte, mais aussi des listes de dates, des listes de chiffres, etc.
Vous avez déjà utilisé Excel. Si vous avez deja tenté d'indiquer une date sans année dans une cellule, vous avez eu affaire avec l'irrepressible besoin de Excel de reformater des cellules derrière vous. Votre 1/12 pour premier décembre est devenu 12 janvier 2018 en texte et bon courage pour modifier ce comportement de votre tableur. R va vous aider et beaucoup.
R possède, de base, un ensemble d'opérations qui permet d'interpréter un élément selon différents critères. as.character(element) comprendra l'élément comme du texte, as.numeric(element) l'interpretera, si possible, comme un nombre, et s'il n'y arrive pas comme une valeur manquante. as.date(element, "m/d") interprétera les données comme une date au format mois/jour. Pour en apprendre davantage sur as.date ainsi que sur toutes les autres commandes de R, il suffit de taper ?nomdelafonction ou help nomdelafonction.
Un élément est particulièrement utile au sein de l'environnement R: la commande subset. R parvient à charger de lourdes bases de données, mais on a rarement besoin de l'intégralité des données présentes. Dans ce cas, et pour mettre au point une base de données optimale, il suffit d'indiquer à subset les conditions de découpage du jeu de données initial. 
Si l'on veut extraire l'ensemble des éléments à Paris,il suffira d'appeler la commande subset(jeudedonnees, ville=="Paris").
Pour ne garder du jeu de données initial qur les valeurs supérieures a 6, subset(jeudedonnees, ville=="Paris" & valeur >6). Et dans le cas où l'on veut garder les éléments qui correspondent à l'un ou l'autre possibilité, on utilise la commande |.

## Tidyverse : group_by, filter
Arrive à présent le moment d'évoquer le tidyverse, de tidy et universe. Il s'agit d'un ensemble de packages qui fonctionnent sur le même principe : simplifier les enchaînements de commandes, via une pipe (prononcer païpe et écrire %>%).
Énorme avantage du tidyverse : la lecture du code est rendue beaucoup plus claire. Par exemple : 
meteofrance%>%
  group_by(villes,mois)%>%
  filter(temperature<0)
Quelqu'un ne connaissant rien de r, et même peu d'anglais, pourrait comprendre l'opération réalisée avec cet suite de %>%.

# R pour le traitement statistique

On entre ici dans le cœur des compétences de R. Cette introduction étant destinée à des journalistes, je vais simplement évoquer quelques unes des possibilités offertes par R dans ce domaine, et, dans la mesure du possible, celles qui seront les plus utiles.

## Base R
### Tables &  proptables
Compter le nombre de modalités d'une d'un jeu de données : table(meteofrance$villes) liste l'ensemble des villes présentes.  
### Summary


### Max, min, which, mean
## Dplyr
### Group_y, select
### Summarise
### Mutate

# R pour la création de contenus

## Rmarkdown pour formater du texte : word/pdf/HTML/blog/bookdown

## R pour créer des vidéos

## R pour créer des sons

# R pour la dataviz

## Dataviz statique
### Base: plot, hist, boxplot, points
### Ggplot2 : geom_bar, geom_line, geom_point, geom_jitter, facet_grid

## Dataviz animée

## Dataviz interactive

# R pour la cartographie

Geocode, distance
## Simple rgdal
## Package gmap
## Package leaflet



# R pour tout le reste (?)
## Text mining with Iramuteq
## Web scraping with Rvest
## Pdf scraping
## Typo writing with extrafont
