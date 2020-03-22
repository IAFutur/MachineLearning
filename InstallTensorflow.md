# Comment installer Tensorflow sur votre machine 

Tensorflow est une bibliothèque de composants que vous pouvez ajouter à votre éditeur de code en langage Python afin de développer des applications de Machine Learning.
La grande force de la bibliothèque Tensorflow est sa flexibilité.
En effet, Tensorflow est assez versatile pour être utilisé avec différents hardware pour la création de l'application ML puis pour son déploiement sur tout type de plateformes incluant les OS PC et Mac, les mobiles, les serveurs ou encore les navigateurs.
En suivant ces instructions vous pourrez ainsi installer facilement et correctement Tensorflow sur votre matériel sans prise de tête. 

## Tensorflow CPU et TPU 

Ce sont surement les versions les moins démocratisées de la bibliothèque comme elles sont les plus contraignantes. 
Tensorflow TPU est une version optimisée uniquement pour des machines virtuelles développées par Google donc vous aurez assez de chances de les utiliser donc nous ne les aborderons pas dans ce post. 

### Installer Tensorflow CPU 

Tensorflow CPU repose entièrement sur l'architecture de votre ordinateur. Ainsi, quand l'éditeur de code compile et génère des opérations, ils sont envoyés bruts à l'unité de calcul CPU.
C'est ensuite ce composant physique de votre ordinateur qui se charge d'effectuer la mise en forme des calculs puis de les exécuter et de renvoyer les résultats. 
Le Machine Learning effectue majoritairement des opérations matricielles tandis que le CPU est habilité à gérer tous les types d'opérations. 
Vous pouvez donc imaginer que ce type de programme ne sera pas optimisé pour les applications que l'on souhaite développer et qui demandent des puissances de calculs démentielles.

Avant tout, vous avez besoin du langage **Python** installé sur votre machine.
Vous pouvez le télécharger sur le site [Python.org](www.Python.org).
Je vous recommande une version 3.6 de Python comme c'est celle qui est le plus compatible avec Tensorflow. 
Dans le bas de la page, choisissez l'installer qui correspond à votre système d'exploitation. 
Durant le processus d'installation, n'oubliez pas d'ajouter Python au PATH de votre ordinateur ce qui nous évitera de bricoler les variables d'environnement à ce point-là. 

Vous pouvez maintenant installer Tensorflow en vous servant de pip le package installator inclus dans **Python**. 
Rien de plus simple, cherchez dans votre menu Démarrer sur Windows l'invité de commande puis insérez la commande suivante 
```
pip install tensorflow-cpu==$VERSION$
```
Vous pouvez remplacer `$VERSION$` par la version que vous souhaitez installer. 
Je vous conseille la version 2.0 car c'est la version la plus aboutie de Tensorflow avec des modules les plus avancés pour le développement d'applications. 
Tandis que Tensorflow 2.1 est encore sujet à des bugs et problèmes de mises à jour. 

C'est tout ! Vous êtes prêt à utiliser **Tensorflow CPU** !

