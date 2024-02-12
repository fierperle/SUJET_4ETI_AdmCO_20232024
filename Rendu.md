# Rendu AdminCo 2024 
**Louis ROBERT**

## Questions Préparatoires

 1. Expliquer de code  (addition.py):
```python
def add(x, y):
  z=x+y
  print('add() executed under the scope: ', __name__)
  return z

if __name__ == '__main__':
  x=input('Enter the first number to add: ')
  y=input('Enter the second number to add: ')
  result = add(int(x),int(y))
  print(x, '+', y,'=', result)
  print('Code executed under the scope: ', __name__)
```
Le fichier addition.py est un module python qui contient une fonction add qui prend deux paramètres x et y et qui retourne la somme de ces deux paramètres. La fonction add affiche également le nom du scope dans lequel elle est exécutée. Si le module est exécuté directement, il demande à l'utilisateur d'entrer deux nombres et exécute la fonction add avec ces deux nombres. Il affiche également le nom du scope dans lequel il est exécuté.

2. A quoi sert requirments.txt ?

Le fichier requirements.txt est un fichier texte qui contient la liste des dépendances d'un projet python. Il est utilisé par pip pour installer les dépendances d'un projet python.

3. A quoi ressemble un module en python ?

Un module en python est un fichier python qui contient des fonctions, des classes et des variables. Il peut également contenir du code exécutable. Un module peut être importé dans un autre module pour utiliser ses fonctions, classes et variables.

4. A quoi ressemble un package ?

Un package en python est un répertoire qui contient un fichier spécial nommé __init__.py et d'autres modules ou packages. Le fichier __init__.py peut être vide ou contenir du code exécutable. Un package peut être importé dans un autre module pour utiliser ses modules et packages.

5. Créer un code python utilisant sous forme de module addition.py

```python
from addition import add
#liste des nombres à additionner
nombres = [1, 2, 3, 4, 5]
#initialisation de la somme
somme = 0
#addition des nombres
for nombre in nombres:
    somme = add(somme, nombre)
#affichage du résultat
print("La somme des nombres est", somme)
```	

6. A quoi sert pip ? 

pip est un gestionnaire de paquets pour python. Il est utilisé pour installer, désinstaller et gérer les dépendances d'un projet python.

7. A quoi sert PYTHONPATH ?

PYTHONPATH est une variable d'environnement qui contient une liste de répertoires dans lesquels python recherche les modules et les packages.

8. Où sont stockés les paquets installé par pip ?

Les paquets installés par pip sont stockés dans le répertoire site-packages du répertoire d'installation de python.

9. A quoi sert pip install –user ? 

pip install --user est utilisé pour installer un paquet python pour un utilisateur spécifique. Le paquet est installé dans le répertoire ~/.local/lib/pythonX.Y/site-packages, où X.Y est la version de python.

10. A quoi sert venv ? 

venv est un module python qui est utilisé pour créer des environnements virtuels. Un environnement virtuel est un environnement python isolé qui contient sa propre installation de python, ses propres modules et ses propres packages.

11. Comment utiliser venv ?

Pour créer un environnement virtuel avec venv, il faut exécuter la commande suivante dans un terminal:
```bash
python3 -m venv /chemin/vers/environnement/virtuel
```
Pour activer l'environnement virtuel, il faut exécuter la commande suivante dans un terminal:
```bash
source /chemin/vers/environnement/virtuel/bin/activate
```

12. A quoi sert docker ?

Docker est une plateforme de conteneurisation qui permet de créer, de déployer et de gérer des conteneurs. 
Un conteneur est une unité logicielle qui contient une application et toutes ses dépendances. Docker permet d'isoler les applications et de les exécuter de manière cohérente sur n'importe quelle plateforme.

13. Comment utiliser docker ?

Pour utiliser docker, il faut d'abord créer un fichier Dockerfile qui contient les instructions pour construire une image docker.
Ensuite, il faut exécuter la commande suivante dans un terminal pour construire une image docker à partir du Dockerfile:
```bash
docker build -t nom_image .
```
Enfin, il faut exécuter la commande suivante dans un terminal pour exécuter un conteneur à partir de l'image docker:
```bash
docker run nom_image
```

## Exercice 0

1. A quoi sert git config , Quelles sont les informtions minimales à renseigner. Est ce bien fait sur votre ordinateur ?

git config est utilisé pour configurer git. Les informations minimales à renseigner sont le nom d'utilisateur et l'adresse e-mail.

1. Quelles sont les commandes de bases git ? a quoi servent elles ? 

Les commandes de base de git sont:
- ```git init```: initialise un dépôt git
- ```git add```: ajoute des fichiers à l'index
- ```git commit```: enregistre les modifications dans le dépôt
- ```git status```: affiche l'état des fichiers
- ```git log```: affiche l'historique des commits
- ```git push```: envoie les commits vers un dépôt distant
- ```git pull```: récupère les commits depuis un dépôt distant
- ```git clone```: clone un dépôt distant
- ```git branch```: crée, supprime ou affiche des branches
- ```git checkout```: change de branche ou restaure des fichiers
- ```git merge```: fusionne des branches
- ```git rebase```: réapplique des commits

Expliquez a quoi correspond ce worklow et pourquoi c'est une bonne pratique 

Le workflow présenté sur l'image présente 6 branches: master, hotfix, release, develop, feature1 et feature2.
ce workflow est une bonne pratique car il permet de séparer les différentes étapes du développement logiciel:
- La branche __master__ contient le code en production.
- La branche __hotfix__ est utilisée pour corriger des bugs en production.
- La branche __release__ est utilisée pour préparer une nouvelle version du logiciel.
- La branche __develop__ contient le code en cours de développement.
- Les branches __feature1__ et __feature2__ sont utilisées pour développer de nouvelles fonctionnalités.
Ce workflow permet de travailler de manière collaborative et de gérer les différentes étapes du développement logiciel de manière efficace.

## Exercice 1 :

L'exercice 1 est disponible dans un repository dédié à cette exercice sur GitLab et est accessible via le lien suivant : [Exercice 1](https://gitlab.com/fierperle/gestcode-exo1)


## Exercice 2 :

L'exercice 2 est disponible dans un repository dédié à cette exercice sur GitLab et est accessible via le lien suivant : [Exercice 2](https://gitlab.com/fierperle/gestcode-exo2)

## Exercice 3 : 
utilisation de pylint et black pour vérifier et formater le code python

**Pylint pour L'exercice 1**
Score d'origine: 8.54/10
Ce score est dû à l'absence de docstrings dans les fonctions
En ajoutant ces docstrings, le score passe à 9,51/10

**Pylint pour L'exercice 2**
Score d'origine: 8.22/10
Ce score est dû à l'absence de docstrings dans les fonctions et au nom du fichier qui ne respecte pas la convention snake_case
En ajoutant ces docstrings le score passe à 9.33/10

**Black**
Touts les fichiers ont été formatés avec black et respectent maintenant les conventions _PEP8_ et _PEP20_
note : c'est l'intégration de black dans l'IDE pycharm qui a été utilisée pour formater les fichiers

_Repository_ : pas de repository dédier à cette exercice, l'éolution des codes avec l'utilisation de pylint et black apparaisent à partir des commits nommés _"complied file to (pep8,pep20)"_

## Exercice 4 :

L'exercice 4 est disponible dans un repository dédié à cette exercice sur GitLab et est accessible via le lien suivant : [Exercice 4](https://gitlab.com/fierperle/gestcode-exo4)

## Exercice 5 :

L'exercice 5 est disponible dans un repository dédié à cette exercice sur GitLab et est accessible via le lien suivant : [Exercice 5](https://gitlab.com/fierperle/gestcode-exo5)

## Exercice 6 :

L'exercice 6 est disponible dans un repository dédié à cette exercice sur GitLab et est accessible via le lien suivant : [Exercice 6](https://gitlab.com/fierperle/gestcode-exo6)

## Exercice 7 :

L'exercice 7 est disponible dans un repository dédié à cette exercice sur GitLab et est accessible via le lien suivant : [Exercice 7](https://gitlab.com/fierperle/gestcode-exo7)

## Exercice 8 :

L'exercice 7 est disponible dans un repository dédié à cette exercice sur GitLab et est accessible via le lien suivant : [Exercice 7](https://gitlab.com/fierperle/gestcode-exo8)




