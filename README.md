# SUJET_4ETI_AdmCO_20232024_PEINADO

**Activités AdmCo Partie 1 2023-2024**

# I. Objectif

Le but de ce TP est de créer un calculateur pouvant réaliser les opérations simples (addition, soustraction, multiplication et division) sur 2 nombres complexes en utilisant la notion de classe et de package.
Il a pour objectif de nous familiariser avec les commandes git et l'utilisation de site tel que https://gitlab.com/ et https://github.com/.
Enfin, plus généralement, ce premier TP avait pour but de nous faire appréhender la gestion d'un projet (avec du code) ainsi que les bonnes pratiques à respecter.

# II. Organisation du projet

Le projet ce présente que ceci :

```.
├── calculator
│   ├── class_calculator.py
│   ├── __init__.py
│   └── __pycache__
│       └── class_calculator.cpython-311.pyc
├── README.md
└── test
    ├── debug.log
    ├── __init__.py
    └── test.py
```
1) Le package calculator :

Ce package permet de contenir la partie fonctionnelle de notre code, le fichier class_calculator.py contient la classe SimpleComplexCalculator qui va réaliser les opérations de base sur deux nombres complexes.

Voici un extrait de la classe SimpleComplexCalculator : 

```
class SimpleComplexCalculator:

    def __init__(self,tuple1,tuple2):
        self.tuple1=tuple1
        self.tuple2=tuple2

    def somme(self):
        somme_partie_relle= self.tuple1[0]+self.tuple2[0]
        somme_partie_imaginaire= self.tuple1[1]+self.tuple2[1]
        return somme_partie_relle,somme_partie_imaginaire

    def soustraction(self):
        soustraction_partie_relle= self.tuple1[0]-self.tuple2[0]
        soustraction_partie_imaginaire= self.tuple1[1]-self.tuple2[1]
        return soustraction_partie_relle,soustraction_partie_imaginaire
```
On peut voir que le constructeur de la classe prend en paramètre 2 tuples qui correspondent chacun à un nombre complexe.

2) Le package test :

Ce package nous permet de faire des tests de fonctionnalités sur notre classe SimpleComplexCalculator contenu dans le package calculator.
Pour pouvoir faire des tests en appelant le package calculator, il faut l'importer dans le programme :
```import calculator ``` ou bien ```from calculator import methodes```
On doit aussi ajouter le package calculator dans le Pythonpath pour ne pas avoir d'erreur lors de l'importation.

A COMPLETER

Voici un extrait de la classe MyTestCase : 
```
class MyTestCase(unittest.TestCase):
    '''Classe permettant de tester la classe "class_calculator" '''

    def test_addition(self):
        '''Classe permettant de tester la methode addition '''
        calculateur = SimpleComplexCalculator((1,2), (3,4)) #cas tous se passe bien
        resultat = calculateur.somme()
        calculateur2 = SimpleComplexCalculator((1.5,2), (3,4)) #cas erreur
        resultat2 = calculateur2.somme()
        return self.assertEqual(resultat[0],4), self.assertEqual(resultat[1],6), self.assertEqual(resultat2,"ERROR"), logger.info("Test addition => OK")

    def test_soustraction(self):
        '''Classe permettant de tester la methode soustraction.'''
        calculateur = SimpleComplexCalculator((1,2), (3,4))
        resultat = calculateur.soustraction()
        calculateur2 = SimpleComplexCalculator((1.5,2), (3,4)) #cas erreur
        resultat2 = calculateur2.soustraction()
        return self.assertEqual(resultat[0],-2), self.assertEqual(resultat[1],-2), self.assertEqual(resultat2, "ERROR"), logger.info("Test soustraction => OK")
```

Pour réaliser ces tests on utilise plusieurs librairies :

a) Librairie unittest :

Cette librairie permet d'automatiser des tests, pour l'utiliser on créer une classe et à chaque méthode on définit des tests spécifiques.
Pour utiliser cette librairie : ```import unittest ```

a) Librairie logging :

Cette librairie permet d'afficher de dialoguer avec l'utilisateur avec des messages d'informations, d'erreurs,...

# Applications des bonnes pratiques

pep 8 et pep20
black et pylint

# Environnement virtuel

Pour créer un environnement virtuel et 

# Librairie nécessaires

Lancer un environnement virtuel (cf section: Environnement virtuel ) pour y installer les librairies nécessaires au projet.

Pour les tests:
unittest + logging

Pour les bonnes 


# Récupération du projet en ligne

Pour rendre accessible la partie fonctionnelle du projet (la classe qui réalise les opérations), 

Pour récupérer le projet en ligne

# Liens vers gitlab

exercice 0:  liens
exercice 1: 


# Ressources

(liens)


