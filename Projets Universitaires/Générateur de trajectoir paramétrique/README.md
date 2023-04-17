**Projet: Générateur de trajectoire pour une grue**

Dans ce projet, un générateur de trajectoire paramétrique a été développé pour déplacer une charge de manière contrôlée avec une grue. La trajectoire consiste en un mouvement vertical initial, suivi d'un déplacement linéaire horizontal et finalisé par un mouvement vertical vers le bas. L'objectif est d'avoir des mouvements continus à vitesse constante et d'atteindre cette vitesse avec une accélération prescrite.

Le générateur de trajectoire utilise des équations paramétriques pour déterminer la trajectoire en 2D, avec des variables représentant l'élévation (y) et le déplacement horizontal (x) de l'objet. Les équations permettent d'imposer divers paramètres, tels que l'élévation maximale, la distance horizontale à parcourir, la longueur du câble, l'accélération gravitationnelle, la vitesse maximale, l'accélération maximale et l'erreur maximale d'initialisation des courbes logistiques.

La trajectoire est ensuite réorientée pour produire un mouvement en 3D dans l'espace de la grue. Les courbes de position, de vitesse et d'accélération sont présentées pour les composantes verticale et horizontale de la trajectoire. Le générateur de trajectoire est conçu pour permettre des trajectoires avec des élévations de départ et d'arrivée différentes en utilisant un paramètre supplémentaire.

## Aperçu

![Figure19 Exemple detrajectoire gnrepar les quations paramtriques](G:/My Drive/Professionnel/Recherche d'emplois/Portfolio/Projets Universitaires/G�n�rateur de trajectoir param�trique\media\Pasted image 20230415183223.png|300)

![Profil de deplacement horizontal en fonction du temps](G:/My Drive/Professionnel/Recherche d'emplois/Portfolio/Projets Universitaires/G�n�rateur de trajectoir param�trique\media\Pasted image 20230415183257.png|300)

![Figure 30  Profil de position vitesse et acceleration de la composante horizontale de la trajectoire](G:/My Drive/Professionnel/Recherche d'emplois/Portfolio/Projets Universitaires/G�n�rateur de trajectoir param�trique\media\Pasted image 20230415183409.png|300)



Graphique interactif du générateur de trajectoire : 

https://www.desmos.com/calculator/mqbedhqcre



<iframe src="https://www.desmos.com/calculator/mqbedhqcre" allow="fullscreen" allowfullscreen="" style="height:100%;width:100%; aspect-ratio: 16 / 9; "></iframe>



