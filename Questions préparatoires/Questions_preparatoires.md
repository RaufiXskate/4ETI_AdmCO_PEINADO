**Activités AdmCo Partie 1 2023-2024**

# Réponses aux questions préparatoires

1) Expliquer le code suivant  (addition.py):

def add(x, y): # on définit une fonction addition

  z=x+y # on réalise l'addition

  print('add() executed under the scope: ', __name__)

  return z # on retourne le résultat de l'addition

if __name__ == '__main__':  # on créer un main 

  x=input('Enter the first number to add: ') # on récupère une première valeur x

  y=input('Enter the second number to add: ') # on récupère une deuxième valeur y

  result = add(int(x),int(y)) # on appelle la fonction addition pour faire l'addition des deux nombres entrés

  print(x, '+', y,'=', result) # affichage du résultat

  print('Code executed under the scope: ', __name__) # permet de savoir la manière dont a été exécuté un programme
  

1) A quoi sert requirments.txt ?

Le fichier `requirments.txt` permet d'indiquer quelles sont les paquets et librairies Python nécessaire aux environnements virtuels pour que le programme fonctionne correctement. 
Il contient une liste de package que l'ont peu utiliser ainsi que leurs versions.

2) A quoi ressemble un module en python ?

Un module est un fichier python qui contient un ensemble de fonctions et des constantes.
En important le module, on a accès à toutes les fonctions définit dedans (fonctions, constantes,...).
Pour cela on peut utiliser : `import le_module` ou bien `from le_module import fonction`.

3) A quoi ressemble un package ?

Un package est un conteneur qui stocke un ensemble de fonctions qui ont des tâches spécifiques.
Pour créer un package il suffit de créer un dossier avec le fichier mon_fichier.py et un autre fichier nommé ```__init__.py``` qui permet d'indiquer à Pyhon que le dossier est un package.

Pour importer un package taper ```from le_package import*```, si on veut récupérer toutes les fonctions du package.
 
4) Créer un code python utilisant sous forme de module addition.py
OK (voir dans le dossier "Questions préparatoires"
pour utiliser le module dans ce cas: taper `from fichier.py import lafonction`

A quoi sert pip ?

Pip est un système de gestion de paquet qui permet d'installer des librairies en python et de les gérer, (choix de version,...).
Pour télecharger une librairie avec pip taper : `pip download nom_librairie`
Pour installer une librairie avec pip taper : `pip install nom_librairie`
Pour désinstaller une librairie : `pip uninstall nom_librairie`
Pour voir toute les possibilités de commande : taper `pip` dans un terminal

6) A quoi sert PYTHONPATH ?

Le pythonpath permet d'indiquer à python quels dossiers il doit prendre en compte pour sa recherche de modules.
Lorsque l'on utilise un `import le_module` au début d'un code, l'interpréteur Python va rechercher le module en regardant une liste prédéfinie de répertoire (définit dans le Python Path).

7) Où sont stockés les paquets installé par pip ?

Les paquets sont enregistrés dans l'environnement virtuel qui est actif.

8) A quoi sert pip install –user ?

Cette commande permet d'installer des paquet (librairie) venant du gestionnaire de paquet pip.
Le paramètre `--user` permet d'installer les packages dans le répertoire home, de plus cette option ne nécessite pas d'avoir des privilèges root.  

9) A quoi sert venv ?

Venv permet de créer des environnements virtuels et permet d'installer pip dans tous ces environnements.

10) Comment utiliser venv ?

Pour utiliser venv :

1) ```python -m venv <environment name>``` # permet de créer un environnement virtuel
2) ```source env/bin/activate ``` # pour activer l'environnement virtuel
3) Pour quitter l'environnement virtuel ```deactivate```


11) A quoi sert docker ?

(Source :https://aws.amazon.com/fr/docker/)

Docker est une plateforme logiciel permettant de concevoir, tester et déployer des applications rapidement. 
Cette plateforme intègre les logiciels dans des unités normalisées appelées conteneurs, qui rassemblent tous les éléments nécessaires à leur fonctionnement, 
dont les bibliothèques, les outils système, le code et l'environnement d'exécution.

Docker vous permet d'envoyer du code plus rapidement, de standardiser les opérations de vos applications, de migrer aisément du code et de faire des économies en améliorant l'utilisation des ressources. Il s’agit d’un environnement d’exécution léger, et d’une alternative aux méthodes de virtualisation traditionnelles basées sur les machines virtuelles.
L’une des pratiques clés du développement de logiciel moderne est d’isoler les applications déployées sur un même hôte ou sur un même cluster. Ceci permet d’éviter qu’elles interfèrent.

12) Comment utiliser docker ?

Comme dis précédemment docker est une plateforme permettant de faciliter les tests et le déploiement d'application :

Il faut se créer un compte sur la plateforme docker.

Les commandes principale pour utiliser docker sont les suivantes :
```
docker ps (permet de lister les conteneurs existants)
docker run image (permet d'éxécuter une image)
docker image ls (permet de lister les images existantes)
docker stop conteneur (permet de stopper un conteneur)
docker rm conteneur (permet de supprimmer un conteneur)
```
