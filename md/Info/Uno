#Projet d'entrainement pour la rentrée : Jeu du Uno en UDP

Le but de cette exercice est de récreer un Uno basique en réseau que vous pourrez parfaire si vous le souhaitez.


## Les fonctionnalités attendus

- à l'entrée du premier joueur, le serveur demendera combien de joueur devront rejoindre (entre 1 et 6)
- une barre avec les cartes qui devront s'afficher en ligne numéroté plus une dernière qui représentera la pioche
- un tableau des scores en haut avec les noms des joueurs et leurs cartes restantes
- quand on doit jouer, il faudra entrain un numéro qui sera celui de la barre des cartes

** Bonus ** 
- afficher en blanc le joueur entrain de jouer
- ajouter les cartes +2, +4, ↔, Ø, multicolor


## Les fonctions données

ces fonctions seront nécessaires pour le bon déroulé de votre programme et ne seront pas à expliquer

```python
def colored(text,color):
	colors = {"jaune":"43","bleu":"44","rouge":"41","vert":"42"}
	return '\x1b[6;30;'+ colors[color] +'m' + text + '\x1b[0m'

def carte(text,color):
	carte = ""
	carte += colored("╔═════╗",color) + "\n"
	carte += colored("║     ║",color) + "\n"
	carte += colored("║  "+text+"  ║",color) + "\n"
	carte += colored("║     ║",color) + "\n"
	carte += colored("╚═════╝",color)
	return carte
```
