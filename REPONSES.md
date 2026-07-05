# Git Practice
# Fichier de reponse
## Partie 1
1.  a) *git init* : sert a initialiser git dans le dossier courant pour tracker tout les changements
    b) Aprés cette commande un dossier caché est créé nommé *.git*
2. Le fichier *README* est considéré comme non suivi car il n'a pas encore étè ajouter comme prêt pour la prochaine étape (staging) avec *git add README*
3. a) Différence :
    - *git add* permet d'ajouter les changements dans l'étape de staging
    - *git commit* permet d'enregistrer les changements de façons permanente comme prét pour être pousser sur le dossier distant de GitHub
    b) Il sépare les deux étapes pour nous donner la possibilité de poucoir modifier nos changement avant de les enregistrés définitivement pour les poussées sur GitHub.
4. a) *git log* montre les informations sur les commits que nous avons fait.
    b) *git diff* permet de voir les changements apportés dans le dépots depuis le dernier commit

## Partie 2
1. a) Le dêpot local c'est le dossier physique present dans notre machine, le dêpot distant (remote) c'est le dossier de GitHub
    b) *git push* envoie le contenu de notre dêpot local dans notre dêpot distant
    c) Si nous perdions notre machine avant d'avoir fait le *git push* notre dêpot distant ne contiendra pas les modifications apportées dans notre dêpot local
2. Il faut pas versionner un fichier *.env* car il contient toutes les informations  sensibles du projet (comme les cles secretes , les mots de passe, les cle api ), et le dossier *node_modules* car c'est un dossier tres lourd qui contient toutes les dependances du projet qui peuvent etres installer manuellement; Si on les commits quand meme tout le monde aura acces aux informations sensibles du projet contenues dans le fichier *.env* et le chargement du commit sera lent a cause du dossier *node_modules* qui contient toutes les dependances du projet.
# Partie 3
1. Nous ne travaillons pas directement sur la branche *main* pour eviter les conflits de merge lorsque nous travaillons en equipe et que chaque personne modifient les mêmes lignes. Une branche represente une version du dépôt isolée du dépôt principale.
2. Aprés le ce push le code a étè mis sur la branche feature/about-page et le code de la branche main est n'a pas changé
# Partie 4
1. Une *pull request* sert a demandé l'avis de l'equipe avant de fusionner les codes des differentes branches, c'est le chef projet qui doit valider une PR avant de la fusionner.
2. On fait une un *git pull* sur sur main pour synchroniser le travail local avec celui de GitHub car la branche main a étè modifier en ligne et non sur notre machine en local.
# Partie 5
1. Ce conflit c'est produit parcequ'il ya eu differentes modification sur la meme ligne du fichier README.md
2. Les marqueurs **<<<<, =====, >>>>** servent a delimitter la zone de conflit
3. Nous aurions pu eviter ce conflit en amont en modifiant une ligne differentes
# Partie 6
1. Le **fork** sert a copier un code open source sur notre serveur GitHub distant alors que le **clone** sert a copier integralement un depot depuis GitHub jusqu'a notre espace de travaille local; ce mecanisme est necessaire car il permet de suggerer des modifications a l'auteur sans modifier directement le depot.
2. Dans ce modele de contribution c'est l'auteur du depot qui garde le controle finale sur le code du depot d'origine, Il difere du travail en equipe par branche car il s'agit d'un changement de proprietaire du depot et non une branche isolée du code source.
# Partie 7
1. Une issue sert a signaler une idee ou un probleme alors qu'une pull request sert a proposer la modification.
2. Lorsqu'on fusionne une PR qui contient **closes #numero**, le status du ticket passe de *Open* a *closed* avec la mention qu'il a ete resolut par cette PR
# Partie 8
1. Un **tag Git** sert a numerote les versions d'un projet, il est utile car il permet de revenir sur une version specifique du code apres livraison si un bug survient sans avoir a retenir l'ID de son commit.
2. **git revert** sert a cree un nouveau commit pour annuler les modification du commit precedent, **git reset --hard** force le projet a revenir a l'etat du commit precedent et supprime tous les commits qui ont ete fait apres, Le plus est sûre a utiliser sur une branche deja partagée est *git revert* car il ne supprime pas les commits mes ajoute un nouveau et ne modifie pas les fichiers locaux en cours.
