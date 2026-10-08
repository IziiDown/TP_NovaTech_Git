## Partie 10 - Questions finales

1. Quelle différence existe-t-il entre la zone de travail, la zone de staging et l’historique ?

   * Zone de travail (Working Directory) : Contient les fichiers en cours de modification sur votre disque.
   * Zone de staging (Index) : Zone intermédiaire où l’on prépare et sélectionne précisément les modifications avec git add avant de créer un commit.
   * Historique (Dépôt Git) : Base de données contenant l’ensemble des commits enregistrés (snapshots) du projet.

2. Pourquoi est-il préférable de réaliser une fonctionnalité sur une branche dédiée ?
   Cela permet d’isoler le développement, d’éviter d’impacter le code stable présent sur la branche principale (main) et de pouvoir travailler en parallèle ou faire relire son code avant la fusion.

3. Quelle différence fondamentale existe-t-il entre les deux méthodes d’annulation utilisées dans les missions 8 et 9 ?

   * git reset (utilisé en mission 8) réécrit l’historique en déplaçant la branche vers un commit antérieur. Il est réservé aux commits locaux non partagés.
   * git revert (utilisé en mission 9) crée un nouveau commit qui annule les modifications du commit ciblé sans supprimer ni réécrire l’historique, ce qui est idéal pour les commits déjà partagés sur un dépôt distant.

4. Dans quelle situation est-il utile de mettre temporairement ses modifications de côté ?
   Lorsqu’on travaille sur une fonctionnalité non terminée et qu’on doit changer de branche en urgence (exemple : pour corriger un bug sur main) sans vouloir créer un commit incomplet ou polluer l’historique. On utilise alors git stash.

5. Pourquoi la récupération d’un commit précis peut-elle être préférable à la fusion complète d’une branche ?
   Si une branche contient plusieurs commits expérimentaux ou non finalisés, utiliser git cherry-pick permet d’extraire uniquement le commit utile (exemple : une correction de bug urgente) sans intégrer l’ensemble du travail incomplet présent sur la branche.

6. À quoi sert HEAD ?
   HEAD est un pointeur qui indique la position actuelle dans l’historique Git (pointe en général vers la branche courante, ou directement vers un commit en état detached HEAD).

7. Que représente HEAD~2 ?
   HEAD~2 désigne le commit situé deux niveaux avant le commit actuel (le grand-parent du commit vers lequel pointe HEAD).

8. À quoi sert un tag Git ?
   Un tag permet d’attribuer un nom clair et permanent à un commit spécifique dans l’historique, afin de repérer facilement des jalons ou des versions majeures publiées (exemple : v1.0.0).

9. Pourquoi des commits petits et précis facilitent-ils la maintenance d’un projet ?
   Des commits atomiques rendent l’historique lisible, facilitent les revues de code, simplifient les retours en arrière ou annulations (revert, cherry-pick) et rendent la recherche de bugs (git bisect) beaucoup plus efficace.

10. Pourquoi certains fichiers ne doivent-ils pas être versionnés ?
    Pour éviter d’encombrer le dépôt avec des fichiers générés temporairement ou volumineux (.log, cache/), et surtout pour des raisons de sécurité afin de ne pas exposer des identifiants ou informations sensibles (.env).
