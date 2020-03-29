# Comment installer Tensorflow sur votre machine 

Tensorflow est une bibliothèque de composants que vous pouvez ajouter à votre éditeur de code en langage Python afin de développer des applications de Machine Learning. La grande force de la bibliothèque Tensorflow est sa flexibilité. En effet, Tensorflow est assez versatile pour être utilisé avec différents hardware pour la création d'applications ML puis pour son déploiement sur tout type de plateformes incluant les OS PC et Mac, les mobiles, les serveurs ou encore les navigateurs internet. En suivant ces instructions vous pourrez ainsi installer facilement et correctement Tensorflow sur votre matériel sans prise de tête. Comme j'utilise majoritairement Windows 10, toutes les explications suivantes seront faites sur cet OS.

## Tensorflow CPU et TPU 

Ce sont surement les versions les moins démocratisées de la bibliothèque comme elles sont les plus contraignantes. **Tensorflow TPU** est une version optimisée uniquement pour du matériel développé par Google donc vous aurez assez de chances de l'utiliser. Certaines sources indiquent que Google pourrait les commercialiser sur des segments grand public dans les prochaines années mais nous ne l'aborderons pas dans ce post. 


**Tensorflow CPU** repose entièrement sur l'architecture de votre ordinateur. Ainsi, quand l'éditeur de code compile et génère des opérations, ils sont envoyés bruts à l'unité de calcul CPU. C'est ensuite ce composant physique de votre ordinateur qui se charge d'effectuer la mise en forme des calculs puis de les exécuter et de renvoyer les résultats. Le Machine Learning effectue majoritairement des opérations matricielles tandis que le CPU est habilité à gérer tous les types d'opérations. Vous pouvez donc imaginer que ce type de programme ne sera pas optimisé pour les applications que l'on souhaite développer et qui demandent des puissances de calculs conséquentes.


Malgré tout ce que vous avez peut-être pu voir sur Internet jusqu'à présent, la meilleure façon pour installer Tensorflow reste la platerforme [Anaconda](https://www.anaconda.com/distribution/). En effet, elle gère absolument tout le processus d'installation fastidieux de Tensorflow, les compatibilités entre les divers package CUDA, Cudnn et Python et met même à votre disposition une suite d'environnements virtuels.  

* Avec le lien fourni précédemment, téléchargez l'installateur Anaconda3 en version Python 3.7. Au moment où j'écris ces lignes, seul Python 3.6 est supporté par Tensorflow mais pas de soucis, nous nous en occuperons par la suite. Installez Anaconda sans l'ajouter au PATH de votre ordinateur pour éviter des problèmes de compatibilité par la suite. 

* Si vous cherchez "anaconda" dans votre menu Démarrer, vous devriez trouver Spyder, Anaconda Prompt et Anaconda Navigator. Choisissez Anaconda Navigator, le navigateur se lance par la suite et vous affiche les différents éditeurs que vous allez pouvoir utiliser séparément pour chaque environnement virtuel que vous crérez. Allez dans le panneau Environnements pour créer votre venv différent de celui de base (root). Si vous essayez de le créer directement, vous vous appercevrez que seul Python 3.7 est disponible comme langage or ce n'est pas celui qui nous intéresse. Cliquez sur ``update index..`` qui va mettre à jour les packages et les versions de Python disponibles. A présent, vous pouvez ré-essayer de créer votre Venv et dans le menu déroulant de Python vous trouverez Python 3.6. Nommez votre Venv ``votreVenv`` et cliquez sur ``Créer``. 
* Maintenant que ``votreVenv`` apparaît dans la colonne de gauche vous devez encore lui ajouter les bibliothèque associées à Tensorflow. Pour ce faire, rien de plus simple: Cherchez Tensorflow dans la barre de recherche de la fenêtre de droite en ayant sélectionné l'option ``Not Installed`` dans le menu déroulant juste à sa gauche. Après avoir coché la case de ``Tensorflow``, faites un clic droit sur cette même case pour sélectionner dans ``Mark for specific version installation``la version de la bibliothèque à installer. Préférez la version 2.0.0 car au jour d'aujourd'hui, c'est la version la plus avancée du package de Google en évitant les bugs récurrents de la dernière version Tensorflow 2.1.0. 


C'est tout ! Vous êtes prêt à utiliser **Tensorflow CPU** ! En effet, pas besoin de se précocuper de l'installation de CUDA ou encore Cudnn, Anaconda se charge de trouver et d'installer pour vous les bonnes versions correspondantes à la version de Tensorflow que vous souhaitez installer. La prochaine fois vous pouvez en ouvrant Anaconda Navigator dans le Home, sélectionner votre Venv dans le menu déroulant et choisir (ou installer si vous ne l'avez pas encore fait) l'éditeur de code. Personnellement, je vous conseillerais d'opter pour Jupyter Notebook pour un premier pas dans le monde du Machine Learning. 

## Tensorflow GPU 

LA version la plus utilisée de Tensorflow. En effet, **Tensorflow GPU** a été optimisée pour l'architecture d'une carte graphique qui correspond bien dans les faits à une majorité de calcul matriciel. Cependant ce développement est assez récent et ne prend pas en charge des cartes graphiques plus vieilles. Pour exécuter Tensorflow GPU il vous faut impérativement une carte graphique NVIDIA équipée d'une puce qui supporte les CUDA Compute Capability > 3.5. Vérifiez cela avec le lien [NVIDIA](https://developer.nvidia.com/cuda-gpus). 

Si votre carte est compatible et que vous estimez que votre système est suffisamment performant, vous avez deviné que l'installation sera similaire à ce qui a été fait pour installer **Tensorflow CPU**. En effet, le processus d'installation est le suivant : 
* Téléchargez et installez Anaconda Navigator en version Python 3.7 sans l'ajouter au PATH de votre système. 
* Dans le panneau Environnements d'Anaconda Navigator, cliquez sur ``update index...`` et créez un Venv en choisissant Python 3.6 dans le menu déroulant. 
* Dans le Venv précédemment créé, cherchez et installez ``tensorflow-gpu`` et modifiez la version à installer pour opter pour **Tensorflow GPU** en version 2.0

C'est tout ! Vous êtes prêt à utiliser **Tensorflow GPU** !

Vous pouvez vérifier l'installation correcte de votre biliothèque Tensorflow en lançant l'éditeur Jupyter Notebook depuis Anaconda Navigator en choisissant bien le bon Venv. Arrivé dans Jupyter Notebook, créez un fichier de version Python 3 et saisissez les lignes de code suivantes : 
```
import tensorflow as tf 
```
Cette commande vous permet d'importer **Tensorflow GPU** et de la stocker en mémoire en vue d'une utilisation prochaine. C'est souvent le point le plus critique dans les processus d'installation de cette bibliothèque donc si tout se passe bien ici, vous avez fait le plus gros du chemin. 

```
print(tf.__version__)
```
Cette commande vous permet d'afficher la version de **Tensorflow GPU** que vous venez d'installer. En tout logique, le retour devrait être ``2.0.0`` ou bien la version que vous venez d'installer. 

```
tf.test.is_gpu_available()
```
Ici vous vérifiez que **Tensorflow GPU** détecte et est prêt à travailler avec votre carte graphique. Plus d'informations qu'un simple ``True`` peuvent être trouvées sur votre machine si vous exécutez ce même processus depuis l'invité de commandes d'Anaconda (Anaconda Prompt). Vous obtiendrez alors plusieurs informations système comme le modèle, la quantité de mémoire disponible ou encore l'emplacement physique du GPU et sa configuration dans votre système. La plupart de ces informations peuvent être retrouvées en utilisant la commande ``nvidia-smi`` depuis l'invté de commandes. 

```
tf.test.is_built_with_cuda()
```
Avec cette dernière commande vous vérifiez que votre module **Tensorflow GPU** est capable de faire transiter les calculs à la suite CUDA (que Anaconda a installé avec ``tensorflow-gpu``) qui elle les transmet aux coeurs du GPU. 

Si vous avez franchi toutes ces vérifications, Félicitations ! Votre machine est dorénavant capable d'exécuter des applications complexes de Machine Learning. 
