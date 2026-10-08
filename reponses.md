TP Git - NovaTech

Mission 5 :
1. b3717ba
2. 14ab41a
3. 9 commits
4. git log --oneline --graph
5. git show 14ab41a

Mission 8 :
J'ai utilisé git reset HEAD~1. Ça permet d'annuler le commit mais de garder les modifs dans les fichiers.
Si j'avais voulu tout supprimer (le commit et les modifs), j'aurais dû utiliser git reset --hard HEAD~1.

Mission 9 :
J'ai utilisé git revert HEAD. C'est différent du reset car ça ne supprime pas le commit de l'historique, ça en recrée un nouveau qui fait l'inverse. C'est important car le commit était déjà partagé, donc modifier l'historique aurait posé problème aux autres membres de l'équipe.

Mission 11 :
Commande : git cherry-pick 9ec4f26 
Identifiant récupéré : 9ec4f26
Une fusion classique (merge) aurait ramené tous les commits de la branche de test, y compris les modifs de couleur et le texte de test qu'on ne voulait pas. Avec cherry-pick on prend juste la correction de la faute.

Mission 12 :
Dans 1.0.0 :
- le 1 c'est pour une version majeure 
- le premier 0 c'est pour une version mineure 
- le dernier 0 c'est le patch 

Correction de bug mineur : 1.0.1
Nouvelle fonctionnalité : 1.1.0
Refonte majeure : 2.0.0

Questions finales :

1. La zone de travail c'est nos fichiers actuels sur le pc. Le staging (index) c'est l'endroit où on prépare ce qu'on va commit avec git add. L'historique c'est là où tous les commits sont définitivement sauvegardés.
2. Pour ne pas casser le code qui marche sur la branche main quand on fait des modifs, et c'est aussi plus simple pour bosser à plusieurs.
3. Le reset modifie le passé et supprime le commit, alors que le revert ajoute un nouveau commit qui fait l'inverse. Le revert est obligatoire si on a déjà push sur le serveur distant pour pas désynchroniser les autres.
4. Quand on bosse sur un truc pas fini mais qu'on doit changer de branche urgemment pour réparer un bug ailleurs (on fait un git stash).
5. Ça permet de prendre juste la modif qui nous intéresse au lieu de ramener tous les tests ou brouillons d'une autre branche.
6. HEAD c'est un curseur qui montre sur quel commit on se trouve actuellement.
7. C'est le commit qui se trouve 2 crans avant HEAD (donc le grand-père du commit actuel).
8. Ça sert à mettre une étiquette sur un commit précis, souvent pour marquer le numéro d'une version (ex: v1.0.0).
9. C'est plus facile de retrouver d'où vient un bug, de comprendre ce qui a été fait, ou d'annuler juste une petite partie sans tout casser.
10. Pour pas polluer le repo avec des trucs inutiles ou générés par le pc (logs, cache) et surtout pour ne pas partager des infos secrètes comme des mots de passe.
