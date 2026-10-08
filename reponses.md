1. l’identifiant court du premier commit : 3e9bb22
2. le commit correspondant à l’ajout de la page Contact : b6df9d4
3. le nombre actuel de commits : 6
4. la commande utilisée pour afficher l’historique sous forme graphique : git log --oneline --graph --all

Examen d'un commit de la fonctionnalité Contact :
    - Commande utilisée : git show b6df9d4


Partie 5 - Annuler correctement

### Mission 8 : Commit local incorrect
- Commande choisie : git reset --soft HEAD~1
- Pourquoi les modifications sont toujours présentes : Le mode --soft annule uniquement le commit et conserve toutes les modifications, ce qui permet de ne pas perdre son travail.
- Méthode qui aurait supprimé les modifications : La commande git reset --hard HEAD~1 aurait annulé le commit ET supprimé définitivement les modifications des fichiers de travail.

### Mission 9 : Commit partagé à annuler
- Pourquoi la méthode est différente de la mission 8 : Le commit ayant déjà été partagé sur le dépôt distant (GitHub), modifier l'historique avec un reset poserait des problèmes de synchronisation pour les autres développeurs. git revert crée un nouveau commit d'annulation, ce qui conserve l'historique intact et sécurisé pour le travail d'équipe.

## Partie 7 - Récupérer une modification précise

### Mission 11 : Correction isolée
- Commande utilisée : git cherry-pick d92a09b
- Identifiant du commit récupéré : d92a09b
- Pourquoi une fusion classique n'était pas adaptée : Une fusion classique (git merge) aurait également intégré le commit 1 (expérimentation de couleurs) et le commit 3 (texte de test du footer) sur la branche principale, alors que seule la correction orthographique du commit 2 devait être conservée.

## Partie 8 - Préparer une version

### Mission 12 : Version stable
  - 1 (Majeure) : Évolutions importantes ou changements incompatibles avec la version précédente.
  - 0 (Mineure) : Ajout de nouvelles fonctionnalités tout en conservant la compatibilité ascendante.
  - 0 (Correctif) : Corrections de bugs ou ajustements mineurs sans impact sur les fonctionnalités existantes.

- Versions suivantes selon les situations :
  - Correction de bug mineur : v1.0.1
  - Nouvelle fonctionnalité compatible : v1.1.0
  - Refonte majeure incompatible : v2.0.0