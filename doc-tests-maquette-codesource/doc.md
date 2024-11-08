# Documentation #

## Stack ##
Figma (maquette)

Unsplash pour les images

VsCode : 
HTML
CSS
JS

Pas de libraries ni de frameworks utilisés.

## Preparation ##
Maquettage avec Figma, j'en ai profité pour refaire le logo car je n'aime pas trop travailler avec de l'IA.
J'ai voulu faire une bannière carousel pour ce projet. Vous pouvez trouver le code détaillé sur ma repo GitHub : https://github.com/AnKSoup/Simple-Carousel-Project

## Explication du code ##
Les explications du carousel sont sur mon github mais pour résumer :
Récupération des images ds le dom; 
Utilisé comme bg images du carousel;
Création d'indicateur de slides cliquable pour chaque image;
Le carousel rapetisse ou grandi selon la valeur de scroll du document;

Cependant le header en lui même reste de la même taille j'ai donc désactivé les pointer-events : il fallait alors les réactiver pour les éléments ajoutés au header afin de ne pas compromettre le bon fonctionnement de la page.

Le CSS reste basique (bien que à 90% responsive et pas super opti mais bon) donc je vais plutôt m'attardé sur le JS :

Utilisation de boxshadow inset sur le bg image du carousel pour l'assombrir lorsqu'on scroll.

Pour gérer les dropdowns je toggle des classes qui le montre ou le cache au clique.
Particularité pour mobile, quand on clique en dehors du dropdown alors qu'il est actif : le dropdown disparaît.

Pour la validation de l'âge : j'ai trouvé ce petit code simple dans la doc de w3c donc je l'ai juste utilisé. 

Pour calculer le montant des billets : je récupère le prix et le amount rentré par utilisateur
lorsque le amount n'est plus focus ou increased/decreased avec les petites flèches : si le amount est un entier supérieur à 0 alors on fait juste amount*prix

## Autocritique ##
- JS trop complexe cause du tord à la responsivité du site : il faut reload pour que certain effets soient pris en compte. La solution "sale" serait de causer un reload à chaque resize de la viewport du client. 
- Css pas opti, en partie à cause du js qui venait décaler des éléments.
- Css trop long.
- Css pas 100% responsive certaines dimensions bizarres force des éléments à se superposer. Mais pas de soucis pour les dimensions les plus orthodoxes.
- Le scroll smooth ajouté à des anchors décalées différemment empêche responsively de marcher mais individuellement ça marche bien.

## Résumé ##
Il faut absolument tout réécrire pour que ça marche mais manque de temps.