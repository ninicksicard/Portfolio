# Analyse par éléments finis du tronc du robot

Le sous-système étudié dans le présent rapport concerne le tronc du robot conçu pour la compétition. Il s’agit évidemment d’une partie essentielle du robot puisqu’il sert de base pour supporter l’ensemble des membres ainsi que la batterie et l’électronique. En raison de l'importance de ce sous-système, il est essentiel de bien comprendre et de valider sa conception. L'objectif principal de cette étude est d'analyser la performance mécanique du tronc et d'identifier les éventuelles améliorations nécessaires pour assurer le bon fonctionnement et la durabilité du robot tout au long des séances de test et de la compétition.

L'analyse par éléments finis s'avère nécessaire dans ce projet pour diverses raisons. Premièrement, elle offre l'opportunité d'évaluer les contraintes mécaniques auxquelles le tronc du robot est soumis lors de son fonctionnement normal, en particulier pendant les mouvements du bras robotisé et les déplacements de la structure. Comprendre l'impact de ces contraintes est primordial pour garantir le fonctionnement et la fiabilité du robot et prévenir d'éventuelles défaillances mécaniques. De plus, l'analyse fréquentielle fournit des renseignements précieux concernant les modes de déformation et les fréquences naturelles de la structure. Ces informations sont essentielles pour trouver les faiblesses structurelles du robot et les corriger par des ajustements et modifications précises.

Bien que l'étude ne se concentre pas sur les contraintes thermiques ou les aspects dynamiques, il est important de noter que ces facteurs pourraient également influencer de manière significative la structure du tronc, notamment par l’échauffement de la motorisation ou d’autres composantes de puissance. Toutefois, pour le moment, ces aspects ne sont pas considérés comme critiques pour la conception actuelle du robot.

Configuration des simulations.

La modélisation du sous-système est réalisée à l'aide d'un logiciel de simulation par éléments finis, en l'occurrence SolidWorks. Pour effectuer cette analyse, un maillage solide est créé sur le modèle du tronc du robot. Le maillage est de type " Maillage basé sur la courbure" de qualité élevé. Les tailles maximale et minimale des éléments sont respectivement de 31.8 mm et 0.2 mm.

Concernant les matériaux, le tronc du robot est principalement composé de tôlerie d'aluminium 6061-T6. Les composantes de motorisation et de transmissions sont fabriquées à partir d'acier, d'alliage de bronze aluminium et de composantes usinées en aluminium 6061-T6. L'ensemble des plaques sont modélisées sous forme de solides volumiques plutôt qu'en tant que tôlerie, dans le but d'obtenir une meilleure qualité de simulation. L'utilisation des options de tôlerie pourrait entraîner des erreurs de contact importantes, notamment aux points de jonction où plusieurs tôles sont superposées.

Plusieurs simplifications et approximations sont effectuées pour faciliter l'analyse. Les engrenages en interférence sont combinés en un seul corps et la jonction est adoucie pour éviter les artéfacts. Les roulements à billes sont simplifiés par des anneaux pleins de mêmes dimensions. La masse de visserie est négligée, les paliers lisses sont fusionnés aux pièces dans lesquels ils sont insérés et les moteurs sont simplifiés par des cylindres rigides de masse fixe.

Pour l’analyse statique, la fixation est appliquée au socle d'une hanche pour simuler une condition similaire à une opération normale. Le bras robotisé est substitué par une masse déportée et une autre est utilisée pour l'autre jambe.

![[Figure 1  Surface de fixation en bleu pour l'analyse fréquentielle.]]

Pour l’analyse fréquentielle, la fixation est faite sur une plaque située au cœur de l’assemblage, tel qu’illustré ci-dessus en bleu, et les deux jambes sont substitués par des masses déportées, comme présenté à la figure 2.

![[Figure 2  Configuration pour la simulation. Les masses déportées sont attachés aux socles pour les hanches et à la plaque de fixation du bras.]]

## Résultats de l'analyse statique

Les résultats de l’analyse statique permettent d’identifier la localisation des concentrations de contraintes. La structure déformée est montrée à la figure 3 A et la contrainte la plus élevée est montrée à la figure 3 B. Celle-ci se manifeste à l’extrémité de l’un des plis de la pièce joignant les deux socles de hanches ensemble. Cette contrainte maximale est de 66.112 MPa, ce qui est très raisonnable pour un assemblage de tôles d’aluminium 6061-T6. La limite élastique de ce matériau pouvant aller à plus de 290 MPa, cette contrainte y est 4.39 fois inférieure. Considérant que ce robot n’est destiné qu’à une opération d’une durée de vie limitée, la fatigue des matériaux n’est pas du tout un risque.

![[Figure 3  A Déformation de l’assemblage.]]

![[B Résultats de l’analyse statique]]

## Résultats de l’analyse fréquentielle

L’analyse fréquentielle a été réalisée à l’aide du logiciel SolidWorks. Les modes de déformation observés lors des analyses initiales ont permis d’identifier les zones où des renforcements, tels que des barres de renforcements ou des goussets, doivent être ajoutés pour améliorer la résistance et la stabilité de l’assemblage.

L’analyse finale révèle que la fréquence minimale pouvant se propager dans l’assemblage du tronc est de 31.7 Hz. Cette valeur correspond au premier mode de vibration. Les résultats indiquent également que les modes d’oscillation les plus significatifs affectent de façon considérable la position et l’orientation du bras robotisé. Les images ci-dessous présentent les 4 modes principaux du tronc du robot.

![[mode 1]]

![[mode 2]]

![[mode 3]]

![[mode 4]]

Figure 4 : Résultat d’analyse en fréquence. Les modes principaux sont (A) [mode 1, 31.6 Hz]. (B) [mode 2, 33.48 Hz] (C) [mode 3, 70.2 Hz] (D) [mode 4, 84.6 Hz]

Cinq modes de vibration ont été analysés. Les fréquences de ces modes sont les suivantes : 31.7 Hz, 33.4 Hz, 70.2 Hz, 84.6 Hz et 144.4 Hz.

## Optimisation incrémentale de la structure

Au cours de cette étude, des renforts géométriques ont été ajoutés aux plis à différents endroits, permettant une amélioration incrémentale de la rigidité de l’objet sans modifications radicales de sa structure initiale (voir figure 5 : Géométries de renfort ajoutées). Les modes de déformation sont restés cohérents, témoignant de la pertinence des ajustements apportés. Les fréquences les plus basses sont passées de 11.9 Hz, 15.51 Hz, 17.939 Hz, 18.99 Hz et 21.57 à 31.7 Hz, 33.4 Hz, 70.2 Hz, 84.6 Hz et 144.4 Hz, démontrant l’efficacité de cette approche d’optimisation.

![[Figure 5  Géométries de renfort ajoutées.]]

## Interprétation des résultats

Les résultats de l’analyse statique démontrent que les contraintes générées dans la structure du tronc en statique sont si faibles qu’elles n’apportent aucun risque. Considérant en plus que la durée de vie du robot est destinée à être courte, la fatigue matérielle ne risque aucunement de nuire aux performances du robot.

En ce qui concerne l’analyse fréquentielle, bien que la fréquence minimale de 31.75 Hz soit relativement faible pour un robot, il est peu probable que cela affecte négativement la performance du système lors de la compétition. En effet, les opérations effectuées par le bras robotisé ne se produisent pas lorsque les jambes sont en mouvement. Ainsi, malgré la présence de vibrations, le robot devrait être capable de fonctionner correctement et d’accomplir les différentes tâches de la compétition.

De plus, la multiplication de la fréquence des modes les plus sensibles, c’est-à-dire le fait que ces fréquences passent de 33.4 Hz au double à 70.2 Hz puis double encore à 144.4 Hz, est un bon signe sur le plan de la rigidité globale. Cette multiplication pourrait suggérer que les géométries permettant les oscillations des deux premiers modes pourraient être les mêmes qui permettent les modes suivants et que ceux-ci pourraient en être des harmoniques. Les figures 3 B et 3 C présentent une déformation inversée de la section du bas du tronc pour une déformation similaire du haut, ce qui renforce l’hypothèse d’harmoniques. Cela signifie que certaines modifications simples pourraient être apportées pour éliminer ces faiblesses et le résultat de cette élimination serait une amélioration très significative. Du même coup, ça signifie que du matériel pourrait être retiré pour réduire la masse du robot, sans empirer les modes les plus sensibles.

## Impact des résultats

Globalement, la validation de l’armature conçue affecte directement l’autonomie du robot. L’enjeu est de fournir une structure suffisamment rigide pour soutenir la batterie et le bras robotisé, tout en respectant la limite de poids que les articulations des chevilles peuvent supporter. Puisque le poids du bras est fixe, une armature plus lourde impose une réduction de la masse de la batterie, qui, en terme, affecte l’autonomie du robot.

Comme les analyses démontrent que la configuration actuelle ne présente pas de faiblesses structurelles graves, il est possible de conclure que le concept proposé est adéquat.