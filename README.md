**Projet Evolution de la vitesse lors du freinage**

Membres du projet:
- BENZIDANE El Yazid
- MIM Akram
- MARZOUGUI Wassim

**Descriptif du projet:**

Notre sujet de recherche concerne l'étude de l'évolution de la vitesse en fonction du temps lors du
freinage d'un véhicule. Cette thématique revêt un intérêt majeur dans de nombreux domaines,
notamment scientifique, technique, commercial, mais aussi sociétal.
En effet, comprendre comment la vitesse d'un véhicule varie pendant le freinage permet de mieux
appréhender les mécanismes physiques à l'œuvre dans ce processus. Cela peut ensuite conduire à
l'amélioration de la sécurité routière en développant des systèmes de freinage plus performants.
D'un point de vue commercial, les constructeurs automobiles ont tout intérêt à concevoir des
voitures dotées d'un système de freinage efficace pour offrir un niveau de sécurité maximal à leurs
clients. De même, les professionnels de l'assurance peuvent utiliser ces données pour évaluer les
risques liés aux accidents de la route.
Enfin, d'un point de vue sociétal, la compréhension des mécanismes impliqués dans le freinage
permet de sensibiliser les conducteurs à l'importance du respect des distances de sécurité et de la
vitesse limite sur les routes. Cela contribue à améliorer la sécurité des usagers de la route et à
réduire le nombre d'accidents de la circulation.

**Problématique:**

Comment notre modèle dynamique peut-il aider à mieux comprendre et optimiser le processus de freinage en analysant l'évolution de la vitesse et les facteurs influençant la décélération d'un véhicule en mouvement ?


Semaine 10 mars:
- Définiton de la problématique
- recherche documentaire
- recherche de modèles

Semaine 17 Mars:

Nous avons hésité entre plusieurs modèles. Nous avons défini plus précisemment le caractère dynamique de notre projet grace aux recherches documentaires.

Semaine 24 Mars:

Nous avons fais des recherches sur les formules de physique qui pourraient nous aider. Nous avons trouvé la formule v=v0*at.

Semaine 31 Mars:

Nous avons décidé des paramètres à prendre en compte. certains paramètres sont négligeables ou trop compliqués à intégrer au modèle comme les différents systèmes de freinage, les systèmes d'abs, l'aérodynamise des véhicules ou encore la densité de l'air. 

Semaine 7 Avril:

Nous avons commencé à effectuer des tests sur python avec des graphiques en utilisant matplotlib afin de visualiser l'avancée de notre travail. Nous avons vu qu'il etait possible d'utiliser la méthode d'Euler afin de calculer la vitesse, c'est une méthode qui utilise l'équation diférentielle suivante: 
dv/dt = -µ * g - (0.5 * ρ * Cd * A * v²) / m qu'il faut résoudre afin d'avoir la vitesse. Cette méthode à été écartée car elle prend en compte la resistance de l'air qui dépend du modèle de véhicule, de la densité de l'air, de la surface frontale, etc...

Semaine 14 Avril:

Nous avons finalisé le code python. Nous avons remarqué que la masse s'annule dans les calculs car plus la masse du véhicule est importante, plus le système de freinage est performant donc adapté.

Semaine 21 Avril:

Nous avons finalisé la présentation et réparti les roles entre les membres du groupe. nous avons effectué les derniers tests et les ecemples de graphique afin de les montrer.

**Description du modèle:**

<img width="620" alt="Formule1" src="https://user-images.githubusercontent.com/125645155/233501182-cc737c81-e370-4dd5-ac4e-429f476284fd.png">

Ce modèle décrit la relation entre la vitesse (v) d'un objet en mouvement, la vitesse initiale (v0) et la décélération (a) subie par cet objet pendant une période de temps (t).
La vitesse initiale (v0) correspond à la vitesse de l'objet au début du mouvement, avant que la décélération ne commence à agir sur lui. La décélération (a) correspond à la diminution de la vitesse de l'objet au fil du temps. Plus la décélération est grande, plus l'objet ralentit rapidement.
La décélération (a) est la force opposée qui ralentit le véhicule. Elle est généralement négative, car elle agit dans le sens opposé à la direction du mouvement du véhicule.
Le temps (t) commence à s'écouler dès que le conducteur applique les freins. Plus le temps s'écoule, plus la vitesse diminue.
En utilisant l'équation v = v0 - at, vous pouvez calculer la vitesse finale (v) du véhicule à n'importe quel moment (t) après avoir appliqué les freins.
Ce modèle peut être utilisé pour analyser l'évolution de la vitesse en fonction du temps et de la décélération. Il peut également aider à déterminer la distance de freinage, qui est la distance parcourue par le véhicule pendant le processus de freinage.
Il convient de noter que, bien que ce modèle soit utile pour comprendre les principes de base de l'évolution de la vitesse lors du freinage, il ne prend pas en compte certains facteurs négligeables qui peuvent influencer légèrement la décélération, tels que l'aérodynamique, la densité de l’air, et les caractéristiques spécifiques du système de freinage.

<img width="350" alt="Capture d’écran 2023-04-21 à 00 56 15" src="https://user-images.githubusercontent.com/125645155/233503764-56e475ca-fe4f-4b04-b928-0a8b6dd7db8e.png">

Lorsqu'un véhicule freine, la force qui permet de ralentir le véhicule provient principalement de la friction entre les pneus et la surface de la route. Cette force de friction dépend de plusieurs facteurs, dont le coefficient de frottement (µ) et le poids du véhicule.
Le coefficient de frottement (µ) est une mesure sans unité qui caractérise la force de friction entre deux surfaces en contact. Dans le cas du freinage d'un véhicule, µ représente la force de friction entre les pneus et la surface de la route. Des valeurs de µ plus élevées indiquent une meilleure adhérence entre les surfaces, ce qui permet une décélération plus importante. Le coefficient de frottement peut varier en fonction du type de pneu, de la surface de la route, et des conditions météorologiques (par exemple, une route mouillée ou enneigée aura un coefficient de frottement plus faible qu'une route sèche et propre).
La force gravitationnelle (g) est la force qui attire tous les objets vers le centre de la Terre. Sur Terre, l'accélération due à la gravité est d'environ 9,81 m/s². Cette force est responsable du poids du véhicule et influe directement sur la force de friction entre les pneus et la route.
La formule a = µ * g permet de calculer la décélération maximale possible en fonction du coefficient de frottement et de la force gravitationnelle. Si le coefficient de frottement est élevé, cela signifie que la force de friction entre les pneus et la route est importante, et le véhicule peut décélérer plus rapidement. À l'inverse, si le coefficient de frottement est faible, la décélération maximale sera plus faible, ce qui signifie que le véhicule mettra plus de temps à s'arrêter.


**Paramètres pris en compte:**

Nous avons décide de prendre en compte la vitesse initiale de la voiture, l'état de la route et des pneus, la gravité et la masse du véhicule.

**Cas témoin:**

![image](https://user-images.githubusercontent.com/125645155/233502190-215285b1-a2bf-43a5-80f2-6a5d9db72f15.png)

Lorsqu'une voiture roule sur une route sèche avec des pneus en bon état et une vitesse initiale de v0 = 27.7 m/s sur la planète Terre, la force de frottement entre les pneus et la route permet de ralentir le véhicule jusqu'à son arrêt complet. Cette force de frottement dépend du coefficient de frottement µ, qui pour cette situation est de 0,7.
Au début du freinage, la voiture ralentit rapidement, perdant de la vitesse presque linéairement au fil du temps. En d'autres termes, la décélération est presque constante pendant cette phase. Cependant, à mesure que la voiture ralentit, la force de frottement diminue progressivement, ce qui entraîne une diminution de la décélération. Finalement, la vitesse de la voiture diminue jusqu'à s'annuler, moment où la voiture s'arrête complètement.

**Résultats :**

pour v0 = 10 m/s :

![image](https://user-images.githubusercontent.com/125645155/233502398-8a84b24f-51c5-4a10-9c42-936516ef76a8.png)

pour v0 = 50 m/s :

![image](https://user-images.githubusercontent.com/125645155/233502469-6af5590a-9480-44cd-aca8-e461a9504d80.png)

pour µ=0,425 route mouillée :

![image](https://user-images.githubusercontent.com/125645155/233502614-c910bf70-d641-4e31-bc77-2d3e28bbb9ce.png)

pour µ=0,25 route mouillée + pneus deffectueux :

![image](https://user-images.githubusercontent.com/125645155/233502699-b63e8d3f-ca9d-4fcb-8e8c-c677b7ca6949.png)


**Conclusion :**

Dans ce projet, nous avons étudié l'évolution de la vitesse d'un véhicule lors du freinage en tenant compte de la masse du véhicule, du coefficient de frottement et de la gravité. Nous avons utilisé des modèles mathématiques pour simuler et visualiser l'impact de ces paramètres sur la performance de freinage. Les résultats obtenus montrent comment la vitesse du véhicule décroît progressivement jusqu'à ce qu'il s'arrête complètement.

Les enjeux liés à la compréhension de l'évolution de la vitesse lors du freinage sont nombreux. Tout d'abord, une meilleure connaissance de ces phénomènes permet d'améliorer la sécurité routière en aidant les conducteurs à adapter leur comportement en fonction des conditions de la route, telles que les routes mouillées ou sèches, et en tenant compte de la masse de leur véhicule. De plus, les constructeurs automobiles peuvent utiliser ces informations pour concevoir des systèmes de freinage plus performants et plus adaptés aux différents types de véhicules et de situations de conduite.

En outre, cette étude met en évidence l'importance de la prise en compte de l'état de la route et de la force de freinage dans le modèle, car ces éléments peuvent également influencer l'évolution de la vitesse lors du freinage.

En conclusion, l'analyse de l'évolution de la vitesse lors du freinage est cruciale pour améliorer la sécurité routière et optimiser les performances de freinage des véhicules. Les enjeux associés à ce sujet concernent à la fois les conducteurs, les constructeurs automobiles et les autorités de régulation, qui doivent travailler ensemble pour réduire les risques d'accidents et garantir une conduite sûre et responsable sur les routes.
