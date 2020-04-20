# La Base de données MNIST 

Avec l'émergence du Big Data et de la société de l'information, on pourrait être amené à croire que le Machine Learning et l'Intelligence Artificielle par essence sont une nouveauté. Il n'en est rien. Le Machine Learning est une science qui a été l'objet d'intenses recherches depuis les années 60. Cependant, c'est avec l'explosion des capacités de calculs et l'apparition de larges banques de données que le Machine Learning a vraiment trouvé une application viable. En effet, toutes les grandes sociétés de services technologiques utilisent aujourd’hui abondamment le Machine Learning et ses dérivés (Amazon, Netflix, Google, Apple, Microsoft, Facebook, etc...). 

Mais il a bien fallu un début à tout cela. Un des sujets de recherches les plus intensément étudié dans le sous-domaine de l'apprentissage supervisé (Supervised Learning) est très certainement le traitement de l'image. Les techniques associées peuvent facilement trouver des applications dans le monde contemporain (lecture de code, reconnaissance faciale, etc..). Quand les capacités de calculs étaient bien moindres, un problème s'est donc imposé comme une mesure de performances pour départager les différents programmes proposés. Ce problème consiste à classifier des chiffres écrits à la main puis numérisés dans leur classe respective. Dans la pratique, les instigateurs de ce projet ont rassemblé 70.000 images de chiffres écrits à la main par des lycéens et des employés de l'INSEE américain, ils les ont numérisées puis mises en forme sous la forme de matrices de pixels en nuances de gris couplées avec le chiffre qu'elles représentent. 

Ainsi pour cette première incursion dans le monde du Machine Learning, nous nous intéresserons à la résolution de ce problème avec un réseau de neurones qui n'est ni plus ni moins qu'une architecture parmi d'autre utilisée pour résoudre ce problème. La grande spécificité des réseaux de neurones est leur capacité à absorber et apprendre des fonctions hautement non linéaires, ce qui demanderait des temps infinis pour coder de manière plus classique un algorithme réalisant une tâche similaire.


<p align="center">
  <img src="../../doc/MnistExamples.png">
</p>
