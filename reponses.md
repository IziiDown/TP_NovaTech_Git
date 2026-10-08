1. l’identifiant court du premier commit : 3e9bb22
2. le commit correspondant à l’ajout de la page Contact : b6df9d4
3. le nombre actuel de commits : 6
4. la commande utilisée pour afficher l’historique sous forme graphique : git log --oneline --graph --all

Examen d'un commit de la fonctionnalité Contact :
    - Commande utilisée : git show b6df9d4


Partie 5 - Annuler correctement

- Commande choisie : git reset --soft HEAD~1
- Pourquoi les modifications sont toujours présentes : Le mode --soft annule uniquement le commit et conserve toutes les modifications, ce qui permet de ne pas perdre son travail.
- Méthode qui aurait supprimé les modifications : La commande git reset --hard HEAD~1 aurait annulé le commit ET supprimé définitivement les modifications des fichiers de travail.

